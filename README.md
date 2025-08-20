# Desafio AgroFuture: Modelo Preditivo de Transações de Vendedores

## 1. Resumo do Projeto
Este projeto foi desenvolvido como parte do desafio "AgroFuture: IA na Previsão de Negociações". O objetivo principal é construir um modelo de Machine Learning para prever quais vendedores (Seller ID) têm a maior probabilidade de realizar uma transação de commodity agrícola nos dias futuros de 04 e 05 de novembro de 2024.

Para alcançar este objetivo, o projeto segue um pipeline completo de Data Science, incluindo:

Análise exploratória de dois datasets (transações e mercado).

Enriquecimento de dados com fontes externas (cotação do Dólar).

Engenharia de features avançada, incluindo a criação de um "perfil comportamental" para cada vendedor com a API da OpenAI.

Tratamento de dados desbalanceados com a técnica SMOTE.

Treinamento, otimização e avaliação de um modelo de classificação (LGBMClassifier).

Geração de uma lista final ranqueada de vendedores para as datas solicitadas.

## 2. Tecnologias Utilizadas
O projeto foi desenvolvido inteiramente em Python 3, utilizando as seguintes bibliotecas e tecnologias:

**Ambiente e Análise:**

Python 3.11+: Linguagem principal do projeto.

Jupyter Notebook: Ambiente de análise interativa para exploração e modelagem.

Pandas: Biblioteca fundamental para manipulação e análise de dados tabulares.

NumPy: Biblioteca para operações numéricas eficientes.

**Visualização de Dados:**

Matplotlib & Seaborn: Utilizadas para criar gráficos e visualizações durante a análise exploratória.

**Machine Learning:**

Scikit-learn: Framework utilizado para pré-processamento, divisão de dados, avaliação de modelos (classification_report) e otimização de hiperparâmetros (RandomizedSearchCV).

LightGBM (LGBMClassifier): Modelo de Gradient Boosting de alta performance escolhido para a tarefa de classificação.

Imbalanced-learn (SMOTE): Biblioteca usada para tratar o desbalanceamento de classes, melhorando o aprendizado do modelo sobre eventos raros.

**Enriquecimento de Dados e IA:**

yfinance: Biblioteca para capturar dados históricos da cotação do Dólar (USD-BRL) do Yahoo Finance.

OpenAI API (GPT-4-Turbo): Utilizada para a criação de uma feature qualitativa, classificando o perfil de cada vendedor com base em seu comportamento histórico.

python-dotenv: Para gerenciamento seguro das chaves de API.

Tabulate: Dependência opcional do Pandas para formatação de tabelas em texto.



## 3. Estrutura de Arquivos
O projeto está organizado da seguinte forma:

desafio_grao/
├── .venv/                      
├── dados/
│   ├── mercado-desafio.xlsx
│   └── transacoes-desafio.xlsx
├── .env
├── analise_desafio.ipynb       
├── requirements.txt            
├── README.md                   
├── previsao_vendedores_2024-11-04.csv 
└── previsao_vendedores_2024-11-05.csv 

## 4. Passo a Passo para Iniciar o Projeto
Siga estas instruções para configurar o ambiente e executar o projeto.

**1. Pré-requisitos:**

Ter o Python 3.11 ou superior instalado.

Ter o Git instalado (opcional, para clonar).

**2. Configuração do Projeto:**

Clone ou baixe este repositório para sua máquina local.

Crie um arquivo chamado .env na pasta raiz (desafio_grao) e adicione sua chave da OpenAI:

`OPENAI_API_KEY="sk-..."`

**3. Criação do Ambiente Virtual:**

Abra um terminal na pasta raiz do projeto e crie um ambiente virtual:


`python -m venv .venv`

**4. Ativação do Ambiente:**

No Windows (CMD/PowerShell):

`.\.venv\Scripts\activate`

No macOS/Linux:

`source .venv/bin/activate`

Seu terminal deve agora mostrar (.venv) no início da linha.

## 5. Instalação das Dependências:

Crie um arquivo requirements.txt na pasta raiz com o seguinte conteúdo:

pandas
numpy
scikit-learn
matplotlib
seaborn
jupyter
openpyxl
yfinance
openai
python-dotenv
lightgbm
imbalanced-learn
tabulate


Instale todas as bibliotecas de uma vez com o seguinte comando:

`pip install -r requirements.txt`

## 6. Execução da Análise:

Com o ambiente ainda ativado, inicie o Jupyter Notebook:

`jupyter notebook`

No seu navegador, abra o arquivo analise_desafio.ipynb.

Para executar o projeto inteiro, vá ao menu e clique em `Kernel > Restart & Run All`. Isso garantirá que todas as células sejam executadas na ordem correta. Os arquivos .csv com as previsões finais serão salvos na pasta raiz.

## 7. Faça perguntas ao assistente!!

Assistente de conversa criado para responder perguntas ou requisições relacionadas ao contexto do projeto...
EX: "Qual a previsão dos vendedores do dia 04/11/2024?", "Mê dê informações sobre o projeto."