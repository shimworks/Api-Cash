##### Projeto de API com docker

#### Antes de iniciar o repósitorio
## Pré requisitos
Crie um aruivo .env utilizando como base o .env-example

### Instalando o repositorio
````
npm install
````

### Iniciando o repositorio
````
docker-compose up -d
````

### Outros comandos úteis
# Desliga o docker e todos seus serviços
````
docker-compose down
````
# Visualiza logs do container
````
docker container logs cash_api
docker container logs database
````
# Acessa o bash do container
````
docker exec -it cash_api bash
docker exec -it database bash

# Para sair do bash
ctrl + C => ctrl + D
````



### Rotas
```
localhost:3001/people
```
![POST](/Public/POST.png)
```
localhost:3001/people
```
![GETALL](/Public/GETALL.png)
```
localhost:3001/people/1
```
![GETONE](/Public/GETONE.png)
```
localhost:3001/people/1
```
![PUT](/Public/PUT.png)
```
localhost:3001/people/1
```
![DELETE](/Public/DELETE.png)