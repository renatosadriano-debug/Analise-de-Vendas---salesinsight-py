# SalesInsight PY

Pipeline de análise de dados de vendas desenvolvido em Python.

## Sobre o projeto

O SalesInsight PY é um mini-projeto de análise de dados que lê, limpa, transforma e analisa um dataset de vendas.

O objetivo é gerar métricas, segmentar clientes, calcular estatísticas com NumPy e criar visualizações para apoiar a análise comercial.

## Tecnologias utilizadas

- **Python**: linguagem principal utilizada para desenvolver o pipeline de análise de dados.

- **Pandas**: biblioteca usada para trabalhar com tabelas, DataFrames, leitura de CSV, limpeza de dados, criação de colunas e agrupamentos.

- **NumPy**: biblioteca usada para cálculos numéricos, estatísticas, arrays, operações vetorizadas e normalização de dados.

- **Matplotlib**: biblioteca usada para criar gráficos e exportar visualizações em formato PNG.

- **Seaborn**: biblioteca usada em conjunto com o Matplotlib para gerar gráficos estatísticos com melhor apresentação visual.

- **ipykernel**: pacote necessário para executar notebooks `.ipynb` no VS Code.

- **jinja2**: biblioteca usada pelo Pandas para aplicar formatação visual em tabelas com `.style`.

- **Jupyter Notebook / VS Code**: ambiente utilizado para desenvolver, executar e testar o projeto.

- **Git e GitHub**: ferramentas utilizadas para versionamento do código, organização por branches e publicação do repositório.

## Arquivos do projeto

- `salesinsight.ipynb`: notebook principal do projeto
- `vendas.csv`: dataset de vendas
- `requirements.txt`: bibliotecas necessárias
- `outputs/`: relatórios e gráficos gerados
- `planejamento/tarefas-kanban.md`: organização das tarefas do projeto

## Funcionalidades implementadas

- Geração ou leitura do dataset de vendas
- Inspeção inicial dos dados
- Limpeza de dados nulos e datas inválidas
- Criação de colunas derivadas
- Cálculo de métricas agregadas
- Segmentação de clientes
- Estatísticas com NumPy
- Geração de gráficos
- Exportação de arquivos CSV, JSON e PNG

## Como executar

1. Clone o repositório:

```bash
git clone https://github.com/renatosadriano-debug/Analise-de-Vendas---salesinsight-py.git