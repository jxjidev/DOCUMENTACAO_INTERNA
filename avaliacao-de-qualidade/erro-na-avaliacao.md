# Erro na avaliação

Quando é solicitado a geração de testes ou avaliação de qualidade no CARD da demanda, inicia o processo de comunicação com o SAP, realizando as seguintes análises.&#x20;

* Validação no SAP se a demanda existe;&#x20;
* Validação se existe objetos inativos na demanda;&#x20;
* Avaliação de qualidade do código de acordo com as regras de qualidade definida pelo cliente;&#x20;

Todos esses processos são executados de acordo com o evento acima, selecionando a classe na tabela: ZTBQAD0001.&#x20;

Caso retorne tudo com sucesso esse é o status que demonstra no CARD.&#x20;

<figure><img src="../.gitbook/assets/image (57).png" alt=""><figcaption></figcaption></figure>

Caso seja evidenciado algum erro, será exibido o seguinte status.

<figure><img src="../.gitbook/assets/image (59).png" alt=""><figcaption></figcaption></figure>

Clicando no ícone, será exibido em qual estágio foi reportado o erro.

<figure><img src="../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>

Para os casos que não retornam à avaliação de qualidade.

<figure><img src="../.gitbook/assets/image (62).png" alt=""><figcaption></figcaption></figure>

Podemos ter algumas situações para não ter o retorno.&#x20;

1. O usuário de comunicação entre os ambientes pode estar bloqueado ou solicitando troca de senha, nesse caso solicitar o desbloqueio ou eliminar essa validação de troca de senha para o usuário admin do cliente ao time do produto a informação do usuário consta no OneNote do produto  link: [QAMetrik - Operação](https://superotecnologia.sharepoint.com/:o:/s/qametrik/operacoes/EoLSLPwM9qtEvR7Uh6Dphe4B84x29lj0KSM72FsgfHxmvw?e=UDJjwT)&#x20;

&#x20;

Toda a avaliação de qualidade é gerada um job na SM37, para localizar ele pesquisar da seguinte forma:&#x20;

<figure><img src="../.gitbook/assets/image (63).png" alt=""><figcaption></figcaption></figure>

Ou pelo nome do programa: ZPQADR\_JOB\_QUALITY\_EVAL&#x20;

Caso o status seja sucesso, validar se tem uma lista no resultado.&#x20;

<figure><img src="../.gitbook/assets/image (64).png" alt=""><figcaption></figcaption></figure>

Clicando na lista.

<figure><img src="../.gitbook/assets/image (65).png" alt=""><figcaption></figcaption></figure>

Clicando no campo tipo, retornou que houve falha de comunicação, que no caso pode ser o usuário bloqueado.

<figure><img src="../.gitbook/assets/image (66).png" alt=""><figcaption></figcaption></figure>

Caso tenha sido avaliado que o usuário admin do Portal esteja ok, por validar se esse parâmetro PROXY\_SM59 esteja cadastrado na tabela ZTBSU\_002, caso não seja o ambiente da Taboca deve apagar o valor.

<figure><img src="../.gitbook/assets/image (67).png" alt=""><figcaption></figcaption></figure>

Se caso continuar erro, será necessário debugar o cenário pela transação zmonitorqa, nesses casos pode ter muitos objetos vinculados a request que acaba gerando lentidão no ambiente.

<figure><img src="../.gitbook/assets/image (68).png" alt=""><figcaption></figcaption></figure>

Caso avaliação no portal esteja diferente do envio do Json, solicitar que seja excluído avaliação anterior do Portal ao time de produto e seja refeito o envio.&#x20;

Tabela e configuração para o SAP consumir o usuário de comunicação.&#x20;

Tabela:ZTBSU\_002&#x20;

Parâmetro: QADEVOPS\_INITPARAM.&#x20;

<figure><img src="../.gitbook/assets/image (69).png" alt=""><figcaption></figcaption></figure>
