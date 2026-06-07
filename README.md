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

- **IPython**: pacote utilizado para recursos interativos no notebook, como `display()` e exibição de tabelas em HTML.

- **ipykernel**: pacote necessário para executar notebooks `.ipynb` no VS Code e em ambientes Jupyter.

- **Jupyter Notebook / VS Code**: ambientes utilizados para desenvolver, executar, testar e documentar o projeto.

- **Git e GitHub**: ferramentas utilizadas para versionamento do código, organização por branches e publicação do repositório.

## Arquivos e estrutura do projeto

```text
salesinsight-py/
│
├── salesinsight.ipynb
├── vendas.csv
├── requirements.txt
├── README.md
│
├── outputs/
│   ├── relatorio_resumo.csv
│   ├── relatorio_metricas.json
│   ├── relatorio_top3_clientes_por_mes.csv
│   ├── relatorio_top3_clientes_ano_2024.csv
│   ├── relatorio_desconto_top10_clientes_2024.csv
│   │
│   └── graficos/
│       ├── grafico_top3_clientes_por_mes.png
│       ├── grafico_top3_clientes_ano_2024.png
│       └── demais gráficos gerados pelo pipeline
│
└── planejamento/
    └── tarefas-kanban.md
    
- `salesinsight.ipynb`: notebook principal do projeto, contendo o pipeline completo de análise de vendas.

- `vendas.csv`: dataset utilizado no projeto. Caso o arquivo não exista, o pipeline pode gerar um dataset sintético automaticamente.

- `requirements.txt`: arquivo com as bibliotecas necessárias para instalação do ambiente.

- `README.md`: documentação principal do projeto.

- `outputs/`: pasta destinada aos relatórios gerados pelo pipeline.

- `outputs/graficos/`: pasta destinada aos gráficos exportados em formato PNG.

- `planejamento/tarefas-kanban.md`: arquivo de apoio para controle das tarefas e requisitos do projeto.

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

## Classes e herança no projeto

O projeto utiliza programação orientada a objetos para organizar o pipeline de análise de dados.

A classe principal `AnalisadorDeVendas` concentra as etapas centrais do processo, como carregamento do arquivo CSV, limpeza dos dados, criação de colunas derivadas, cálculo de métricas, geração de gráficos e exportação de relatórios.

```python
class AnalisadorDeVendas:
```

Essa classe funciona como a estrutura base do pipeline, mantendo os principais atributos do projeto, como `df_bruto`, `df_limpo`, `metricas` e `clientes`.

Também foi criada a classe `AnalisadorComProjecao`, que herda de `AnalisadorDeVendas`:

```python
class AnalisadorComProjecao(AnalisadorDeVendas):
```

Essa classe filha reaproveita todos os métodos da classe principal e adiciona funcionalidades específicas de projeção simples de tendência, como o método `projetar_tendencia()`.

No construtor da classe filha, foi utilizado `super()` para chamar o construtor da classe pai:

```python
def __init__(self, caminho_arquivo, meses_projecao=3):
    super().__init__(caminho_arquivo)
    self.meses_projecao = meses_projecao
    self.projecoes = []
```

O uso de `super().__init__(caminho_arquivo)` permite inicializar corretamente os atributos herdados da classe `AnalisadorDeVendas`, como o caminho do arquivo, os DataFrames e as métricas. Em seguida, a classe filha adiciona seus próprios atributos, como `meses_projecao` e `projecoes`.

Com isso, o projeto aplica herança de forma prática, evitando repetição de código e permitindo estender o comportamento do pipeline original.

## Como executar no VS Code

Esta é a receita de execução do projeto **SalesInsight PY** no VS Code.

### Pré-requisitos

Antes de iniciar, confirme que você possui instalado:

- Python
- VS Code
- Extensão Jupyter no VS Code
- Git

### Receita de execução

1. Abra o terminal na pasta onde deseja salvar o projeto.

2. Clone o repositório do GitHub:

```bash
git clone https://github.com/renatosadriano-debug/Analise-de-Vendas---salesinsight-py.git
```

3. Entre na pasta do projeto:

```bash
cd Analise-de-Vendas---salesinsight-py
```

4. Crie um ambiente virtual para o projeto:

```bash
python -m venv .venv
```

5. Ative o ambiente virtual no Windows PowerShell:

```bash
.venv\Scripts\Activate.ps1
```

6. Instale as bibliotecas necessárias:

```bash
pip install -r requirements.txt
```

7. Abra o projeto no VS Code:

```bash
code .
```

8. No VS Code, abra o notebook principal:

```text
salesinsight.ipynb
```

9. Selecione o kernel Python do ambiente virtual.

No canto superior direito do notebook, escolha o kernel relacionado ao ambiente `.venv`, normalmente exibido como:

```text
Python (.venv)
```

10. Execute as células do notebook em sequência, do início ao fim.

Durante a execução, o pipeline irá carregar o arquivo `vendas.csv`. Caso esse arquivo não exista, o próprio notebook poderá gerar um dataset sintético automaticamente.

11. Ao final da execução, confira os arquivos gerados.

Os relatórios serão salvos em:

```text
outputs/
```

Os gráficos serão salvos em:

```text
outputs/graficos/
```

### Resultado esperado

Ao executar o notebook completo, o projeto realiza:

- leitura do dataset de vendas;
- limpeza e padronização dos dados;
- criação de colunas derivadas;
- cálculo de métricas agregadas;
- segmentação de clientes;
- cálculo de estatísticas com NumPy;
- geração de gráficos com Matplotlib e Seaborn;
- projeção simples de tendência;
- ranking dos principais clientes;
- relatório de descontos para clientes com maior faturamento;
- exportação de relatórios e gráficos.

Após a execução, o projeto estará pronto para análise dos resultados dentro do próprio notebook e também pelos arquivos exportados nas pastas `outputs/` e `outputs/graficos/`.

## Versionamento com GitHub

O projeto foi versionado com Git e publicado no GitHub. O repositório permite acompanhar a evolução do código, registrar alterações importantes e organizar o desenvolvimento por meio de branches.

O fluxo utilizado no projeto segue a lógica de desenvolvimento por etapas:

```text
main
develop
branches de funcionalidades
```

A branch `main` representa a versão principal do projeto. A branch `develop` é utilizada como base de desenvolvimento, onde as melhorias são integradas antes de serem consideradas estáveis. Para novas funcionalidades, são criadas branches específicas, permitindo trabalhar em alterações sem comprometer diretamente a versão principal.

Exemplo de criação de branch para uma nova funcionalidade:

```bash
git checkout -b feat/ranking-clientes
```

Após implementar uma alteração, os arquivos são adicionados ao controle de versão:

```bash
git add .
```

Em seguida, é criado um commit com uma mensagem objetiva:

```bash
git commit -m "feat: adiciona ranking de clientes por faturamento"
```

Depois, a branch é enviada para o GitHub:

```bash
git push -u origin feat/ranking-clientes
```

No GitHub, as alterações podem ser revisadas e integradas por meio de Pull Request. Esse processo ajuda a manter o histórico organizado e facilita a rastreabilidade das melhorias implementadas no projeto.

Repositório do projeto:

```text
https://github.com/renatosadriano-debug/Analise-de-Vendas---salesinsight-py
```


## Kanban do projeto

O acompanhamento das tarefas do projeto foi organizado no Notion.

Link do Kanban:

[Kanban — SalesInsight PY](https://app.notion.com/p/Mini-Projeto-Analise-de-Vendas-Ai-37235d940f7d804bbf60fb4f662b87c4?source=copy_link)