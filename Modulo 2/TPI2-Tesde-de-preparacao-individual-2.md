# Teste de Preparação Individual 2: 

## Temas abordados:
**Teste Caixa-Preta**, **Classes de Equivalência**, **Particionamento de Equivalência**, **Análise de Valor Limite (Boundary Value Analysis)**, **Grafo de Causa-Efeito (Cause Effect-Graphing)**, **Error Guessing**, **Testes de Alto Nível (High Order Testing)**, **Teste Funcional (Function Test)**, **Teste de Compatibilidade**, **Teste de Performance**, **Métodos de Conclusão de Testes**. 

---

# Questões:

## Questão 1: Qual é o objetivo do teste caixa-preta?

### Resposta certa:
- **Identificar situações em que o programa não se comporta conforme as especificações.**

### Justificativa para as erradas:
- **a. Identificar o subconjunto mais efetivo de casos de teste dado uma funcionalidade específica.**
  - Está errado porque o teste caixa-preta não visa selecionar subconjuntos, mas sim verificar se o comportamento do software está de acordo com as especificações.
  
- **b. Detectar defeitos de entrada e saída de dados de forma sistemática.**
  - Está errado porque a caixa-preta não é focada apenas em entradas e saídas de dados, mas em verificar o cumprimento das especificações gerais.
  
- **c. Detectar falhas a partir da execução de todos os fluxos do programa.**
  - Está errado porque a caixa-preta não lida diretamente com fluxos internos do programa, mas sim com a saída em relação às entradas esperadas.

---

## Questão 2: Por que é importante atribuir um número único para cada classe de equivalência identificada?

### Resposta certa:
- **Para garantir a cobertura de todas as classes de equivalência ao elaborar os casos de teste.**

### Justificativa para as erradas:
- **b. Para assegurar que uma mesma classe não seja atendida por dois casos de teste.**
  - Está errado porque o foco não é evitar redundância, mas sim garantir a cobertura de todas as classes identificadas.
  
- **c. Para garantir que uma quantidade mínima de casos de teste seja elaborada.**
  - Está errado porque o número de casos de teste não é o ponto principal. A atribuição de números visa assegurar que todas as classes sejam cobertas.
  
- **d. Para assegurar que seja elaborado um caso de uso único para cada classe de equivalência.**
  - Está errado porque o objetivo não é criar casos de uso, mas garantir a cobertura das classes de equivalência nos testes.

---

## Questão 3: Aplicando o critério Particionamento de Equivalência (Equivalence Partitioning) para a condição de entrada de intervalo de valores "a quantidade de itens deve ser entre 1 e 100", quais classes de equivalência podem ser identificadas?

### Resposta certa:
- **3 classes: 1 <= quantidade <= 100; quantidade < 1; quantidade > 100**

### Justificativa para as erradas:
- **b. 4 classes: quantidade < 1; quantidade >=1; quantidade <= 100; quantidade > 100**
  - Está errado porque as classes de equivalência devem ser exclusivas e distintas. A classe `quantidade >= 1` é redundante com `1 <= quantidade <= 100`.
  
- **c. 2 classes: classe válida e classe inválida**
  - Está errado porque o particionamento de equivalência requer que as classes sejam mais específicas e detalhadas, não apenas uma classificação binária.
  
- **d. 2 classes: 1 <= quantidade <= 100; classe inválida**
  - Está errado porque essa abordagem não considera as classes distintas abaixo e acima do intervalo válido.

---

## Questão 4: O que é INCORRETO afirmar sobre o critério de Análise de Valor Limite (Boundary Value Analysis)?

### Resposta certa:
- **O particionamento de equivalência não deve ser utilizado em conjunto com a análise de valor limite.**

### Justificativa para as erradas:
- **a. Condições limites são as situações diretamente sobre, acima ou abaixo das bordas das classes de equivalência.**
  - Está certo porque essa é uma descrição correta do que são as condições limite.
  
- **c. Casos de teste são produzidos também para as classes de equivalência de saída.**
  - Está certo porque a análise de valor limite também é aplicada às saídas, além das entradas.
  
- **d. Os valores limites são utilizados para representar as classes de equivalência.**
  - Está certo porque os valores limite são usados para definir as bordas das classes de equivalência.

---

## Questão 5: Aplicando o critério Análise de Valor Limite para a condição de entrada de intervalo de valores "a quantidade de itens deve ser entre 1 e 100", quais casos de teste podem ser identificados?

### Resposta certa:
- **0; 1; 100; 101**

### Justificativa para as erradas:
- **b. 1; 2; 99; 100**
  - Está errado porque os valores limite incluem os valores diretamente fora do intervalo (0 e 101), e não apenas os limites internos.
  
- **c. -1; 0; 100; 101**
  - Está errado porque -1 não faz parte do intervalo relevante, enquanto o 1 deve ser incluído.
  
- **d. 1; 100**
  - Está errado porque essa abordagem ignora os valores imediatamente fora do intervalo (0 e 101), que são cruciais na análise de valor limite.

---

## Questão 6: É INCORRETO afirmar sobre o Grafo de Causa-Efeito (Cause Effect-Graphing):

### Resposta certa:
- **Efeitos são ligados às causas de acordo com a lógica implementada no código.**

### Justificativa para as erradas:
- **a. As causas e os efeitos são identificados a partir da especificação.**
  - Está certo porque a identificação de causas e efeitos realmente ocorre a partir das especificações.
  
