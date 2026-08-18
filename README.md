<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>O Agronegocio no Parana</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            color: #222;
        }
        header {
            background-color: #1b5e20;
            color: #ffffff;
            padding: 20px;
            text-align: center;
        }
        nav {
            background-color: #2e7d32;
            padding: 10px;
            text-align: center;
        }
        nav a {
            color: #ffffff;
            margin: 0 15px;
            text-decoration: none;
            font-weight: bold;
        }
        nav a:focus, nav a:hover {
            text-decoration: underline;
            outline: 2px solid #ffffff;
        }
        main {
            max-width: 900px;
            margin: 20px auto;
            padding: 20px;
            background: #ffffff;
            border-radius: 8px;
        }
        section {
            margin-bottom: 30px;
        }
        h1, h2 {
            color: #1b5e20;
        }
        a.fonte-link {
            color: #1b5e20;
            text-decoration: underline;
        }
        a.fonte-link:hover {
            color: #2e7d32;
        }
        footer {
            background-color: #1b5e20;
            color: #ffffff;
            text-align: center;
            padding: 15px;
            font-size: 0.9em;
        }
    </style>
</head>
<body>

    <header role="banner">
        <h1>O Agronegocio no Parana</h1>
        <p>A forca da producao agricola e pecuaria do estado</p>
    </header>

    <nav role="navigation" aria-label="Menu principal">
        <a href="#sobre">Sobre</a>
        <a href="#produtos">Principais Produtos</a>
        <a href="#fontes">Fontes e Pesquisas</a>
        <a href="#direitos">Direitos Autorais</a>
    </nav>

    <main role="main">
        <section id="sobre" aria-labelledby="titulo-sobre">
            <h2 id="titulo-sobre">Sobre o Setor</h2>
            <p>
                O estado do Parana e reconhecido como um dos maiores produtores de alimentos do Brasil, posicao comprovada por dados de institutos de pesquisa oficiais como o <a href="#ref-seab" class="fonte-link">DERAL/SEAB</a> e o <a href="#ref-ibge" class="fonte-link">IBGE</a>. Com solo fertil e o constante avanco de tecnologias no campo impulsionadas por orgaos como o IDR-Parana e a Embrapa, a agricultura e a pecuaria garantem o desenvolvimento economico da regiao e o abastecimento de diversos paises.
            </p>
        </section>

        <section id="produtos" aria-labelledby="titulo-produtos">
            <h2 id="titulo-produtos">Principais Culturas e Producoes</h2>
            <ul>
                <li><strong>Soja:</strong> Um dos itens mais exportados do estado, com acompanhamento de safra validado pelo <a href="#ref-seab" class="fonte-link">DERAL</a>.</li>
                <li><strong>Milho:</strong> Essencial para a alimentacao animal e consumo interno e externo.</li>
                <li><strong>Trigo:</strong> O Parana lidera nacionalmente a producao deste grao, segundo levantamentos continuos de safra.</li>
                <li><strong>Proteina Animal:</strong> Destaque na avicultura e suinocultura, com certificacoes sanitarias e dados do <a href="#ref-ibge" class="fonte-link">IBGE (Pesquisa da Pecuaria Municipal)</a>.</li>
            </ul>
        </section>

        <!-- Nova secao para atender a necessidade de citar e disponibilizar fontes de pesquisas e noticias -->
        <section id="fontes" aria-labelledby="titulo-fontes">
            <h2 id="titulo-fontes">Fontes de Dados e Pesquisas</h2>
            <p>Para garantir a credibilidade das informacoes divulgadas e permitir que voce aprofunde seu conhecimento, fundamentamos nossos dados nas seguintes instituicoes e pesquisas oficiais:</p>
            <ul>
                <li id="ref-seab">
                    <strong>SEAB / DERAL:</strong> Secretaria da Agricultura e do Abastecimento do Parana e Departamento de Economia Rural. 
                    <br><a href="https://www.agricultura.pr.gov.br/DERA" target="_blank" rel="noopener noreferrer" class="fonte-link">Acesse os relatorios de safras e noticias do DERAL</a>
                </li>
                <li id="ref-ibge">
                    <strong>IBGE:</strong> Instituto Brasileiro de Geografia e Estatistica (Levantamento Sistematico da Producao Agricola). 
                    <br><a href="https://www.ibge.gov.br/" target="_blank" rel="noopener noreferrer" class="fonte-link">Consulte dados e pesquisas de producao agricola no IBGE</a>
                </li>
                <li id="ref-embrapa">
                    <strong>Embrapa & IDR-Parana:</strong> Pesquisas e inovacoes tecnologicas para o desenvolvimento sustentavel do campo.
                    <br><a href="https://www.embrapa.br/" target="_blank" rel="noopener noreferrer" class="fonte-link">Conheca as pesquisas cientificas da Embrapa</a>
                </li>
            </ul>
        </section>

        <section id="direitos" aria-labelledby="titulo-direitos">
            <h2 id="titulo-direitos">Direitos Autorais e Licenca</h2>
            <p>Todo o conteudo textual desta pagina foi produzido para fins informativos e educativos. A reproducao e permitida desde que citada a fonte original e os institutos de pesquisa mecionados responsaveis pelos dados apresentados.</p>
        </section>
    </main>

    <footer role="contentinfo">
        <p>&copy; 2026 Agronegocio no Parana. Todos os direitos reservados.</p>
    </footer>

</body>
</html>
