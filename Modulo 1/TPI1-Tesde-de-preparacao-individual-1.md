# Teste de Preparação Individual 1

## Temas abordados:
**Definição de Testes de Software**, **Estratégias de Teste Caixa-Preta e Caixa-Branca**, **Princípio da Probabilidade de Defeitos**, **Property-Based Testing**, **Teste Sistemático**, **Ser Sistemático no Teste de Software**, **Distinção entre Design e Execução de Casos de Teste**, **Importância de Múltiplas Técnicas de Teste**, **Pirâmide de Testes**, **Vantagem dos Testes Unitários**, **Teste de Sistema**.

---

# Questões

## Questão 1: Qual é a melhor definição para a atividade de testes de software?

### Resposta certa:
- **Teste é o processo de executar um programa com a intenção de encontrar falhas.**

### Justificativa para as erradas:
- **b. Teste é o processo de demonstrar que falhas não estão presentes em um programa.**
  - Está errado porque o objetivo dos testes é encontrar falhas, não provar sua ausência. A ausência de falhas pode ser inferida com base em testes bem-sucedidos, mas não é o propósito principal.
  
- **c. O propósito do teste é mostrar que um programa executa as suas funcionalidades de forma correta.**
  - Está errado porque o teste visa descobrir erros ou falhas e não apenas validar o funcionamento correto do programa. Encontrar problemas é o foco principal.
  
- **d. Teste é o processo de estabelecer confiança que o programa faz o que deveria fazer.**
  - Está errado porque o objetivo primário do teste é encontrar falhas e não criar confiança. A confiança pode ser um subproduto do processo de teste bem conduzido, mas não é o propósito.

---

## Questão 2: Escolha a alternativa que melhor descreve as estratégias de teste caixa-preta e caixa-branca.

### Resposta certa:
- **Na estratégia caixa-preta os testes são derivados das especificações de requisitos, enquanto que na estratégia caixa-branca os testes são derivados da lógica de programação.**

### Justificativa para as erradas:
- **b. Na estratégia caixa-preta os testes são derivados da lógica de programação, enquanto que na estratégia caixa-branca os testes são derivados da especificação de requisitos.**
  - Está errado porque inverte os conceitos de caixa-preta e caixa-branca. Testes caixa-preta são baseados em requisitos, não na lógica de programação.
  
- **c. Na estratégia caixa-preta não é permitido analisar a estrutura interna do programa, enquanto na estratégia caixa-branca a especificação não é utilizada.**
  - Está errado porque, embora a estrutura interna não seja analisada na caixa-preta, a caixa-branca utiliza a lógica interna, mas sem deixar de usar a especificação.
  
- **d. Na estratégia caixa-preta os testes são derivados dos dados de entrada, enquanto que na estratégia caixa-branca os testes são derivados dos algoritmos utilizados.**
  - Está errado porque, na caixa-preta, os testes são baseados em especificações, e não apenas em dados de entrada. A caixa-branca, de fato, se baseia nos algoritmos, mas a definição é imprecisa.

---

## Questão 3: É correto afirmar sobre o princípio da probabilidade de que a existência de mais defeitos em uma seção de código é proporcional ao número de defeitos já encontrados naquela seção:

### Resposta certa:
- **Indica que defeitos tendem a vir em clusters e que, em um programa típico, algumas seções parecem ser muito mais propensas a defeitos do que outras seções.**

### Justificativa para as erradas:
- **a. Não faz sentido, pois os defeitos tendem a ter uma distribuição uniforme em todas as seções de código.**
  - Está errado porque, na prática, defeitos não são distribuídos uniformemente. Eles costumam se concentrar em áreas específicas do código.
  
- **b. Se foram identificados muitos defeitos em uma seção de código, o princípio indica que mais esforço deve ser investido em outras seções de código.**
  - Está errado porque, de acordo com o princípio, é provável que onde muitos defeitos já foram encontrados, outros ainda existam. O foco deve continuar nessas seções problemáticas.
  
- **d. É um fenômeno útil porque nos dá uma visão ou feedback no processo de teste, indicando as seções de código mais propensas a defeitos.**
  - Embora isso faça sentido, essa resposta não se refere diretamente ao princípio de clustering de defeitos, que é a explicação correta.

