# Módulo 3: Testes de Caixa Branca e Testes Unitários

### Introdução

Neste módulo, aprendemos a realizar **testes de caixa branca** e abordamos o conceito de **cobertura de código**, além de técnicas para maximizar a qualidade e a eficácia dos testes com menos esforço, utilizando estratégias como o **MC/DC** (Modified Condition/Decision Coverage). Esses testes são fundamentais para garantir que o software funcione corretamente, tanto em termos de lógica quanto de estrutura interna.

### Teste de Caixa Branca (White-Box Testing)

Os **testes de caixa branca** focam em verificar o funcionamento interno do código. O testador tem acesso ao código-fonte e analisa como cada parte do código funciona, garantindo que todas as instruções, caminhos e condições sejam testados corretamente. Isso ajuda a encontrar bugs mais sutis que poderiam ser ignorados em um teste de caixa preta, já que o desenvolvedor pode visualizar o comportamento exato do código.

#### Principais Técnicas de Caixa Branca

1. **Cobertura de Comandos**
   - **O que é?**: Garante que cada linha de código (comando) seja executada pelo menos uma vez.
   - **Problema**: Nem sempre garante que todas as condições lógicas do programa sejam testadas. Por exemplo, pode executar o código, mas sem verificar todas as ramificações que dependem de diferentes condições.

2. **Cobertura de Decisões**
   - **O que é?**: Garante que cada decisão (como instruções `if`, `switch`, etc.) seja testada para ambos os resultados (verdadeiro e falso).
   - **Problema**: Ainda pode deixar passar erros em subcondições dentro de uma decisão. Por exemplo, testar apenas o resultado final de uma decisão sem verificar todas as combinações de suas condições internas.

3. **Cobertura de Condições**
   - **O que é?**: Foca em testar cada subcondição dentro de uma decisão para garantir que todas as variações de verdadeiro e falso sejam cobertas.
   - **Problema**: Pode não cobrir completamente todas as combinações possíveis entre as condições, deixando a possibilidade de falhas não descobertas em situações mais complexas.

4. **Cobertura de Condições/Decisões**
   - **O que é?**: Garante que todas as condições dentro de uma decisão sejam testadas, assim como a própria decisão, verificando todos os resultados possíveis.
   - **Problema**: Condições complexas dentro de uma decisão podem mascarar outras, dificultando a detecção de erros específicos.

5. **Cobertura de Caminhos Básicos**
   - **O que é?**: Baseia-se na escolha de um caminho básico no código (geralmente o caminho "feliz", ou seja, sem erros) e na variação de suas decisões para cobrir diferentes caminhos no código.
   - **Problema**: Pode ser insuficiente em programas com alta complexidade, onde várias decisões e condições interagem de maneiras mais complicadas.

---

### Teste Unitário (Unit Testing)

Os **testes unitários** são fundamentais para testar unidades pequenas e isoladas de um código, como funções ou métodos, garantindo que cada uma delas funcione de maneira correta. Esses testes são especialmente úteis no desenvolvimento ágil, onde as mudanças no código são frequentes e precisam ser testadas rapidamente.

- **Objetivo**: Validar se uma unidade de código (como um método ou função) funciona corretamente. Um teste unitário deve ser rápido de executar e fácil de automatizar.
- **Exemplo**: Suponha que você tenha uma função que soma dois números. Um teste unitário garantiria que, ao passar dois valores conhecidos (por exemplo, 2 e 3), o resultado seja sempre 5.

Os testes unitários são a primeira linha de defesa contra bugs e garantem que pequenas partes do código funcionem como esperado antes de serem integradas a outras partes maiores.

---

### Cobertura MC/DC (Modified Condition/Decision Coverage)

O **MC/DC** é uma técnica avançada de cobertura de testes, usada principalmente em sistemas críticos, como software aeronáutico ou médico, onde a precisão é essencial. Essa técnica garante que, mesmo com um número reduzido de testes, você possa cobrir as combinações mais importantes de condições e decisões.

#### Como Funciona o MC/DC?

1. **Cada ponto de entrada e saída** no código deve ser invocado.
2. **Cada decisão** no código deve ser testada para ambos os resultados (verdadeiro e falso).
3. **Cada condição em uma decisão** deve ser testada de forma que afete o resultado final da decisão de maneira independente.

Com isso, o MC/DC permite que você reduza o número de testes necessários sem perder a qualidade da cobertura.

#### Exemplo Simples de MC/DC

Se você tem uma condição com três variáveis, como `A && B || C`, o número de testes necessários seria 8 (2^3) para cobrir todas as combinações possíveis. No entanto, com o MC/DC, você pode reduzir esse número para apenas 4 testes, já que o objetivo é garantir que cada variável seja testada de forma independente.

#### Fórmula para Calcular Testes no MC/DC

O número de testes no MC/DC é sempre igual ao número de condições + 1. Portanto, para uma expressão com 3 condições, você teria 3 + 1 = 4 testes no total.

---

### Aplicação do MC/DC em Sistemas Complexos

A técnica de **MC/DC** é especialmente útil em **sistemas complexos**, onde o número de condições e decisões pode ser muito alto. Usar o MC/DC reduz significativamente o número de testes, mantendo uma cobertura alta, o que é essencial em sistemas onde a segurança e a precisão são fundamentais.

- **Exemplo Prático**: Em um software de controle de voo, onde existem muitas condições e variáveis a serem verificadas, o MC/DC garante que o código seja testado adequadamente, sem a necessidade de criar centenas de testes.

---

### Teste de Caixa Cinza (Gray-Box Testing)

O **teste de caixa cinza** combina o conhecimento do código interno (caixa branca) com a funcionalidade externa (caixa preta). É uma abordagem híbrida, onde o testador tem algum conhecimento sobre a lógica interna do código, mas também foca em como o sistema se comporta do ponto de vista do usuário.

---

### Conclusão

No **Módulo 3**, aprendemos sobre **testes de caixa branca**, que analisam a estrutura interna do código e garantem uma cobertura completa. Também abordamos o conceito de **testes unitários**, essenciais para testar pequenas unidades de código de forma isolada. Por fim, a técnica **MC/DC** foi destacada como uma maneira eficiente de testar sistemas complexos, reduzindo o número de testes necessários sem perder a qualidade. É fundamental que os desenvolvedores apliquem essas técnicas para garantir a confiabilidade e a segurança do software, principalmente em sistemas críticos.