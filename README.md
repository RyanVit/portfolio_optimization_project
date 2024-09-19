# Projeto de Otimização de Portfólio de Investimentos

Este projeto realiza a otimização de portfólio de ações utilizando dados históricos do Yahoo Finance. Ele coleta os dados, armazena-os em um banco de dados PostgreSQL, calcula os pesos ótimos para maximizar o retorno ajustado ao risco e gera visualizações gráficas do desempenho do portfólio.

## Objetivo

O objetivo deste projeto é fornecer uma ferramenta que auxilie investidores a otimizar a alocação de ativos no portfólio, maximizando o retorno e minimizando o risco, com base em dados históricos de preços de ações.

---

## Funcionalidades

1. **Coleta de Dados de Ações**: Usa a biblioteca `yfinance` para baixar os dados históricos de ações específicas.
2. **Armazenamento no Banco de Dados**: Salva os dados coletados em um banco de dados PostgreSQL.
3. **Otimização de Portfólio**: Calcula a melhor distribuição de pesos para maximizar o retorno ajustado ao risco.
4. **Visualização de Retornos**: Gera gráficos de desempenho do portfólio.

---

## Tecnologias Utilizadas

- **Linguagem**: Python 3
- **Bibliotecas**:
  - `yfinance`: Coleta de dados de ações.
  - `SQLAlchemy`: Conexão com o banco de dados PostgreSQL.
  - `NumPy` e `SciPy`: Para cálculos de otimização.
  - `Pandas`: Manipulação de dados.
  - `Matplotlib`: Visualização de gráficos.
  - `Logging`: Para rastrear a execução e erros.

---

