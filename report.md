# Test Report



## Pré-requisitos

1. Minikube


## Criação de Dockerfile e imagem Docker
- Primeiramente testei a aplicação localmente utilizando o VScode com os comandos "npm install" para as dependências contidas no arquivo package.jason serem instaladas. Com o comando "npm start", a aplicação foi inicializada na porta 3000, default da própria aplicação.
Abri o navegador e com o comando "localhost:3000" verifiquei a seguinte imagem.
![localhost3000](https://user-images.githubusercontent.com/85547913/161094199-dad79235-b481-4ed4-881c-ba31ebf30a18.jpg)

- Com sucesso do teste local, comecei a criação do arquivo Dockerfile  e utilizei os seguintes comandos:

FROM node:16  -> para o Docker buscar no Docker Hub a imagem do Node na versão 16
WORKDIR /app-node  -> definição do diretório padrão.
COPY . .   -> com o 1º ponto, será copiado os arquivos do host para dentra imagem, sendo o 2º ponto.
RUN npm install  -> instalar todas as dependências da aplicação
ENTRYPOINT npm start  -> start da aplicação

- Com o comando "docker build -t rafaelsonego/app-node:1.0" criei a imagem e utilizando o comando "docker run -d -p 8080:3000 rafaelsonego/app-node:1.0" executei o container para testar a aplicação, redirecionando a porta 8080(host) para a porta 3000(app) e por assim, testando com o comando "localhost:8080" como imagem abaixo.
![docker_run](https://user-images.githubusercontent.com/85547913/161100023-ed5de4de-94da-4b76-8d81-bfb232c5b66c.jpg)
![localhost8080](https://user-images.githubusercontent.com/85547913/161100198-b99f9ce1-b4a2-4f3c-843f-e4a2e1d550db.jpg)

## Deploy da aplicação em Minikube




## Infrastructure as Code



