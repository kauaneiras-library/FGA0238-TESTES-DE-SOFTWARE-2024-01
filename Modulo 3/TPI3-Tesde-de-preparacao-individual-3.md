# Teste de Preparação Individual 3:

## Temas abordados:
**Grafo de Fluxo de Controle**, **Teste de Unidade**, **Cobertura de Condição e Decisão**, **Cobertura de Múltiplas Condições**, **MC/DC (Modified Condition/Decision Coverage)**, **Critérios de Cobertura Lógica**, **Teste Incremental e Não Incremental**, **Teste Top-Down e Bottom-Up**.

---

# Questões:

## Questão 1: Qual é a representação de programa mais comumente utilizada nos critérios de teste estrutural?

### Resposta certa:
- **Grafo de Fluxo de Controle.**

### Justificativa para as erradas:
- **a. Grafo de Causa-Efeito.**
  - Está errado porque o grafo de causa-efeito é mais utilizado em testes baseados em especificações e não em testes estruturais.
  
- **b. Grafo de Fluxo de Dados.**
  - Está errado porque o grafo de fluxo de dados é utilizado para testes baseados em análise de dados, e não é o mais comum em testes estruturais.
  
- **c. Grafo de Caminhos Independentes.**
  - Está errado porque esse grafo é utilizado para identificar caminhos únicos, mas não é a representação mais comumente utilizada em critérios de teste estrutural.

---

## Questão 2: Qual das seguintes afirmações é MAIS VERDADEIRA sobre o teste de unidade?

### Resposta certa:
- **É uma abordagem de teste de caixa branca que foca nos componentes individuais de um programa.**

### Justificativa para as erradas:
- **a. É uma abordagem de teste de caixa preta onde a estrutura interna do módulo não é considerada.**
  - Está errado porque o teste de unidade é caixa branca, já que analisa a estrutura interna do código.
  
- **c. Só é usado para grandes programas com mais de 500 instruções.**
  - Está errado porque o teste de unidade pode ser usado em programas de qualquer tamanho.
  
- **d. É o mesmo que teste de integração, que combina vários componentes.**
  - Está errado porque o teste de unidade foca em componentes individuais, enquanto o teste de integração combina múltiplos componentes.

---

## Questão 3: Quais são os dois principais motivos para realizar o teste de unidade?

### Resposta certa:
- **Reduzir a complexidade de testar programas grandes e facilitar a depuração.**

### Justificativa para as erradas:
- **a. Documentar a funcionalidade do programa e identificar erros no início do processo de desenvolvimento.**
  - Está errado porque o foco do teste de unidade é na depuração e redução de complexidade, e não na documentação.
  
- **c. Atender aos requisitos do usuário e garantir que o programa esteja livre de erros.**
  - Está errado porque o teste de unidade não visa atender diretamente aos requisitos do usuário, mas sim testar partes isoladas do código.
  
- **d. Melhorar a cobertura do código e testar o desempenho do programa.**
  - Está errado porque o teste de unidade foca em testar funcionalidade e não em otimização de desempenho.

---

## Questão 4: Por que a cobertura de condição pode não satisfazer a cobertura de decisão?

### Resposta certa:
- **Porque algumas condições podem mascarar outras.**

### Justificativa para as erradas:
- **a. Porque a cobertura de condição não testa todas as instruções.**
  - Está errado porque a cobertura de condição não está diretamente relacionada à execução de instruções, mas sim à verificação de combinações de condições.
  
- **c. Porque a cobertura de condição não inclui os pontos de entrada do programa.**
  - Está errado porque os pontos de entrada não são o foco da cobertura de condição.
  
- **d. Porque a cobertura de condição não testa todas as combinações de condições.**
  - Está errado porque essa afirmativa se refere à cobertura de múltiplas condições e não à cobertura de decisão.

---

## Questão 5: Qual é a principal limitação da cobertura de decisão?

### Resposta certa:
- **Não considera as múltiplas condições dentro de uma decisão.**

### Justificativa para as erradas:
- **a. Não garante que todas as instruções sejam executadas.**
  - Está errado porque o foco da cobertura de decisão é nas condições e não na execução de instruções.
  
- **c. Não testa todas as possíveis combinações de condições.**
  - Embora seja verdade, essa é a limitação da cobertura de múltiplas condições e não da cobertura de decisão.
  
- **d. Não identifica erros em decisões aninhadas.**
  - Está errado porque a cobertura de decisão pode identificar erros em decisões aninhadas, mas não lida bem com múltiplas condições.

---

## Questão 6: Qual dos critérios de cobertura de lógica é considerado o mais fraco?

### Resposta certa:
- **Cobertura de instrução.**

### Justificativa para as erradas:
- **a. Cobertura de condição.**
  - Está errado porque a cobertura de condição testa mais aspectos do código do que a cobertura de instrução.
  
- **b. Cobertura de decisão.**
  - Está errado porque a cobertura de decisão é mais robusta que a cobertura de instrução.
  
- **c. Cobertura de múltiplas condições.**
  - Está errado porque a cobertura de múltiplas condições é uma das mais fortes, testando várias combinações.

---

## Questão 7: O que o método MC/DC visa alcançar?

### Resposta certa:
- **Garantir que cada condição independente em uma decisão tenha um efeito independente na saída da decisão.**

### Justificativa para as erradas:
- **a. Testar todas as instruções do programa pelo menos uma vez.**
  - Está errado porque essa é a definição de cobertura de instrução.
  
- **b. Testar todas as combinações de decisões em um programa.**
  - Está errado porque isso se refere à cobertura de múltiplas condições, não ao MC/DC.
  
