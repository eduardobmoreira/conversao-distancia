# conversao-distancia

deletar todos os containers:
	docker container rm -f $(docker container ls -qa)

construir imagem
	docker build -t conversao-distancia -f Dockerfile .
	
rodar um container
	docker container run -d -p 8181:5000 conversao-distancia

construir imagem para o docker hub
	docker build -t eduardobmoreira/conversao-distancia:v1 .
	
liimpar imagens que não tem referência
	docker image prune

autenticar no docker hub
	docker login

subir imagem no docker hub
	docker push eduardobmoreira/conversao-distancia:v1

criar a tag latest
	docker tag eduardobmoreira/conversao-distancia:v1 eduardobmoreira/conversao-distancia:latest

zerar o docker
	docker system prune
