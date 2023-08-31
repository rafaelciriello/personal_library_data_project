# Projeto de Biblioteca Pessoal

Bem-vindo ao projeto de Engenharia de Dados para Gestão de Biblioteca Pessoal. Este projeto visa demonstrar habilidades sólidas em Engenharia de Dados ao abordar algumas das fases mais importantes do ciclo de vida dos dados, desde a modelagem de um banco de dados, passando por um processo de ETL (extracao, transformacao e carregamento) até consultas e análises utilizando os dados armazenados.


## Fases do Projeto

### 1. Modelagem de Dados

Durante o desenvolvimento deste projeto, foram seguidas três fases essenciais de modelagem de dados:


##### Modelagem Conceitual

Na etapa de modelagem conceitual, inicialmente concentrei-me em identificar os principais elementos-chave do projeto: "book", "author", "loan" e "washlist". Defini cada um desses componentes como "entidades" e determinei suas conexões e interações.


#### Modelagem Lógica

Com as entidades definidas, passei para a fase de modelagem lógica. Nesse ponto, detalhei a estrutura de cada entidade. Por exemplo, a entidade "book" foi enriquecida com atributos como título, ano de lancamento, número de páginas, genero, etc. As relações entre as entidades foram estabelecidas, com chaves primárias e estrangeiras definindo vínculos entre elas. Nesta etapa utilizei a ferramenta workbench para criar o diagrama e poder visualizar a estrutura montanda.


#### Modelagem Física

A última etapa, a modelagem física, envolveu a implementação real do modelo no banco de dados atraves do MySQL. Aqui, traduzi as definições lógicas em comandos SQL concretos, exportando o diagrama criado na etapa anterior para gerar o scrip em SQL. Cada tabela, como "book", "author", "loan" e "washlist", foi criada com seus atributos específicos e as devidas restrições.


### 2. ETL (Extracao, Transfomacao e Carregamento)

A fonte de dados para este projeto consite em tres arquivos no formato cvs, armazenados localmente em nossa maquina. O primeiro deles denominado books possui informacoes sobre os livros e seus respectivos autores, dele vamos extrair informacoes para alimentar duas de nossas tabelas no banco de dados a tabela book e a tabela author. O segundo aquivo denominado loans contem uma lista das pessoas que pegaram livros emprestados e suas data de retirada e devolucao caso ja tenha ocorrido. E o terceiro arquivo chamado wishlist contem uma lista de livros que desejamos adquirir no futuro, com informacoes sobre autor e data de lancamento.

Todas os tres arquivos precisaram passar por uma fase de limpeza e transformacao, considerando que existem dados invalidos, desnecessarios e em formatos diversos dos que precisaremos para alimentar nosso banco de dados modelado anteriormente.


#### Extracao

Nesta etapa, realizei a extracao dos dados utilizando Python atraves do Jupyter Notebook, nos serviu como fontes de dados tres arquivos no formato csv, books_authors.csv (contendo informacoes a respeito dos livros e de seus respectivos autores presentes na biblioteca), loans.csv (com ifnormacoes sobre emprestimos realizados) e o arquivo wishlist.csv (contendo uma relacao de titulos para futuras aquisicoes).


#### Transformacao

Atraves do Pandas, uma biblioteca muito utilizada em Python, realizei a etapa de tranformacao e limpeza nos dados. 

No arquivo books.csv, retiramos tres titulos de livros que apareciam de forma duplicada na nossa fonte de dados. Devido a divergencia de formatos de datas, tratamos o campo de birthday do autor para que apresentase apenas o ano de nascimento, atingindo desta forma uma padronizacao nas informacoes. Alem disso, foi necessario separar as informacoes desse arquivo em dois DataFrame que foram utilizados para alimentar duas de nossas tabelas no banco de dados, a tabela book e a tabela author.

No arquivo loans.csv, realizamos o tratamento no campo data de devolucao em relacao ao emprestimo realizado a nossa amiga Ana, considerando que no nosso exemplo ela ja teria devolvido o livro e eu me esqueci de anotar a data, desta forma, o tratamento foi realizado para preenchimento do campo com a data atual.

No arquivo wishlist.csv podemos observar que em 2 registros conta apenas o ano de lancamento do livro e um comentario breve que nao nos permite identificar qual livro se trata. Desta forma realizei a exclusao destes dois registros.


#### Carregamento

Nesta etapa ainda utilizando Jupyter Notebook, Python e sua biblioteca "XXXXXXX" realize a conexao no Banco de Dados, e utilizando os dados tratados na etapa anterior alimentei o banco de dados com estas informacoes.


### 4. Manipulação de Dados com Python

Usando notebooks Jupyter, os registros foram consultados, atualizados e manipulados com código Python. Isso destacou a interação prática com o banco de dados.

## Como Utilizar

1. Clone este repositório.
2. Execute os scripts SQL na pasta `database` para criar o banco e as tabelas.
3. Execute os notebooks Jupyter na pasta `notebooks` para explorar a manipulação de dados.

Este projeto oferece uma visão abrangente da engenharia de dados, do conceito à aplicação prática. Ideal para quem busca compreender a gestão de dados em projetos do mundo real.
