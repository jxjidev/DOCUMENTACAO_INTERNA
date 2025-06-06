# Arquitetura Frontend

A arquitetura de frontend é projetada para proporcionar uma interface interativa e modular aos usuários, suportando micro frontends e integrações com serviços backend.

1. **Autenticador - DevOps**: Similar ao backend, este componente gerencia a autenticação no frontend, garantindo acesso seguro.
2. **APIs**:
   * **API - DevOps**: Fornece serviços de integração relacionados às operações de DevOps.
   * **API - AI**: Serve como ponte entre o frontend e os serviços de inteligência artificial.
3. **Aplicações Web**:
   * **Web App - DevOps**: Uma aplicação específica para interações e gerenciamento de operações DevOps.
   * **Web App - AI**: Similar ao backend, fornece funcionalidades específicas para IA no frontend.
4. **Serviços e Microservices**: A arquitetura também suporta a comunicação com serviços baseados em IA, como **QAMetrik** e **Service Claude**, e integra-se diretamente com microservices.
5. **Microfrontend**: Um padrão utilizado para dividir o frontend em componentes menores e independentes, promovendo escalabilidade e manutenibilidade.
6. **Base UI Project - Orchestrator**: Um projeto principal que orquestra os micro frontends e garante consistência na interface do usuário.
