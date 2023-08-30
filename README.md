# Projeto de Biblioteca Pessoal

Bem-vindo ao projeto de Engenharia de Dados para Gestão de Biblioteca Pessoal. Este projeto visa demonstrar habilidades sólidas em Engenharia de Dados ao abordar algumas das fases mais importantes do ciclo de vida dos dados, desde a modelagem de um banco de dados, passando por um processo de ETL (extracao, transformacao e carregamento) até consultas e análises utilizando os dados armazenados.


## Fases do Projeto

### 1. Modelagem de Dados

Durante o desenvolvimento deste projeto, foram seguidas três fases essenciais de modelagem de dados:

##### Modelagem Conceitual
Na etapa de modelagem conceitual, inicialmente concentrei-me em identificar os principais elementos-chave do projeto: livros, autores, empréstimos e lista de desejos. Defini cada um desses componentes como "entidades" e determinei suas conexões e interações.

#### Modelagem Lógica
Com as entidades definidas, passei para a fase de modelagem lógica. Nesse ponto, detalhei a estrutura de cada entidade. Por exemplo, a entidade "book" foi enriquecida com atributos como título, ano de lancamento, número de páginas, genero, etc. As relações entre as entidades foram estabelecidas, com chaves primárias e estrangeiras definindo vínculos sólidos entre elas. Nesta etapa utilizei a ferramenta workbench para criar o diagrama.

#### Modelagem Física
A última etapa, a modelagem física, envolveu a implementação real do modelo no banco de dados atraves do MySQL. Aqui, traduzi as definições lógicas em comandos SQL concretos, exportando o diagrama criado na etapa anterior para gerar o scrip SQL. Cada tabela, como "Livro", "Autor", "Empréstimo" e "Lista de Desejos", foi criada com seus atributos específicos e as devidas restrições.


### 2. ETL (Extracao, Transfomacao e Carregamento)

Foram inseridos dados fictícios nas tabelas para simular a coleção de livros e autores de um determinado usuario. Isso preparou o banco para a próxima fase.

#### Extracao


#### Transformacao


#### Carregamento




### 4. Manipulação de Dados com Python

Usando notebooks Jupyter, os registros foram consultados, atualizados e manipulados com código Python. Isso destacou a interação prática com o banco de dados.

## Como Utilizar

1. Clone este repositório.
2. Execute os scripts SQL na pasta `database` para criar o banco e as tabelas.
3. Execute os notebooks Jupyter na pasta `notebooks` para explorar a manipulação de dados.

Este projeto oferece uma visão abrangente da engenharia de dados, do conceito à aplicação prática. Ideal para quem busca compreender a gestão de dados em projetos do mundo real.
