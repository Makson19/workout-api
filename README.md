# Workout API

Este projeto faz parte do [3º Desafio do Bootcamp Luizalabs na DIO](https://www.dio.me/bootcamp/luizalabs-back-end-com-python) e se trata de uma API de competição de crossfit desenvolvida utilizando o FastAPI.

## Modelagem de entidade e relacionamento - MER

<img src='./mer.jpg' alt='Modelo de entidade e relacionamento da API'>

## Stack da API

A API foi desenvolvida utilizando o `fastapi`, junto das seguintes libs: `alembic`, `SQLAlchemy` e `pydantic`. Para salvar os dados está sendo utilizado o `postgres`, por meio do `docker`.

## Execução da API

Para executar essa API é necessário ter o `poetry` e o `docker-compose` instalados em sua máquina.

Para instalar as dependências do projeto, execute:

~~~python
poetry install
~~~

Para ativar o ambiente virtual, realize o passo a passo abaixo:

1. Com o projeto aberto no VSCode, abra o terminal e execute o comando `poetry env info`.
2. Em `Virtualenv`, copie o valor da chave `PATH`.
3. Digite `ctrl + shift + P` para abrir a paleta de comandos do VSCode.
4. Procure pela opção `Select interpreter` (para facilitar a busca basta digitar o nome da opção) e clique nela.
5. Ao selecionar a opção `Select interpreter`, clique na opção `Enter interpreter path...` e cole o valor de `PATH` (etapa 2). Em seguida, tecle `Enter`.
6. Abra um novo terminal no VSCode.

Para subir o banco de dados, caso não tenha o `docker-compose` instalado, faça a instalação e logo em seguida, execute:

~~~python
make run-docker
~~~

Para criar uma nova migration, execute:
~~~python
make create-migrations d="nome_da_migration"
~~~

Para criar o banco de dados, execute:
~~~python
make run-migrations
~~~

Para subir a API, execute:

~~~python
make run
~~~

e acesse: [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)
