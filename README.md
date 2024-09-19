# portfolio_optimization_project

    <h1>Projeto de Otimização de Portfólio de Investimentos</h1>

    <p>
        Este projeto realiza a otimização de portfólio de ações utilizando dados históricos do Yahoo Finance. Ele coleta os dados, armazena-os em um banco de dados PostgreSQL, calcula os pesos ótimos para maximizar o retorno ajustado ao risco e gera visualizações gráficas do desempenho do portfólio.
    </p>

    <h2>Objetivo</h2>

    <p>O objetivo deste projeto é fornecer uma ferramenta que auxilie investidores a otimizar a alocação de ativos no portfólio, maximizando o retorno e minimizando o risco, com base em dados históricos de preços de ações.</p>

    <h2>Funcionalidades</h2>
    <ul>
        <li>Coleta de Dados de Ações: Usa a biblioteca <code>yfinance</code> para baixar os dados históricos de ações específicas.</li>
        <li>Armazenamento no Banco de Dados: Salva os dados coletados em um banco de dados PostgreSQL.</li>
        <li>Otimização de Portfólio: Calcula a melhor distribuição de pesos para maximizar o retorno ajustado ao risco.</li>
        <li>Visualização de Retornos: Gera gráficos de desempenho do portfólio.</li>
    </ul>

    <h2>Tecnologias Utilizadas</h2>
    <ul>
        <li><strong>Linguagem</strong>: Python 3</li>
        <li><strong>Bibliotecas</strong>:
            <ul>
                <li><code>yfinance</code>: Coleta de dados de ações.</li>
                <li><code>SQLAlchemy</code>: Conexão com o banco de dados PostgreSQL.</li>
                <li><code>NumPy</code> e <code>SciPy</code>: Para cálculos de otimização.</li>
                <li><code>Pandas</code>: Manipulação de dados.</li>
                <li><code>Matplotlib</code>: Visualização de gráficos.</li>
                <li><code>Logging</code>: Para rastrear a execução e erros.</li>
            </ul>
        </li>
    </ul>

    <h2>Instalação</h2>

    <h3>1. Clonar o Repositório</h3>
    <pre><code>git clone https://github.com/seuusuario/portfolio-optimization.git
cd portfolio-optimization
</code></pre>

    <h3>2. Criar e Ativar um Ambiente Virtual</h3>
    <pre><code>python3 -m venv venv
source venv/bin/activate
</code></pre>

    <h3>3. Instalar as Dependências</h3>
    <pre><code>pip install -r requirements.txt</code></pre>

    <h3>4. Configurar o Banco de Dados</h3>
    <p>1. Criar um banco de dados PostgreSQL local.<br>
       2. Atualizar o arquivo <code>config.py</code> com a URL de conexão do banco de dados:</p>
    <pre><code>DATABASE_URL = "postgresql://usuario:senha@localhost:5432/portfolio_db"</code></pre>

    <h3>5. Executar o Projeto</h3>
    <pre><code>python main.py</code></pre>

    <h2>Exemplo de Uso</h2>

    <h3>Entrada do Usuário</h3>
    <p>Ao executar o script, o usuário será solicitado a inserir os tickers das ações e o intervalo de datas:</p>
    <pre><code>Digite os tickers das ações separados por vírgula (ex. AAPL, MSFT, GOOGL): AAPL, MSFT, GOOGL
Digite a data inicial no formato YYYY-MM-DD: 2023-01-01
Digite a data final no formato YYYY-MM-DD: 2023-12-31
</code></pre>

    <h3>Saída Esperada</h3>

    <h4>1. Pesos Otimizados para o Portfólio:</h4>
    <pre><code>Pesos Otimizados: {'AAPL': 0.40, 'MSFT': 0.35, 'GOOGL': 0.25}</code></pre>

    <h4>2. Visualização de Retornos (Gráfico):</h4>
    <p>O gráfico abaixo mostra os retornos cumulativos do portfólio com os pesos otimizados:</p>
    <img src="example_returns_chart.png" alt="Gráfico de Retornos">

    <h2>Banco de Dados</h2>
    <p>Os dados coletados para cada ação serão salvos em tabelas separadas no banco de dados PostgreSQL. A estrutura das tabelas segue o padrão abaixo:</p>

    <h4>Exemplo de Tabela <code>AAPL_data</code>:</h4>
    <table border="1">
        <tr>
            <th>timestamp</th>
            <th>Open</th>
            <th>High</th>
            <th>Low</th>
            <th>Close</th>
            <th>Volume</th>
        </tr>
        <tr>
            <td>2023-01-01</td>
            <td>150.50</td>
            <td>152.20</td>
            <td>149.80</td>
            <td>151.00</td>
            <td>1000000</td>
        </tr>
        <tr>
            <td>2023-01-02</td>
            <td>151.00</td>
            <td>153.50</td>
            <td>150.50</td>
            <td>152.00</td>
            <td>1050000</td>
        </tr>
    </table>

    <h2>Explicação dos Componentes</h2>

    <h3>Coleta de Dados</h3>
    <p>Os dados históricos das ações são coletados usando a API <code>yfinance
