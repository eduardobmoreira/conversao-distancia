# conversao-distancia

Repositório no Docker Hub
https://hub.docker.com/repository/docker/eduardobmoreira/conversao-distancia/general

COMANDOS BÁSICOS

deletar todos os containers <br>
	docker container rm -f $(docker container ls -qa)

construir imagem<br>
	docker build -t conversao-distancia -f Dockerfile .
	
rodar um container<br>
	docker container run -d -p 8181:5000 conversao-distancia

construir imagem para o docker hub<br>
	docker build -t eduardobmoreira/conversao-distancia:v1 .
	
liimpar imagens que não tem referência<br>
	docker image prune

autenticar no docker hub<br>
	docker login

subir imagem no docker hub<br>
	docker push eduardobmoreira/conversao-distancia:v1

criar a tag latest<br>
	docker tag eduardobmoreira/conversao-distancia:v1 eduardobmoreira/conversao-distancia:latest

zerar o docker<br>
	docker system prune
