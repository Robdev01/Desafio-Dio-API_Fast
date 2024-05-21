# Desafio-Dio-API_Fast
Projeto: WorkoutAPI
Esta é uma API de competição de crossfit chamada WorkoutAPI, unificando duas paixões: codar e treinar. É um projeto hands-on e simplificado, desenvolvido para ensinar o uso do FastAPI.

Modelagem de Entidade e Relacionamento (MER)
A API foi modelada com um MER simplificado para facilitar o aprendizado.

Stack da API
A API foi desenvolvida utilizando:

FastAPI (async)
Alembic
SQLAlchemy
Pydantic
Postgres (utilizando Docker)
Execução da API
Para executar o projeto, utilizei a pyenv com a versão 3.11.4 do Python para o ambiente virtual.

Passos para execução:
Configurar o ambiente virtual:

sh
Copy code
pyenv virtualenv 3.11.4 workoutapi
pyenv activate workoutapi
pip install -r requirements.txt
Subir o banco de dados:
Caso não tenha o docker-compose instalado, faça a instalação e logo em seguida, execute:

sh
Copy code
make run-docker
Criar uma nova migration:

sh
Copy code
make create-migrations d="nome_da_migration"
Criar o banco de dados:

sh
Copy code
make run-migrations
Executar a API
Para subir a API, execute:

sh
Copy code
make run
Acesse: http://127.0.0.1:8000/docs

Desafio Final
Adicionar query parameters nos endpoints:

Atleta:
nome
cpf
Customizar response de retorno de endpoints:

Get all:
atleta
nome
centro_treinamento
categoria
Manipular exceção de integridade dos dados em cada módulo/tabela:

sqlalchemy.exc.IntegrityError
Mensagem: “Já existe um atleta cadastrado com o cpf: x”
status_code: 303
Adicionar paginação utilizando a lib: fastapi-pagination

limit e offset
Referências
FastAPI
Pydantic
SQLAlchemy
Alembic
Fastapi-pagination
