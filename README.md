# portfolio_optimization_project

Este projeto realiza a otimização de portfólio de ações utilizando dados históricos do Yahoo Finance. Ele coleta os dados, armazena-os em um banco de dados PostgreSQL, calcula os pesos ótimos para maximizar o retorno ajustado ao risco e gera visualizações gráficas do desempenho do portfólio.

#Objetivo
O objetivo deste projeto é fornecer uma ferramenta que auxilie investidores a otimizar a alocação de ativos no portfólio, maximizando o retorno e minimizando o risco, com base em dados históricos de preços de ações.

###Funcionalidades
Coleta de Dados de Ações: Usa a biblioteca yfinance para baixar os dados históricos de ações específicas.
Armazenamento no Banco de Dados: Salva os dados coletados em um banco de dados PostgreSQL.
Otimização de Portfólio: Calcula a melhor distribuição de pesos para maximizar o retorno ajustado ao risco.
Visualização de Retornos: Gera gráficos de desempenho do portfólio.

###Tecnologias Utilizadas
Linguagem: Python 3
Bibliotecas:
yfinance: Coleta de dados de ações.
SQLAlchemy: Conexão com o banco de dados PostgreSQL.
NumPy e SciPy: Para cálculos de otimização.
Pandas: Manipulação de dados.
Matplotlib: Visualização de gráficos.
Logging: Para rastrear a execução e erros.

###Configurar o Banco de Dados
Criar um banco de dados PostgreSQL local.
Atualizar o arquivo config.py com a URL de conexão do banco de dados:
DATABASE_URL = "postgresql://usuario:senha@localhost:5432/nome_do_banco"

###Exemplo de Uso
Entrada do Usuário
Ao executar o script, o usuário será solicitado a inserir os tickers das ações e o intervalo de datas:
Digite os tickers das ações separados por vírgula (ex. AAPL, MSFT, GOOGL): AAPL, MSFT, GOOGL
Digite a data inicial no formato YYYY-MM-DD: 2023-01-01
Digite a data final no formato YYYY-MM-DD: 2023-12-31

###Saída Esperada
Pesos Otimizados para o Portfólio:
Pesos Otimizados: {'AAPL': 0.40, 'MSFT': 0.35, 'GOOGL': 0.25}
Banco de Dados
Os dados coletados para cada ação serão salvos em tabelas separadas no banco de dados PostgreSQL. A estrutura das tabelas segue o padrão abaixo:

Exemplo de Tabela AAPL_data:

timestamp	Open	High	Low	Close	Volume
2023-01-01	150.50	152.20	149.80	151.00	1000000
2023-01-02	151.00	153.50	150.50	152.00	1050000
...	...	...	...	...	...
