# Funcionamento

Comunicação ocorre entre SAP e Portal via:

RFC (Remote Function Call) → chamada direta de funções no SAP a partir do portal.

SAP CPI (Cloud Platform Integration) → middleware para orquestrar integrações.

Integração é acionada e bate diretamente em uma função/método ABAP.



2. Componentes Técnicos Classes e Funções

Função ZFQAD\_INTEGRA\_DEVOPS

Classe ZCLQAD\_CREATE\_DEMAND

Método sfqad\_action\_integration\_execute

Classe ZCLQAD\_SEND\_MSG\_PORTAL

Método m\_send

Classe ZCLQAD\_INTEGRATE\_REQUEST

Método m\_execute\_case

Configurações

Atualização de tabelas (telas de manutenção de parâmetros)

Configuração de endpoint (API, porta, usuário admin do cliente)

Decode Base64 → usado para processar arquivos recebidos/codificados.



3. Fluxo de Autenticação e Dependências

Usuário admin é fundamental:

Responsável por gerar o token de autenticação.

Sem token → portal para completamente (sem avaliação de qualidade, transporte, cópia, risco, movimentação de cards).

Teste rápido:

Pode ser feito via Postman → se não retornar token, significa que o portal está parado.

Ponto crítico:

Se algum parâmetro na tabela for alterado incorretamente (ex: trocar 1 letra), o portal quebra.

Bloqueio de admin:

Ocorre raramente, em média a cada 6 meses.

Acontece por excesso de tentativas de acesso consecutivas sem espaçamento de tempo.



4. Boas Práticas

Sempre validar parâmetros críticos (tabela de integração e parâmetro principal do portal).

Monitorar a saúde do usuário admin e token.

Utilizar ferramentas de documentação (GitBook interno, Tiflux) para centralizar informações de fluxo.

Fluxos devem ser organizados de forma simples e direta, permitindo rápida identificação de falhas.



📌 Resumo Macro do Processo

Evento ocorre no Portal.

Integração aciona função no SAP (via RFC ou CPI).

SAP executa métodos ABAP específicos (m\_send, m\_execute\_case, etc.).

Dados podem ser armazenados em tabelas ou processados (incluindo decode Base64).

Autenticação depende do usuário admin, que gera token.

Se token falhar → todo o portal fica indisponível.
