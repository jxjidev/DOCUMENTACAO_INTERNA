# Arquitetura Backend

A arquitetura de backend é composta por diversos componentes integrados para suportar serviços de inteligência artificial (IA) e operações de DevOps.

1. **Autenticador - DevOps**: É responsável por gerenciar a autenticação e autorização dos serviços, fornecendo segurança e controle de acesso.
2. **Web App - AI**: Um ponto central para interações no backend, conectando-se ao controlador da API para processamento adicional.
3. **API Controller - AI**: Atende como intermediário principal para direcionar solicitações entre o front-end e os serviços de backend.
4. **Microservices**: Conjunto de serviços menores e independentes que fornecem funcionalidades específicas.
5. **Serviços de IA**: Dois serviços principais são destacados:
   * **AI - QAMetrik**: Provavelmente focado em métricas de qualidade automatizadas utilizando IA.
   * **Service Claude - AI**: Um serviço adicional de IA que complementa as funcionalidades do sistema.
6. **Databases**: Dois bancos de dados, um específico para operações de DevOps e outro para dados relacionados à IA.

<br>
