# Comandos Docker

## Visualizar containers criados e ativos

sudo docker ps -a

<figure><img src="../.gitbook/assets/supero3.jpg" alt=""><figcaption></figcaption></figure>

## Visualizar logs do container

sudo docker logs -f dev-qacodai

<figure><img src="../.gitbook/assets/supero4.jpg" alt=""><figcaption></figcaption></figure>

## Remover Imagem Docker que será feita a atualização

sudo docker rmi cadalu2025/qacodai-api:latest

sudo docker rmi cadalu2025/qapayments-api:latest

sudo docker rmi cadalu2025/qacodai-ui:latest

## Baixar Imagen Docker que será atualizada

sudo docker pull cadalu2025/qacodai-api:latest

sudo docker pull cadalu2025/qapayments-api:latest

sudo docker pull cadalu2025/qacodai-ui:latest

## Cria Containers e roda as imagens com as configurações do Container Portal-Web

sudo docker run -d --name dev-qacodai --restart unless-stopped --network host -p 8052:44357 cadalu2025/qacodai-api:latest

sudo docker run -d --name dev-qapayments-api --restart unless-stopped --network -p 8055:44355 host cadalu2025/qapayments-api:latest

sudo docker run -d --name dev-qacodai-ui -p 4200:80 --restart unless-stopped cadalu2025/qacodai-ui:latest
