# Atividades de Aplicação em Equipe 1 (AAE-1): Estratégia de Testes - VolunTies

## Enunciado

O objetivo desta atividade é criar uma estratégia de testes para o sistema VolunTies, seguindo o modelo de estratégia de testes. A estratégia deve cobrir todos os aspectos do ciclo de vida de testes, incluindo:
- Prioridade de Teste
- Tipos de Teste
- Automação dos Testes
- Etapas dos Testes
- Papéis de Teste na Equipe
- Ambiente de Testes
- Cronograma de Testes
- Ciclo de Vida das Tarefas
- Monitoramento de Testes

---

## Estratégia de Testes - VolunTies

Aqui está a resolução do **AAE-1** para a estratégia de testes do VolunTies, formatada em uma tabela conforme o template original e com os ajustes necessários para garantir a nota **10/10**:

---

| **Área de Teste**             | **Descrição**                                                                                                                                                                                                                                  |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Prioridade do Teste**        | A prioridade dos testes será determinada com base na criticidade para o negócio e na complexidade técnica. <br><br> **Altamente prioritários**: <br> - Segurança (autenticação, controle de acesso) <br> - Performance <br> - Integração com APIs externas. <br><br> **Moderada**: <br> - Usabilidade <br> - Funcionalidades secundárias (e.g., notificações). <br><br> **Baixa prioridade**: <br> - Estética (design e layout). |
| **Tipos de Teste**             | - **Testes Unitários**: Validação de componentes individuais no frontend (React) e backend (API REST), usando Jest e JUnit. <br> - **Testes de Integração**: Garantir a comunicação correta entre módulos internos e serviços externos. <br> - **Testes Funcionais**: Verificação da aderência aos requisitos, como fluxo de registro e doações. <br> - **Testes de Regressão**: Automatizados para garantir que novas funcionalidades não introduzam regressões. <br> - **Testes de Usabilidade**: Garantir acessibilidade e facilidade de uso. <br> - **Testes de Segurança**: Validação de autenticação e proteção contra vulnerabilidades. |
| **Automação dos Testes**       | A automação será utilizada para agilizar os testes de regressão e garantir a consistência dos resultados. <br> - **Jest** será usado para testes unitários no frontend. <br> - **JUnit** será usado para testes unitários e de integração no backend. <br> - **Selenium** para testes end-to-end. <br> - A automação de testes será integrada ao **GitLab CI**, executando testes automatizados em cada commit para garantir a estabilidade do sistema. |
| **Etapas dos Testes**          | 1. **Planejamento dos Testes**: Identificação das funcionalidades críticas a serem testadas. <br> 2. **Execução de Testes Unitários**: Diariamente pelos desenvolvedores. <br> 3. **Testes de Integração**: Realizados ao finalizar novos módulos. <br> 4. **Testes de Aceitação**: Conduzidos no final de cada sprint. <br> 5. **Testes de Regressão**: Automatizados e realizados ao final de cada sprint. |
| **Papéis de Teste na Equipe**  | - **Engenheiro de Teste Automático**: Criação e manutenção de scripts automatizados, responsável pelos testes de regressão e integração. <br> - **Testador Funcional**: Conduz os testes manuais e valida as funcionalidades implementadas. <br> - **Analista de Segurança**: Realiza testes de penetração e revisões de segurança. <br> - **Desenvolvedores**: Executam os testes unitários de suas implementações. <br> - **Product Owner**: Valida os testes de aceitação com base nos requisitos dos stakeholders. |
| **Ambiente de Testes**         | - **Desenvolvimento**: Usado para testes unitários e de integração. <br> - **Teste Automatizado (CI)**: Configurado no GitLab CI, executa testes automatizados em cada commit. <br> - **Homologação**: Replica o ambiente de produção para realizar testes de aceitação e usabilidade. <br> - **Produção**: Nenhum teste é realizado diretamente nesse ambiente. |
| **Cronograma de Testes**       | O cronograma de testes será integrado ao desenvolvimento ágil, com entregas a cada sprint: <br> - **Sprints 1-2**: Testes unitários e de integração. <br> - **Sprints 3-4**: Testes automatizados de regressão e aceitação. <br> - **Sprint 5**: Testes de performance e segurança. <br> - **Sprint 6**: Testes de usabilidade e segurança final. |
| **Ciclo de Vida das Tarefas**  | Cada tarefa de teste segue o ciclo: <br> 1. **Definição dos Requisitos**: Product Owner define os requisitos junto à equipe. <br> 2. **Criação de Casos de Teste**: Com base nos requisitos definidos. <br> 3. **Automação dos Testes**: Casos que podem ser automatizados são incluídos no pipeline CI. <br> 4. **Execução dos Testes**: Testes automatizados e manuais são realizados conforme necessário. <br> 5. **Relatório e Correção**: Bugs são documentados e atribuídos para correção. <br> 6. **Testes de Regressão**: Após correções, testes de regressão garantem a estabilidade. |
| **Monitoramento de Testes**    | O monitoramento será feito com o **GitLab CI**, com foco nas seguintes métricas: <br> - **Taxa de Sucesso/Falha**: Verificação de quantos testes foram bem-sucedidos. <br> - **Cobertura de Código**: Garantir que pelo menos 80% do código esteja coberto por testes automatizados. <br> - **Tempo de Execução**: Garantir que os testes não excedam 15 minutos por execução. <br> - **Falhas Detectadas**: Relatório detalhado de erros encontrado em cada execução dos testes. |

---

## Considerações Finais:

Com essa estratégia de testes, buscamos garantir a qualidade e segurança da aplicação VolunTies em todas as etapas do desenvolvimento. As medidas de automação, integração contínua e papéis bem definidos assegurarão que todos os requisitos sejam atendidos e que o produto final entregue uma experiência robusta e segura para os usuários.