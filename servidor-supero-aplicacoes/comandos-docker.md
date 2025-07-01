# Comandos Docker

## Visualizar containers criados e ativos

sudo docker ps -a

<figure><img src="../.gitbook/assets/supero3.jpg" alt=""><figcaption></figcaption></figure>

## Visualizar logs do container

sudo docker logs -f dev-qacodai

<figure><img src="../.gitbook/assets/supero4.jpg" alt=""><figcaption></figcaption></figure>

## Parar Container Docker que será feita a atualização

sudo docker stop dev-qacodai-api

sudo docker stop dev-qapayments-api

sudo docker stop dev-qacodai-ui

## Remover Container Docker que será feita a atualização

sudo docker rm dev-qacodai-api

sudo docker rm dev-qapayments-api

sudo docker rm dev-qacodai-ui

## Baixar Imagen Docker que será atualizada

sudo docker pull cadalu2025/qacodai-api:latest

sudo docker pull cadalu2025/qapayments-api:latest

sudo docker pull cadalu2025/qacodai-ui:latest

## Cria Containers e roda as imagens com as configurações do Container Portal-Web

sudo docker run -d --name dev-qacodai --restart unless-stopped --network rede-local -p 8052:44357 cadalu2025/qacodai-api:latest

sudo docker run -d --name dev-qapayments-api --restart unless-stopped --network rede-local -p 8055:44355 cadalu2025/qapayments-api:latest

sudo docker run -d --name dev-qacodai-ui -p 4200:80 --restart unless-stopped cadalu2025/qacodai-ui:latest