---

## Questão 4: Por que Eleanor usou a técnica property-based testing para testar o método que retorna os extremos?

### Resposta certa:
- **Porque a entrada era uma lista e a ordem dos elementos poderia afetar o algoritmo.**

### Justificativa para as erradas:
- **a. Porque ela precisava testar o comportamento inválido do método.**
  - Está errado porque a técnica property-based testing pode testar diversos cenários, não apenas comportamentos inválidos.
  
- **b. Porque é a única técnica que ela conhece.**
  - Está errado porque a justificativa da escolha da técnica se baseia nas características da entrada, e não na limitação de conhecimento da Eleanor.
  
- **c. Porque ela queria gerar casos de teste extra para analisar o comportamento do algoritmo.**
  - Está errado porque a técnica não foi escolhida apenas para gerar mais testes, mas sim para lidar com a natureza da entrada (listas, cuja ordem poderia alterar o resultado).

---

## Questão 5: Qual das opções abaixo melhor justifica a aplicação de teste sistemático, mesmo que aumente o esforço de desenvolvimento?

### Resposta certa:
- **Os custos de prevenção são mais baixos que os custos para corrigir defeitos no ambiente de produção.**

### Justificativa para as erradas:
- **a. A aplicação das técnicas de teste dá mais segurança para a equipe implantar novas releases em produção.**
  - Embora seja um benefício real dos testes sistemáticos, esta justificativa não aborda diretamente a relação entre prevenção e os custos de correção de defeitos, que é o ponto central.
  
- **b. Os clientes estão dispostos a arcar com os custos da aplicação do teste sistemático.**
  - Está errado porque a justificativa adequada deve se basear nos benefícios técnicos e econômicos, e não na disposição dos clientes de pagar por isso.
  
- **c. O teste sistemático reduz a dívida técnica e assegura melhoria contínua da qualidade do produto.**
  - Embora isso seja verdadeiro, a resposta correta foca nos custos diretos de prevenção versus correção, o que é uma justificativa mais concreta e objetiva.

---

## Questão 6: O que significa ser sistemático no teste de software?

### Resposta certa:
- **Que dois desenvolvedores deveriam chegar ao mesmo conjunto de casos de teste para o mesmo pedaço de código.**

### Justificativa para as erradas:
- **a. Que dois desenvolvedores deveriam seguir as mesmas etapas de testes para chegar aos mesmos resultados.**
  - Está errado porque a sistematicidade não se refere a seguir os mesmos passos, mas a obter os mesmos resultados de teste.
  
- **b. Que os desenvolvedores deveriam seguir as mesmas etapas de testes para chegar aos mesmos resultados.**
  - Está errado porque ser sistemático significa que o processo é reproduzível, não que as etapas precisam ser idênticas.
  
- **c. Que os desenvolvedores deveriam usar mais a criatividade para escrever as suites de teste.**
  - Está errado porque ser sistemático não envolve criatividade, mas sim seguir um processo organizado e repetível para alcançar os mesmos resultados.

---

## Questão 7: Qual afirmação melhor representa a distinção entre as atividades de design de casos de teste e execução de casos de teste?

### Resposta certa:
- **O design de casos de teste é uma atividade mais desafiadora que a escrita do código de execução dos testes.**

### Justificativa para as erradas:
- **a. O design de casos de teste exige o envolvimento de analistas de QA, enquanto a automação da execução é realizada pelos desenvolvedores.**
  - Está errado porque o envolvimento de analistas de QA não é o ponto central da distinção entre design e execução de testes.
  
- **b. Os casos de testes precisam ser corretamente definidos na atividade de design para que os desenvolvedores possam automatizá-los.**
  - Está errado porque, embora a definição de testes seja importante, isso não é a principal distinção entre design e execução.
  
- **d. A escrita de casos de teste é uma atividade maçante e evitada por grande parte dos desenvolvedores, que preferem a escrita de código de execução em frameworks como JUnit.**
  - Está errado porque isso não reflete a complexidade do design de testes em comparação à execução. A resposta correta aborda a diferença de desafios entre as duas atividades.

