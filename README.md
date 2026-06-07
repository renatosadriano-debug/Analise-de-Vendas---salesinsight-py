# SalesInsight PY

Pipeline de análise de dados de vendas desenvolvido em Python.

## Sobre o projeto

O SalesInsight PY é um mini-projeto de análise de dados que lê, limpa, transforma e analisa um dataset de vendas.

O objetivo é gerar métricas, segmentar clientes, calcular estatísticas com NumPy e criar visualizações para apoiar a análise comercial.

## Tecnologias utilizadas

- **Python**: linguagem principal utilizada no desenvolvimento do pipeline de análise de dados.

- **Pandas**: biblioteca utilizada para manipulação de dados em formato tabular, leitura e exportação de arquivos CSV, limpeza de dados, criação de colunas derivadas e cálculos agregados com DataFrames.

- **NumPy**: biblioteca utilizada para cálculos numéricos, estatísticas descritivas, operações com arrays e apoio à projeção simples de tendência.

- **Matplotlib**: biblioteca utilizada para criação, personalização e exportação de gráficos em formato PNG.

- **Seaborn**: biblioteca utilizada em conjunto com o Matplotlib para gerar visualizações estatísticas com melhor apresentação visual.

- **Jinja2**: biblioteca utilizada pelo Pandas para renderização e formatação visual de tabelas estilizadas com `.style`.

- **IPython**: pacote utilizado para recursos interativos no notebook, como `display()` e exibição de tabelas em HTML..

- **ipykernel**: pacote necessário para executar notebooks `.ipynb` no VS Code e em ambientes Jupyter.

- **Jupyter Notebook / VS Code**: ambientes utilizados para desenvolver, executar, testar e documentar o projeto.

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