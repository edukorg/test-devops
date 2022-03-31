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
RUN npm install  -> comando para instalar todas as dependências da aplicação
ENTRYPOINT npm start  ->

## Deploy da aplicação em Minikube




## Infrastructure as Code