- **c. Garantir que cada condição em uma decisão tenha um resultado verdadeiro e falso pelo menos uma vez.**
  - Está errado porque isso não captura a essência do MC/DC, que foca na independência das condições.

---

## Questão 8: Qual é uma das principais vantagens do método MC/DC em relação a outros critérios de cobertura?

### Resposta certa:
- **Garante uma cobertura mais robusta ao testar condições de decisão.**

### Justificativa para as erradas:
- **a. Requer menos casos de teste para ser implementado.**
  - Está errado porque o MC/DC requer mais casos de teste do que critérios mais simples.
  
- **b. É mais fácil de entender e aplicar em programas grandes.**
  - Está errado porque o MC/DC pode ser mais complexo e difícil de aplicar.
  
- **d. Não requer testes de múltiplas condições dentro de uma decisão.**
  - Está errado porque o MC/DC testa várias combinações de condições, embora não todas as combinações possíveis.

---

## Questão 9: Qual das seguintes afirmações melhor descreve o primeiro passo ao usar técnicas de cobertura lógica no teste de software?

### Resposta certa:
- **Listar as decisões condicionais no programa, focando em declarações IF, DO e similares.**

### Justificativa para as erradas:
- **a. Identificar todas as variáveis no programa e garantir que cada uma seja testada em diferentes condições.**
  - Está errado porque o foco inicial da cobertura lógica está nas decisões, não nas variáveis.
  
- **c. Criar casos de teste para todas as funcionalidades do software sem considerar a estrutura interna do código.**
  - Está errado porque essa é uma abordagem de teste caixa-preta, não de cobertura lógica.
  
- **d. Garantir que todas as declarações IF no programa sejam testadas de forma isolada para verificar seu comportamento.**
  - Está errado porque o objetivo é testar todas as decisões condicionais, não apenas as instruções IF.

---

## Questão 10: Qual das seguintes afirmações melhor descreve uma característica do critério de cobertura de múltiplas condições?

### Resposta certa:
- **Mesmo testes que satisfazem o critério de cobertura de múltiplas condições podem não detectar certos erros, como valores iniciais incorretos.**

### Justificativa para as erradas:
- **a. O critério de cobertura de múltiplas condições é suficiente para detectar todos os erros possíveis em uma unidade.**
  - Está errado porque, mesmo cumprindo a cobertura de múltiplas condições, alguns erros podem passar despercebidos.
  
- **c. O critério de cobertura de múltiplas condições se concentra apenas em testes de caixa-preta.**
  - Está errado porque a cobertura de múltiplas condições é uma técnica de teste estrutural, que considera a lógica interna.
  
- **d. O critério de cobertura de múltiplas condições garante que todos os caminhos de execução do código sejam testados.**
  - Está errado porque a cobertura de múltiplas condições não garante a cobertura de todos os caminhos de execução.

---

## Questão 11: Qual é uma vantagem importante do teste incremental sobre o teste não incremental?

### Resposta certa:
- **Requer menos módulos de driver e stub.**

### Justificativa para as erradas:
- **b. Necessita de menos tempo de máquina.**
  - Está errado porque o teste incremental pode exigir mais tempo de máquina, dependendo da implementação.
  
- **c. Permite que todos os módulos sejam testados simultaneamente.**
  - Está errado porque o teste

 incremental testa módulos em sequência, não simultaneamente.
  
- **d. Reduz a possibilidade de detectar erros nas interfaces dos módulos.**
  - Está errado porque o teste incremental é justamente utilizado para detectar esses erros nas interfaces.

---

## Questão 12: Qual das seguintes observações é uma vantagem do teste não incremental?

### Resposta certa:
- **Permite mais atividades paralelas no início da fase de testes de módulo.**

### Justificativa para as erradas:
- **a. Detecta erros de interfaces de módulos mais cedo.**
  - Está errado porque o teste incremental é que permite a detecção precoce de erros de interface.
  
- **b. Reduz a necessidade de drivers e stubs.**
  - Está errado porque o teste não incremental exige drivers e stubs para a integração dos módulos.
  
- **d. Resulta em testes mais completos dos módulos.**
  - Está errado porque o teste não incremental não garante necessariamente uma maior completude dos testes.

---

## Questão 13: Qual é uma das principais vantagens do teste top-down?

### Resposta certa:
- **Facilita a representação de casos de teste uma vez que as funções de entrada e saída são adicionadas.**

### Justificativa para as erradas:
- **a. Não requer a criação de stubs.**
  - Está errado porque o teste top-down requer a criação de stubs para simular módulos inferiores.
  
- **c. Permite a identificação de todos os erros possíveis no programa.**
  - Está errado porque nenhum método de teste garante a identificação de todos os erros.
  
- **d. Garante que todos os módulos são testados simultaneamente.**
  - Está errado porque o teste top-down não testa todos os módulos ao mesmo tempo.

---

## Questão 14: Qual é uma desvantagem do teste bottom-up?

### Resposta certa:
- **Não permite a criação de um esqueleto inicial do programa.**

### Justificativa para as erradas:
- **a. A produção de módulos driver é mais difícil que a produção de stubs.**
  - Está errado porque a dificuldade da produção de drivers não é necessariamente maior que a de stubs.
  
- **c. Requer que todos os módulos sejam testados simultaneamente.**
  - Está errado porque o teste bottom-up não requer que todos os módulos sejam testados simultaneamente.
  
- **d. Aumenta a possibilidade de erros humanos durante a fase de design.**
  - Está errado porque a técnica de teste bottom-up não afeta diretamente o design, mas sim a sequência dos testes.