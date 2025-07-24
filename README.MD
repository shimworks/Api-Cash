# Projeto de API SQL com docker 

## Antes de iniciar o repósitorio
### Pré requisitos
Crie um aruivo .env utilizando como base o .env-example
````
DOCKER_MYSQL_HOST=<ENDEREÇO DO BANCO>
API_PORT=<PORTA DE CONEXÃO DA API>
MYSQL_PORT=<PORTA DE CONEXÃO DO BANCO>
MYSQL_USER=<NOME DE USUÁRIO DO BANCO>
MYSQL_PASSWORD=<SENHA DE ACESSO DO BANCO>
MYSQL_ROOT_PASSWORD=<SENHA DE ACESSO DO BANCO DO USUÁRIO ROOT>
MYSQL_WAIT_FOR_CONNECTIONS=true
MYSQL_CONNECTION_LIMIT=10
MYSQL_QUEUE_LIMIT=0
````
##### Se estiver utilizando **root** em **MYSQL_USER**: As variáveis **MYSQL_PASSWORD** e **MYSQL_ROOT_PASSWORD** precisam ser iguais

#### Instalando o repositorio
````
npm install
````

#### Iniciando a API e o Banco de Dados
````
npm run du
````

## Outros comandos úteis
#### Desliga o docker e todos seus serviços
````
npm run dd
````
#### Visualiza logs do container
````
docker container logs cash_api
````
````
docker container logs <DOCKER_MYSQL_HOST>
````

#### Acessa o bash do container
````
docker exec -it cash_api bash
````
````
docker exec -it <DOCKER_MYSQL_HOST> bash
````
Para sair do bash
ctrl + C => ctrl + D



## Rotas

POST - Adiciona uma pessoa ao banco de dados
```
localhost:3001/people
```
```
{
  "firstName": "Lukes",
  "lastName": "Skywalker",
  "email": "lukes.skywalker@email.com",
  "phone": "851 678 4453"
}
```
![POST](/Public/POST.png)

GET - Mostra todos as pessoas do banco de dados
```
localhost:3001/people
```
![GETALL](/Public/GETALL.png)

GET - Mostra uma pessoa do banco de dados
```
localhost:3001/people/1
```
![GETONE](/Public/GETONE.png)

PUT - Atualiza uma pessoa do banco de dados
```
localhost:3001/people/1
```
```
{
  "firstName": "Darth",
  "lastName": "Vader",
  "email": "the_father@email.com",
  "phone": "851 678 4453"
}
```
![PUT](/Public/PUT.png)

DELETE - Remove uma pessoa do Banco de Dados
```
localhost:3001/people/1
```
![DELETE](/Public/DELETE.png)