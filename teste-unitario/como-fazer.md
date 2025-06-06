# Como fazer

Para os clientes **Localiza**, **Pottencial** e **Fogás**, o **teste unitário está ativo no SAP**. Caso o **pacote termine com "SC"**,  o teste unitário não será realizado. Após isso, deve-se **executar a medição de cobertura** da **classe** e do **pacote**.

Caso há algum erro na demanda é importante **validar a classe** para verificar se há alguma situação específica, e somente depois validar o pacote.

Se ocorrer um erro como `Exception Error <CX_SY_DYN_CALL_ILLEGAL_METHOD>`, investigue a causa, pois pode estar relacionado a chamadas de métodos dinâmicas no teste.

Um exemplo de request é:

* **Request:** DEVK9A0SB7
* **Ambiente:** FABRICAQA
* **Objeto:** AB\_K\_12006\_Baixa de boleto no Banco do Brasil

<figure><img src="../.gitbook/assets/image (97).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (98).png" alt=""><figcaption></figcaption></figure>

Caso tenha algum erro similar a esse, solicitar um ajuste ao responsável da demanda.
