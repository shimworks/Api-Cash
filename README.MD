##### Projeto de API com docker em andamento

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

# para sair do bash
ctrl + C => ctrl + D
````



### Rotas
![POST](/Public/POST.png)
![GETALL](/Public/GETALL.png)
![GETONE](/Public/GETONE.png)
![PUT](/Public/PUT.png)
![DELETE](/Public/DELETE.png)