- **b. As causas são as condições de entrada específicas ou classes de equivalência.**
  - Está certo porque as causas representam condições de entrada ou classes de equivalência no grafo de causa-efeito.
  
- **c. Os efeitos são as condições de saída ou transformações do sistema.**
  - Está certo porque os efeitos no grafo são os resultados ou condições de saída.

---

## Questão 7: Qual é a ideia por trás do critério de geração de casos de teste chamado de "Error Guessing"?

### Resposta certa:
- **Explora certos tipos prováveis de defeitos, de forma a produzir casos de teste para expor esses defeitos.**

### Justificativa para as erradas:
- **b. Propõe o uso da intuição e experiência do desenvolvedor para priorizar os casos de testes gerados por outros critérios.**
  - Está errado porque Error Guessing se baseia diretamente na experiência para gerar casos de teste, e não apenas para priorizá-los.
  
- **c. Faz uso de técnicas de Inteligência Artificial para determinar as áreas críticas do programa que precisam de mais casos de teste.**
  - Está errado porque Error Guessing não utiliza técnicas de IA, mas sim a intuição humana e o conhecimento prévio de erros comuns.
  
- **d. Utiliza a identificação de defeitos anteriores para prever novos defeitos e a partir disso gerar os casos de teste.**
  - Embora faça algum sentido, está errado porque Error Guessing se baseia mais em prever os tipos de erro mais prováveis, não em defeitos específicos identificados anteriormente.

---

## Questão 8: Qual a melhor definição para o propósito dos testes de alto nível (high order testing)?

### Resposta certa:
- **Identificar uma classe distinta de defeitos a partir de um tipo distinto de documentação.**

### Justificativa para as erradas:
- **a. Testar o sistema por completo, repetindo em alto nível os testes dos níveis mais baixos.**
  - Está errado porque testes de alto nível não se limitam a repetir testes anteriores. Eles visam detectar defeitos em uma perspectiva mais ampla.
  
- **b. Testar o sistema a partir da visão do usuário, de forma a encontrar defeitos de interface.**
  - Está errado porque, embora os testes de alto nível possam incluir a visão do usuário, o propósito principal é identificar defeitos específicos que não são detectados em níveis mais baixos.
  
- **d. Identificar defeitos em alto nível inseridos após os testes de níveis mais baixos.**
  - Está errado porque os testes de alto nível não focam apenas em defeitos "inseridos" depois, mas sim em uma classe diferente de defeitos.

---

## Questão 9: Qual é o propósito do teste funcional (function test)?

### Resposta certa:
- **Revelar falhas e expôr inconsistências com a especificação da funcionalidade.**

### Justificativa para as erradas:
- **a. Demonstrar que a funcionalidade está de acordo com a sua especificação.**
  - Está errado porque o teste funcional não busca "demonstrar" conformidade, mas sim identificar falhas.
  
- **b. Revelar inconsistências da cobertura lógica do programa realizada previamente por métodos caixa-branca.**
  - Está errado porque o teste funcional não se baseia em cobertura lógica ou métodos caixa-branca, mas sim em testar funcionalidades específicas contra a especificação.
  
- **c. Demonstrar que as funcionalidades foram integradas corretamente e não apresentam falhas.**
  - Está errado porque o teste funcional não se limita a integração de funcionalidades, mas foca em revelar falhas.

---

## Questão 10: Que tipo de teste implica em verificar o software em diferentes dispositivos e sistemas operacionais?

### Resposta certa:
- **Teste de compatibilidade**

### Justificativa para as erradas:
- **a. Teste de configuração**
  - Está errado porque o teste de configuração visa validar a instalação e configuração do software, não sua compatibilidade entre diferentes dispositivos.
  
- **c. Teste de instalação**
 

 - Está errado porque teste de instalação se refere à verificação de que o software pode ser corretamente instalado, não testado em diferentes ambientes.
  
- **d. Teste de confiabilidade**
  - Está errado porque teste de confiabilidade verifica a robustez do software em situações adversas, e não sua compatibilidade com dispositivos e sistemas operacionais diferentes.

---

## Questão 11: Para que serve o teste de performance?

### Resposta certa:
- **Determinar se o software atende aos requisitos de tempo de resposta e taxa de throughput.**

### Justificativa para as erradas:
- **a. Assegurar que o software é capaz de lidar com grandes volumes de acessos simultâneos.**
  - Está errado porque esse é um aspecto do teste de carga, e não especificamente de performance.
  
- **c. Verificar que o software atende as especificações de processamento de grandes volumes de dados.**
  - Está errado porque essa é uma descrição do teste de capacidade, não de performance.
  
- **d. Garantir que o software tenha desempenho equivalente em diversas versões de hardware.**
  - Está errado porque a equivalência de desempenho entre hardwares diferentes é o foco do teste de compatibilidade, e não de performance.

---

## Questão 12: Qual alternativa representa o melhor método para conclusão de testes?

### Resposta certa:
- **A combinação dos critérios acima.**

### Justificativa para as erradas:
- **a. Exame da curva de erros por unidade de tempo.**
  - Embora seja uma técnica útil, está errado porque a decisão de encerrar os testes não deve ser feita com base apenas em um critério.
  
- **b. Identificação de uma quantidade estimada de erros.**
  - Está errado porque o número de erros encontrados não é um critério suficiente para determinar a conclusão dos testes.
  
- **c. Execução de todos os testes derivados a partir de um ou mais métodos estabelecidos.**
  - Está errado porque, embora útil, a execução completa dos testes não garante que não há mais falhas. Combinar diferentes critérios é a abordagem ideal.
---