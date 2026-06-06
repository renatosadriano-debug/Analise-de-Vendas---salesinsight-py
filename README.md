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

- Geração de dataset sintético de vendas
- Leitura do arquivo `vendas.csv`
- Inspeção inicial dos dados com `shape`, colunas, tipos e valores nulos
- Criação de cópia de segurança do DataFrame original
- Limpeza de dados nulos, datas inválidas e espaços extras
- Imputação de quantidades nulas e preços unitários nulos
- Criação de colunas derivadas:
  - `receita_total`
  - `mes`
  - `mes_nome`
  - `trimestre`
  - `ano`
  - `faixa_receita_item`
  - `preco_medio_item`
  - `comparacao_preco_media`
  - `percentual_diferenca_media`
- Cálculo de métricas agregadas com `groupby`
- Segmentação de clientes por total gasto
- Cálculo de estatísticas com NumPy
- Normalização de receitas com operações vetorizadas
- Criação de gráficos com Matplotlib e Seaborn
- Exportação de relatórios em CSV e JSON
- Uso de expressões regulares para limpeza de strings
- Uso de funções lambda
- Uso de função que recebe outra função como parâmetro
- Criação da classe `AnalisadorDeVendas`
- Criação da classe `AnalisadorComProjecao` com herança
- Projeção simples de tendência com média móvel

## Como executar

1. Clone o repositório:

```bash
git clone https://github.com/renatosadriano-debug/Analise-de-Vendas---salesinsight-py.git
```

2. Acesse a pasta do projeto:

```bash
cd Analise-de-Vendas---salesinsight-py
```

3. Crie um ambiente virtual:

```bash
python -m venv .venv
```

4. Ative o ambiente virtual no Windows PowerShell:

```bash
.venv\Scripts\Activate.ps1
```

5. Instale as dependências do projeto:

```bash
pip install -r requirements.txt
```

6. Abra o projeto no VS Code:

```bash
code .
```

7. Execute o notebook principal:

```text
salesinsight.ipynb
```

Após abrir o notebook, execute as células em sequência, do início ao fim.


## Kanban do projeto

O acompanhamento das tarefas do projeto foi organizado no Notion.

Link do Kanban:

[Kanban — SalesInsight PY](https://app.notion.com/p/Mini-Projeto-Analise-de-Vendas-Ai-37235d940f7d804bbf60fb4f662b87c4?source=copy_link)