---

## Questão 8: Por que é necessário aplicar várias técnicas de teste para se ter um teste efetivo?

### Resposta certa:
- **Para revelar tipos diferentes de defeitos.**

### Justificativa para as erradas:
- **a. Para que todos na equipe possam contribuir com o design dos casos de teste.**
  - Está errado porque o objetivo principal não é a contribuição da equipe, mas sim a detecção de diferentes tipos de defeitos.
  
- **c. Para diminuir os custos com a automação de teste.**
  - Está errado porque a aplicação de várias técnicas de teste pode, na verdade, aumentar os custos. O foco é na eficácia para encontrar defeitos.
  
- **d. Para pode focar apenas no teste unitário e melhorar a efetividade dos testes.**
  - Está errado porque a aplicação de múltiplas técnicas visa cobrir diferentes áreas e defeitos, não focar exclusivamente em testes unitários.

---

## Questão 9: Qual alternativa melhor descreve a pirâmide de testes?

### Resposta certa:
- **É uma organização dos níveis de teste no formato de uma pirâmide. Na base está o nível menos complexo (unitário) realizado em maior volume. No topo está o nível mais complexo, realizado em menor quantidade.**

### Justificativa para as erradas:
-

 **a. A pirâmide representa quanto esforço é gasto em cada nível de teste. A base da pirâmide (testes automatizados) indica o nível em que a equipe dedicará mais tempo, enquanto o topo representa o teste menos realizado (manual).**
  - Está errado porque o esforço gasto não é o ponto central da pirâmide de testes. A pirâmide reflete a quantidade e a complexidade dos testes em diferentes níveis.
  
- **c. Uma hierarquia de níveis de teste no formato de uma pirâmide, em que os testes mais complexos e numerosos estão na base, enquanto os menos complexos e mais rápidos de serem executados estão no topo.**
  - Está errado porque a base da pirâmide tem testes menos complexos (unitários) e não mais complexos. Testes mais rápidos e em maior número estão na base.
  
- **d. É uma estratégia que permite planejar quantos testes serão executados em cada nível. É um modelo proposto em oposição ao modelo troféu (trophy), que privilegia os testes unitários.**
  - Está errado porque a pirâmide de testes não se opõe diretamente ao modelo troféu, e o foco da pirâmide é na hierarquia de complexidade e volume de testes, não no planejamento da quantidade de testes.

---

## Questão 10: Qual das alternativas abaixo pode ser vista como uma vantagem do teste unitário?

### Resposta certa:
- **Os testes unitários são fáceis de escrever.**

### Justificativa para as erradas:
- **a. Os testes unitários são capazes de revelar mais tipos de defeitos em comparação aos outros níveis de teste.**
  - Está errado porque testes unitários geralmente cobrem apenas defeitos em funções isoladas, enquanto outros tipos de testes podem revelar defeitos mais amplos.
  
- **b. Os testes unitários não requerem que os desenvolvedores conheçam os frameworks de teste.**
  - Está errado porque os desenvolvedores precisam, sim, conhecer frameworks de teste para escrever testes unitários eficazes.
  
- **c. Os testes unitários em geral representam a execução real do software.**
  - Está errado porque testes unitários geralmente testam partes isoladas do código e não representam a execução completa ou realista de um software.

---

## Questão 11: Qual das alternativas abaixo pode ser vista como uma vantagem do teste de sistema?

### Resposta certa:
- **É mais realístico que os outros níveis de teste.**

### Justificativa para as erradas:
- **b. É menos suscetível a comportamentos erráticos (flakiness).**
  - Está errado porque testes de sistema podem, sim, ser suscetíveis a comportamentos erráticos devido à sua complexidade.
  
- **c. É mais fácil de escrever o teste, pois não leva em consideração o código.**
  - Está errado porque testes de sistema não são necessariamente mais fáceis de escrever. A complexidade envolvida no ambiente torna esses testes desafiadores.
  
- **d. A sua execução é mais rápida que os outros tipos de teste.**
  - Está errado porque testes de sistema tendem a ser mais demorados, já que testam o sistema como um todo e não apenas partes isoladas.

---