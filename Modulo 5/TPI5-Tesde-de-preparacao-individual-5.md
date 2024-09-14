# Teste de Preparação Individual 5:

## Temas abordados:
**Segurança no Ciclo de Vida de Desenvolvimento de Software (SDLC)**, **Mentalidade para Testes de Segurança**, **Vantagens de Acesso ao Código-Fonte em Revisões de Segurança**, **Desvantagens de Revisões Manuais**, **Modelagem de Ameaças**, **Desafios da Revisão de Código-Fonte**, **Limitações dos Testes de Penetração**, **Requisitos Funcionais e Negativos de Segurança**, **Casos de Uso e Abuso (Misuse Cases)**, **Testes de Segurança na Codificação**, **Triggers e Checkpoints em DevSecOps**, **Preocupações ao Introduzir Ferramentas como SAST**.

---

# Questões:

## Questão 1: Para minimizar efetivamente as vulnerabilidades de segurança em aplicações de software, que abordagem deve ser adotada de acordo com as melhores práticas no desenvolvimento de software?

### Resposta certa:
- **Incorporar medidas e testes de segurança consistentemente em cada fase do Ciclo de Vida de Desenvolvimento de Software (SDLC) para detectar e resolver problemas de forma preventiva.**

### Justificativa para as erradas:
- **a. Investir prioritariamente nos testes da fase final de implantação para identificar e corrigir falhas de segurança.**
  - Está errado porque a segurança deve ser integrada ao longo de todo o SDLC, não apenas na fase final.
  
- **b. Dispensar modelos formais do Ciclo de Vida de Desenvolvimento de Software (SDLC) para permitir avaliações de segurança com mais flexibilidade.**
  - Está errado porque os modelos formais garantem uma abordagem sistemática para a segurança.
  
- **c. Realizar revisões de segurança abrangentes após a finalização do desenvolvimento da aplicação, garantindo remoção efetiva das vulnerabilidades.**
  - Está errado porque a segurança deve ser tratada durante todo o processo de desenvolvimento, não apenas no final.

---

## Questão 2: Por que é importante desenvolver a mentalidade correta para testar a segurança de uma aplicação?

### Resposta certa:
- **Para pensar de forma criativa e como um atacante, identificando falhas que ocorrem fora dos casos de uso normais.**

### Justificativa para as erradas:
- **a. Para permitir o desenvolvimento e automação de teste dos casos de uso normais definidos pelos desenvolvedores.**
  - Está errado porque a mentalidade de segurança requer pensar além dos casos normais, como um atacante.
  
- **c. Para reduzir o tempo necessário para concluir os testes de segurança.**
  - Está errado porque o foco da mentalidade de segurança não é apenas acelerar o processo, mas garantir a identificação de vulnerabilidades.
  
- **d. Para garantir que todos os usuários compreendam os relatórios de segurança.**
  - Está errado porque a mentalidade de segurança não se concentra em tornar relatórios acessíveis aos usuários, mas sim em detectar falhas.

---

## Questão 3: Qual é a principal vantagem de ter acesso ao código-fonte durante uma revisão de segurança?

### Resposta certa:
- **Identificar vulnerabilidades específicas do código que não são detectáveis através de técnicas de teste de caixa-preta.**

### Justificativa para as erradas:
- **a. Possibilitar a análise de padrões de codificação para a otimização do desempenho da aplicação.**
  - Está errado porque o foco da revisão de segurança não é a otimização de desempenho, mas sim a identificação de vulnerabilidades.
  
- **b. Eliminar a necessidade de testes de penetração dinâmicos e externos.**
  - Está errado porque ter acesso ao código-fonte não elimina a necessidade de testes dinâmicos.
  
- **d. Minimizar a dependência de ferramentas automatizadas para a detecção de falhas de segurança.**
  - Está errado porque mesmo com acesso ao código, as ferramentas automatizadas continuam sendo importantes.

---

## Questão 4: Qual é uma desvantagem significativa das inspeções e revisões manuais no contexto de segurança de software?

### Resposta certa:
- **São flexíveis e aplicáveis a várias situações, porém podem ser lentas e exigem habilidades humanas avançadas.**

### Justificativa para as erradas:
- **a. Requerem o uso constante de ferramentas especializadas, o que pode limitar sua eficácia.**
  - Está errado porque revisões manuais não dependem necessariamente de ferramentas especializadas.
  
- **b. Fornecem resultados rápidos, mas não substituem a análise humana detalhada do código.**
  - Está errado porque revisões manuais são, na verdade, mais lentas, e o foco está na análise detalhada.
  
- **c. Podem ser demoradas, porém não dependem de materiais de suporte específicos para sua aplicação.**
  - Está errado porque essa resposta é vaga e não destaca a necessidade de habilidades avançadas.

---

## Questão 5: Qual abordagem recomendada para o desenvolvimento de um modelo de ameaças?

### Resposta certa:
- **Decompor a aplicação, definir e classificar os ativos, explorar vulnerabilidades e ameaças, e criar estratégias de mitigação.**

