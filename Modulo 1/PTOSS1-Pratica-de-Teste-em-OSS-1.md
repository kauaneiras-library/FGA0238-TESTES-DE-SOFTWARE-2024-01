# Prática de Teste em OSS 1 – Estratégia de Testes

## Enunciado

Esta atividade consiste em identificar e reportar a estratégia de testes utilizada pelo projeto OSS selecionado pela equipe.

### Atividades:

1. Cada membro da equipe deve fazer um fork do projeto e configurar o ambiente de desenvolvimento. Dúvidas e problemas de configuração devem ser postados no fórum do respectivo projeto no GitHub para que os monitores possam dar apoio.

2. Analisar a documentação, as issues e o código do projeto no GitHub e identificar todos os aspectos relacionados a teste. Seguir o template fornecido para levantar as informações mínimas a respeito da estratégia de testes adotada no projeto.

3. Com base nas informações levantadas e nos conteúdos estudados neste módulo, avaliar a estratégia adotada pelo projeto e recomendar possíveis melhorias para a realização de testes no projeto.

### Entregável:

1. Produzir um relatório em equipe com os itens da estratégia de testes identificados do projeto e a análise da estratégia adotada, com possíveis recomendações.

---

## Resolução

### 1. Identificação dos Tipos e Níveis de Teste

- **Tipos de Teste**: O projeto **Cobblemon** apresenta principalmente **testes unitários**. Não foram identificados testes de integração ou de sistema no código.
- **Níveis de Teste**: O nível de teste unitário é o mais predominante. Em conformidade com a **Pirâmide de Testes**, onde deve haver mais testes de baixo nível, como testes unitários, o projeto parece estar seguindo essa prática, mas não possui testes de mais alto nível.

### 2. Automação de Testes

- O projeto utiliza automação de testes com bibliotecas como **JUnit**, **Mockito**, **MockK**, e **ClassGraph** para testes unitários.
- Não foi possível determinar se outros tipos de testes (como integração ou sistema) estão automatizados.

### 3. Ciclo de Vida das Tarefas

- As issues são criadas para descrever problemas ou tarefas, muitas vezes com templates, que incluem informações como título, descrição, passos para reprodução e comportamento esperado.
- O ciclo de vida de uma issue pode incluir:
  - Reprodutibilidade do bug.
  - Processo de depuração e análise de logs.
  - Correção do bug e verificação.
  
- O ciclo pode variar dependendo do tipo de issue, mas nem todas as issues têm uma comunicação formal clara ou atribuições explícitas.

### 4. Papéis e Responsabilidades

- **Líder de Testes**: Define a estratégia de testes, monitora o progresso e comunica-se com as partes interessadas.
- **Testadores**: Executam testes manuais e automatizados, documentando bugs encontrados.
- **Especialista em Automação de Testes**: Cria e mantém scripts de testes automatizados.
- **Especialista em Testes Não Funcionais**: Realiza testes de desempenho, segurança e usabilidade.

### 5. Ferramentas de Teste

As principais bibliotecas de teste utilizadas são:
- **JUnit**: Framework de teste unitário para Java.
- **Mockito/MockK**: Frameworks de simulação para testes unitários em Java e Kotlin.
- **ClassGraph**: Usado para escanear o classpath durante os testes.

### 6. Métricas de Teste

- Não foram encontradas informações diretas sobre a coleta de métricas de teste, como cobertura de código. Para obter métricas, ferramentas como **JaCoCo** poderiam ser utilizadas.

### 7. Necessidades de Testes

- O projeto não indica explicitamente classes ou componentes que precisem de maior cobertura de testes.

### 8. Análise da Estratégia de Testes

Com base nas informações levantadas:
- O projeto foca principalmente em **testes unitários**, mas carece de testes de integração e não funcionais (como segurança ou desempenho).
- A falta de ferramentas de cobertura de testes é um ponto a ser abordado.
- A documentação relacionada a testes pode ser aprimorada para facilitar o entendimento de novos contribuidores.

### 9. Recomendações

1. **Cobertura de Testes**: Implementar uma ferramenta de cobertura de testes como **JaCoCo** para garantir que todos os aspectos do código estejam sendo testados adequadamente.
2. **Testes Não Funcionais**: Incluir testes de segurança e desempenho, utilizando ferramentas como **OWASP ZAP** e **JMeter**.
3. **Documentação de Testes**: Melhorar a documentação da estratégia de testes para facilitar a compreensão dos contribuidores.
4. **Automação**: Expandir a automação para incluir testes de integração e sistema.
5. **Integração Contínua (CI)**: Implementar um pipeline de integração contínua para automatizar a execução dos testes.