import requests
import pandas as pd

def buscar_dados_agro_parana():
    """
    Consulta a API do SIDRA / IBGE para obter a Produção Agrícola Municipal (PAM)
    no Paraná (UF 41).
    """
    # Exemplo: Tabela 1612 (Área plantada, colhida e valor da produção agrícola)
    # UF 41 = Paraná | Variavel 214 = Valor da Produção (R$ mil)
    url = "https://servicodados.ibge.gov.br/api/v3/agregados/1612/periodos/2023/variaveis/214?localidades=N3[41]"

    headers = {
        "User-Agent": "AcessibilidadeAgroApp/1.0 (contato@exemplo.com)"
    }

    try:
        response = requests.get(url, headers=headers)
        response.raise_for_status()
        dados = response.json()

        # Estruturação básica dos dados
        resultados = []
        for item in dados[0]['resultados'][0]['series']:
            localidade = item['localidade']['nome']
            serie = item['serie']
            for ano, valor in serie.items():
                resultados.append({
                    "Estado": localidade,
                    "Ano": ano,
                    "Valor_Producao_Mil_Reais": valor
                })

        df = pd.DataFrame(resultados)
        return df

    except Exception as e:
        print(f"Erro ao carregar dados: {e}")
        return None

if __name__ == "__main__":
    dados_pr = buscar_dados_agro_parana()
    if dados_pr is not None:
        print(dados_pr.to_string(index=False))