### Justificativa para as erradas:
- **a. Realizar uma análise automatizada dos ativos e ameaças do sistema, identificando classes de ataque.**
  - Está errado porque o processo recomendado inclui tanto a análise manual quanto a criação de estratégias de mitigação, e não apenas a análise automatizada.
  
- **c. Focar na identificação de vulnerabilidades técnicas da arquitetura, sem considerar ameaças externas.**
  - Está errado porque as ameaças externas também devem ser consideradas em um modelo de ameaças.
  
- **d. Desenvolver o modelo de ameaças após a conclusão do ciclo de vida de desenvolvimento de software, contemplando uma visão holística da aplicação.**
  - Está errado porque o modelo de ameaças deve ser desenvolvido durante o ciclo de vida do software, e não apenas no final.

---

## Questão 6: Qual é um desafio associado à revisão de código-fonte em comparação com outras técnicas de teste de segurança?

### Resposta certa:
- **Não consegue detectar erros que ocorrem em tempo de execução.**

### Justificativa para as erradas:
- **a. Pode identificar vários tipos de erros como falsos negativos.**
  - Está errado porque o desafio principal da revisão de código-fonte não é a produção de falsos negativos, mas sim a incapacidade de detectar problemas em tempo de execução.
  
- **c. Pode falhar em detectar vulnerabilidades relacionadas a padrões de código.**
  - Está errado porque a revisão de código pode identificar vulnerabilidades relacionadas a padrões de código.
  
- **d. Requer menos habilidade técnica do que outros métodos de análise de segurança.**
  - Está errado porque a revisão de código exige habilidades técnicas avançadas.

---

## Questão 7: Por que os testes de penetração não devem ser considerados a única técnica de teste em um programa de segurança?

### Resposta certa:
- **Porque identificam apenas uma amostra das vulnerabilidades possíveis e não garantem a cobertura completa de riscos.**

### Justificativa para as erradas:
- **a. Porque são sempre lentos e caros, não se justificando como a única técnica.**
  - Está errado porque nem todos os testes de penetração são necessariamente lentos e caros.
  
- **b. Porque são menos eficazes do que as ferramentas automatizadas disponíveis.**
  - Está errado porque os testes de penetração não são necessariamente menos eficazes, mas sim limitados em escopo.
  
- **c. Porque produzem elevadas taxas de falsos positivos nos relatórios gerados.**
  - Está errado porque os testes de penetração não são particularmente conhecidos por gerar altas taxas de falsos positivos.

---

## Questão 8: Qual dos seguintes exemplos é um requisito de segurança funcional para a autenticação?

### Resposta certa:
- **As senhas devem ser alfanuméricas, incluir caracteres especiais e ter no mínimo dez caracteres de comprimento.**

### Justificativa para as erradas:
- **a. A aplicação deve usar um algoritmo de encriptação definido pela organização.**
  - Está errado porque o uso de algoritmos de encriptação não é um requisito específico de autenticação.
  
- **c. Testes de segurança estáticos devem ser realizados a cada commit.**
  - Está errado porque essa não é uma prática de autenticação, mas uma prática de segurança de desenvolvimento.
  
- **d. Os erros de validação devem ser específicos e detalhados para facilitar a correção pelo usuário.**
  - Está errado porque mensagens de erro detalhadas podem expor informações de segurança e não são um requisito de autenticação.

---

## Questão 9: Qual dos seguintes requisitos de segurança é um exemplo de um requisito negativo?

### Resposta certa:
- **A aplicação deve garantir que os dados não sejam alterados ou destruídos sem autorização adequada.**

### Justificativa para as erradas:
- **a. A aplicação deve permitir que os usuários redefinam suas senhas a qualquer momento, sem validação adicional.**
  - Está errado porque isso seria uma falha de segurança, não um requisito negativo.
  
- **c. A aplicação deve exibir mensagens de erro detalhadas quando a validação de dados falhar.**
  - Está errado porque mensagens de erro detalhadas não são um requisito negativo.
  
- **d. A aplicação deve permitir que usuários acessem dados sem autenticação, se solicitado.**
  - Está errado porque isso comprometeria a segurança e não é um requisito negativo aceitável.

---

## Questão 10: Qual é o propósito principal dos casos de

 uso e abuso (misuse ou abuse cases) na derivação dos requisitos de segurança?

### Resposta certa:
- **Descrever a funcionalidade pretendida da aplicação e os cenários de uso malicioso e abusivo para identificar vulnerabilidades.**

### Justificativa para as erradas:
- **b. Avaliar o desempenho da aplicação em condições normais e anormais de uso para garantir que não haja falhas de segurança.**
  - Está errado porque o foco dos casos de uso e abuso não é avaliar desempenho, mas sim identificar vulnerabilidades.
  
- **c. Identificar e documentar os erros de código durante a fase de desenvolvimento para prevenir falhas de autenticação.**
  - Está errado porque o objetivo dos casos de uso e abuso é identificar ameaças de segurança, não apenas falhas de autenticação.
  
- **d. Criar um guia de usuário para fornecer instruções sobre como utilizar a aplicação de forma segura.**
  - Está errado porque os casos de uso e abuso não têm a ver com a criação de guias de usuário.