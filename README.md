# Análise de Vendas

Este projeto realiza a análise de vendas a partir de uma base de dados em Excel.

## Estrutura do Projeto

- `main.ipynb` contendo o código para carregar e analisar os dados de vendas.
- `vendas.xlsx` arquivo Excel contendo os dados de vendas.

## Requisitos

- Python 3.12.5
- Extensão Jupyter Notebook do VSCode
- Pandas

## Instalação

1. Clone o repositório:
    `git clone <URL_DO_REPOSITORIO>`

2. Navegue até o diretório do projeto:
    `cd <NOME_DO_DIRETORIO>`

3. Instale as dependências:
    `pip install pandas`

## Uso

1. Abra o arquivo `main.ipynb` para utilizar o Jupyter Notebook.
3. Execute as células para carregar e analisar os dados de vendas.

## Análise Realizada

O notebook `main.ipynb` realiza as seguintes análises:

1. Carrega os dados de vendas do arquivo [`vendas.xlsx`].
    ```python
    import pandas as pd
    tabela = pd.read_excel("vendas.xlsx")
    display(tabela)
    ```
2. Agrupa os dados por loja e produto, calculando o faturamento total por produto em cada loja.
    ```python
    faturamento_por_produto = tabela[["ID Loja", "Produto", "Valor Final"]].groupby(["ID Loja", "Produto"]).sum()
    display(faturamento_por_produto)
    ```
## Fonte

Este projeto foi realizado através do canal Hashtag. Link do vídeo: https://www.youtube.com/watch?v=kCMaqla6Grs&list=PLpdAy0tYrnKx9CtTmgSdzHz9YQ-C5ZNI9