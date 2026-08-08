import requests
import pandas as pd

def buscar_dados_agro_parana():
    """
    Consulta a API do SIDRA / IBGE para obter a Producao Agricola Municipal (PAM)
    no Parana (UF 41).
    """
    # Tabela 1612: Area plantada, colhida e valor da producao agricola
    # UF 41 = Parana | Variavel 214 = Valor da Producao (R$ mil)
    url = "https://servicodados.ibge.gov.br/api/v3/agregados/1612/periodos/2023/variaveis/214?localidades=N3[41]"

    headers = {
        "User-Agent": "AcessibilidadeAgroApp/1.0 (contato@exemplo.com)"
    }

    try:
        response = requests.get(url, headers=headers, timeout=10)
        response.raise_for_status()
        dados = response.json()

        # Validacao da resposta da API
        if not dados or not isinstance(dados, list):
            print("Resposta da API veio vazia ou em formato inesperado.")
            return None

        resultados_api = dados[0].get("resultados", [])
        if not resultados_api:
            print("Nenhum resultado encontrado na consulta.")
            return None

        series = resultados_api[0].get("series", [])

        # Processamento e estruturacao dos dados
        lista_resultados = []
        for item in series:
            nome_localidade = item.get("localidade", {}).get("nome", "Desconhecido")
            historico_serie = item.get("serie", {})

            for ano, valor in historico_serie.items():
                lista_resultados.append({
                    "Estado": nome_localidade,
                    "Ano": ano,
                    "Valor_Producao_Mil_Reais": valor
                })

        # Criacao do DataFrame
        df = pd.DataFrame(lista_resultados)
        return df

    except requests.exceptions.RequestException as err:
        print(f"Erro na requisicao HTTP: {err}")
        return None
    except (KeyError, IndexError, TypeError) as err:
        print(f"Erro ao processar a estrutura dos dados JSON: {err}")
        return None

if __name__ == "__main__":
    dados_pr = buscar_dados_agro_parana()
    
    if dados_pr is not None and not dados_pr.empty:
        print(dados_pr.to_string(index=False))
    else:
        print("Nao foi possivel gerar a tabela de dados.")
