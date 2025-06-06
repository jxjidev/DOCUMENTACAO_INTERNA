# ZCLQAD\_TOKEN

Classe de geração do token RFC para conexão do Portal QaDevops com o cliente. Esta classe realiza a leitura do parâmetro QADEVOPS\_INITPARAM que está cadastrado na tabela ZTBSU\_002 e através dessas informações realiza a geração do token no Portal.

Para realizar o decode do cadastro utilizar o site [https://www.base64decode.org/](https://www.base64decode.org/).\
\
Caso não esteja gerando o token, validar se o usuário admin não está bloqueado, se estiver bloqueado solicitar o desbloqueio para o time do produto.
