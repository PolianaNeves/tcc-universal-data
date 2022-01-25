# **PUC Minas - Pós Graduação Inteligência Artificial**
## **Trabalho de Conclusão de Curso - Poliana Neves**
### Universal Studios Reviews - *Analysis*


---



* #### **Onde posso encontrar os dados originais?**

O dataset foi obtido através do Kaggle, [neste link](https://www.kaggle.com/dwiknrd/reviewuniversalstudio), porém o dataset obtido ao início da análise, pode ser encontrado na pasta de scripts do projeto.


* #### **Qual a proposta do trabalho?**

A proposta deste trabalho é entregar valor aos gestores dos parques temáticos da Universal Studios. Isso está sendo realizado através da análise de dados das reviews obtidas do TripAdvisor, plataforma de qual os dados foram extraídos, conforme informações do Kaggle.


* #### **Qual a licença para os dados contidos no dataset?**

Conforme verificado no Kaggle, os dados estão sob a licença CC0. Veja mais informações sobre este tipo de licença [aqui](https://creativecommons.org/publicdomain/zero/1.0/).

* #### **Qual é a estrutura do dataset?**

O dataset é composto de 6 colunas e mais de 50mil avaliações de visitantes. As colunas presentes no dataset são: `reviewer`, `rating`, `written_date`, `title`, `review_text` e `branch`.


* #### **Lógica de execução dos scripts python**

Os scripts contidos dentro da pasta de scripts, são executados individualmente, e devem seguir a ordem de execução abaixo para funcionar.
Os nomes possuem números que indicam a ordem de execução de cada arquivo, apenas para facilitar o entendimento, não seguindo nenhum dos padrões `python` ou `pep8`.

* 1_treatments -> Neste script, é realizada a limpeza, tratativa e separação dos datasets
* 2_intermediary_treatments -> Como será explicado nos scripts, por questões de estratégia, as reviews do dataset foram separadas em positivas e negativas. Este script trata então da predição de sentimentos (positivos ou negativos) das avaliações.
* 3_dataset_union -> Para ser usado nas demais funcionalidades, o script gera um dataset com todas as reviews
* 4_wordcloud_and_frequency -> O script gera um dataset com os termos e suas frequências, além de duas imagens, contendo a nuvem de palavras (positiva e negativa). Estas informações são usadas no dashboard.
* 5_time_series_analysis -> Criação de várias funções para análise de gráficos e obtenção de informações gerenciais. Este script também é usado na api, para geração dos gráficos no dashboard.

* #### **Como executar os arquivos?**

Os arquivos podem ser executados normalmente através de qualquer interpretador python.
Para criá-los, usei o Google Colab, porém é possível utilizar também outros meios, como por exemplo, VS Code ou Anaconda.

* #### **Porque gerar datasets quebrados?**

Dado ao que queria executar com o projeto, utilizei da estratégia de quebrar o fluxo em pequenos datasets que possam ser consumidos a qualquer momento.
Isso me fez ganhar em tempo de execução, já que o BERT, por exemplo, demora em torno de 3 horas a ser executado (usando o Colab Pro, com configuração para TCU e RAM Alta).
Outro ponto também, é que o dashboard terá todos os dados pré-carregados, fazendo uma leitura fácil e rápida dos dados.
