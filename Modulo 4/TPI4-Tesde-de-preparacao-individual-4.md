# Teste de Preparação Individual 4:

## Temas abordados:
**Objetos Dummy, Fake, Stubs e Mocks**, **Injeção de Dublês de Teste**, **Lançamento de Exceções com Dublês**, **Vantagens e Desvantagens de Dublês de Teste**, **Desenvolvimento Orientado a Testes (TDD)**, **Impacto do TDD no Design de Software**, **Benefícios e Limitações do TDD**.

---

# Questões:

## Questão 1: O que são objetos dummy?

### Resposta certa:
- **Objetos passados para a classe em teste, mas nunca utilizados.**

### Justificativa para as erradas:
- **a. Objetos que possuem implementações reais, mas simplificadas.**
  - Está errado porque objetos dummy não possuem implementação real, eles são apenas placeholders que não são utilizados.
  
- **c. Objetos que fornecem respostas codificadas para chamadas realizadas durante o teste.**
  - Está errado porque essa é uma característica de **stubs**, não de objetos dummy.
  
- **d. Objetos que gravam todas as interações e permitem fazer asserções posteriormente.**
  - Está errado porque essa é uma característica de **mocks**, e não de objetos dummy.

---

## Questão 2: Qual a principal característica de objetos fake?

### Resposta certa:
- **Eles têm implementações reais, mas geralmente fazem a tarefa de forma mais simples.**

### Justificativa para as erradas:
- **b. Eles fornecem respostas codificadas para chamadas realizadas durante o teste.**
  - Está errado porque fornecer respostas codificadas é característica dos **stubs**.
  
- **c. Eles gravam todas as interações e permitem fazer asserções posteriormente.**
  - Está errado porque essa é uma característica de **mocks**.
  
- **d. Eles envolvem o objeto real e observam seu comportamento.**
  - Está errado porque **fakes** têm implementação simplificada, e essa definição está mais associada a **mocks** ou **spies**.

---

## Questão 3: Como os stubs diferem dos objetos fake?

### Resposta certa:
- **Stubs fornecem respostas codificadas e não têm uma implementação funcional.**

### Justificativa para as erradas:
- **a. Stubs têm implementações reais, mas simplificadas.**
  - Está errado porque stubs não têm implementação funcional real.
  
- **b. Stubs são usados apenas para observar o comportamento de uma dependência real.**
  - Está errado porque essa função é característica dos **mocks**, não dos stubs.
  
- **d. Stubs permitem fazer asserções sobre as interações após o teste.**
  - Está errado porque **mocks**, e não stubs, são usados para fazer asserções.

---

## Questão 4: Qual a vantagem principal dos objetos mocks em comparação com os stubs?

### Resposta certa:
- **Mocks podem gravar interações e permitir asserções sobre elas.**

### Justificativa para as erradas:
- **a. Mocks têm implementações reais.**
  - Está errado porque mocks não possuem implementação real, eles simulam comportamento.
  
- **b. Mocks são mais fáceis de controlar do que stubs.**
  - Está errado porque ambos são controláveis, mas o ponto principal é a capacidade de mocks fazerem asserções.
  
- **d. Mocks fornecem respostas codificadas para chamadas realizadas durante o teste.**
  - Está errado porque fornecer respostas codificadas é função de **stubs**, não de **mocks**.

---

## Questão 5: Uma classe que simula uma base de dados usando um array list em vez de uma base de dados real pode ser classificada como que tipo de dublê de teste?

### Resposta certa:
- **Fake object.**

### Justificativa para as erradas:
- **b. Dummy object.**
  - Está errado porque dummy objects não têm implementação, enquanto um fake object tem.
  
- **c. Mock.**
  - Está errado porque mocks são usados para verificar interações, não para simular implementações reais.
  
- **d. Stub.**
  - Está errado porque stubs não possuem uma implementação real, ao contrário de fake objects.

---

## Questão 6: O que pode ser necessário para injetar dublês de teste nas classes sendo testadas?

### Resposta certa:
- **Pode ser necessário alterar o código da classe sendo testada para passar a classe de dependência que será mockada em seu construtor.**

### Justificativa para as erradas:
- **a. Pode ser necessário criar um tipo especial de dublê de teste que seja capaz de interceptar as chamadas da classe sendo testada a partir da classe de dependência.**
  - Está errado porque a abordagem mais comum é modificar o construtor da classe, não criar um dublê especial.
  
- **b. Pode ser necessário refatorar o construtor da classe de teste para instanciar a classe que será mockada no código da classe sendo testada.**
  - Está errado porque a refatoração é na classe sendo testada, não na classe de teste.
  
- **c. Pode ser necessário utilizar um framework de mocking para que o dublê de teste seja injetado na classe de dependência.**
  - Embora possa ser verdade em alguns casos, a resposta correta é mais abrangente ao envolver a alteração do código da classe sendo testada.

---

## Questão 7: Qual é a principal vantagem de configurar dublês para lançar exceções em testes de software?

### Resposta certa:
- **Permite testar como os sistemas se comportariam em cenários inesperados, simulando a indisponibilidade de sistemas externos.**

### Justificativa para as erradas:
- **b. Garante que todos os métodos da aplicação sejam chamados pelo menos uma vez durante o teste, cobrindo diversos cenários.**
  - Está errado porque o lançamento de exceções não garante a chamada de todos os métodos.
  
- **c. Facilita a implementação de respostas codificadas para chamadas realizadas durante o teste, simplificando o processo.**
  - Está errado porque lançar exceções não simplifica a implementação de respostas codificadas.
  
- **d. Substitui a necessidade de testes de integração com sistemas externos reais, economizando tempo e recursos.**
  - Está errado porque lançar exceções não elimina a necessidade de testes de integração com sistemas reais.

---

## Questão 8: Qual é uma das principais desvantagens de usar dublês de teste?

### Resposta certa:
- **O acoplamento entre os dublês e o código de produção, que pode causar a falha dos testes quando a interação entre as classes muda.**

### Justificativa para as erradas:
- **b. A dificuldade em configurar e manter os dublês durante o ciclo de vida do projeto, resultando em testes menos eficientes.**
  - Está errado porque a configuração dos dublês pode ser trabalhosa, mas isso não é a principal desvantagem.
  
- **c. A incapacidade de dublês em simular comportamentos complexos de sistemas externos, limitando a eficácia dos testes.**
  - Está errado porque dublês podem simular comportamentos complexos, mas o problema está no acoplamento ao código.
  
- **d. A necessidade de modificar o código de produção para acomodar o uso de dublês, introduzindo complexidade desnecessária.**
  - Está errado porque a modificação do código não é sempre necessária e não é o principal problema com dublês.

---

## Questão 9: Qual é o ciclo repetido no processo de TDD (Test-Driven Development)?

### Resposta certa:
- **Escrever um teste que falhe, implementar a funcionalidade para que o teste passe, refatorar o código de produção e de teste.**

### Justificativa para as erradas:
- **a. Escrever um teste que passe, implementar a funcionalidade, refatorar o código de produção e de teste.**
  - Está errado porque o ciclo de TDD começa com um teste que falha, e não que já passa.
  
- **c. Implementar a funcionalidade, escrever um teste que passe, refatorar o código de produção e de teste.**
  - Está errado porque o TDD começa com o teste, não com a implementação da funcionalidade.
  
- **d. Refatorar o código de produção, escrever um teste que falhe, implementar a funcionalidade para que o teste passe.**
  - Está errado porque a refatoração é o último passo no ciclo de TDD.

---

## Questão 10: Por que o TDD facilita a identificação de novos problemas à medida que surgem?

### Resposta certa:
- **Porque os desenvolvedores são forçados a dar um passo de cada vez, escrevendo um teste, fazendo-o passar e refletindo sobre isso, o que torna mais fácil identificar problemas depois de escrever apenas uma pequena quantidade de código.**

### Justificativa para as erradas:
- **a. Porque os desenvolvedores escrevem grandes pedaços de código de produção antes de obter qualquer feedback, o que facilita a identificação de problemas em um estágio mais avançado.**
  - Está errado porque o TDD envolve pequenos incrementos de código, não grandes pedaços.
  
- **b. Porque os desenvolvedores podem focar especificamente no código, o que permite que estejam mais concentrados no produto final para identificar os problemas.

**
  - Está errado porque o foco do TDD é em pequenos incrementos e não no produto final como um todo.
  
- **c. Porque os desenvolvedores escrevem todos os testes de uma vez e depois implementam a funcionalidade, o que permite uma visão completa do sistema antes de começar a escrever o código.**
  - Está errado porque no TDD os testes são escritos um de cada vez, e não todos de uma vez.

---

## Questão 11: Como o TDD afeta o design das classes ou componentes?

### Resposta certa:
- **O código de teste é frequentemente o primeiro cliente da classe ou componente, e se é difícil instanciar a classe, invocar um método e verificar os resultados, isso sugere que pode haver uma maneira melhor de projetar a classe.**

### Justificativa para as erradas:
- **a. O código de teste raramente influencia o design das classes ou componentes, uma vez que ele é escrito após a implementação estar completa, então não afeta a estrutura do código.**
  - Está errado porque no TDD o código de teste influencia diretamente o design das classes.
  
- **c. O TDD encoraja designs mais complexos, uma vez que cada teste deve cobrir múltiplos casos de uso, aumentando a complexidade do design e da implementação.**
  - Está errado porque o TDD tende a simplificar o design, focando em pequenos incrementos.
  
- **d. O TDD desencoraja a refatoração, pois os desenvolvedores se concentram apenas em fazer os testes passarem, sem considerar o design, resultando em um código menos flexível.**
  - Está errado porque o TDD incentiva a refatoração contínua para melhorar o design.

---

## Questão 12: Quando o uso do TDD pode ser mais vantajoso?

### Resposta certa:
- **Em problemas mais complicados, onde a abordagem TDD ajuda a estruturar melhor o desenvolvimento e detectar problemas de design mais cedo.**

### Justificativa para as erradas:
- **a. Em problemas simples, onde a abordagem TDD pode ser aplicada rapidamente, em ciclos curtos de desenvolvimento.**
  - Está errado porque o TDD tende a ser mais vantajoso em problemas mais complexos.
  
- **b. Em qualquer tipo de problema, independentemente da complexidade, pois os benefícios do TDD são sempre os mesmos.**
  - Está errado porque o TDD é mais útil em problemas complexos, onde a estruturação incremental é mais necessária.
  
- **c. Em projetos de manutenção, onde o código já está bem estabelecido e requer poucas mudanças.**
  - Está errado porque o TDD é mais eficaz em novos desenvolvimentos, não em manutenção.

---

## Questão 13: Em quais situações o uso do TDD não é recomendado?

### Resposta certa:
- **Quando o problema é bem conhecido e não há necessidade de experimentação.**

### Justificativa para as erradas:
- **b. Quando se está trabalhando em projetos ágeis, onde a velocidade de entrega é crucial.**
  - Está errado porque o TDD pode ser usado em ambientes ágeis, e a velocidade de entrega não é um impedimento direto.
  
- **c. Quando se está desenvolvendo software para sistemas embarcados, devido às suas limitações naturais.**
  - Está errado porque o TDD pode ser aplicado a sistemas embarcados, apesar das limitações.
  
- **d. Quando a pirâmide de testes não estiver sendo aplicada como estratégia de testes.**
  - Está errado porque o uso do TDD não depende da pirâmide de testes.

---

## Questão 14: Qual é a eficácia dos testes gerados durante as sessões de TDD em comparação com testes sistemáticos?

### Resposta certa:
- **As suítes de teste geradas durante as sessões de TDD não são tão boas quanto as suítes de teste sistemáticos, pois TDD foca no desenvolvimento e não no teste.**

### Justificativa para as erradas:
- **a. As suítes de teste geradas durante as sessões de TDD são superiores às suítes de teste sistemáticos em vários aspectos.**
  - Está errado porque os testes gerados durante o TDD são voltados ao desenvolvimento, não são superiores aos testes sistemáticos.
  
- **b. As suítes de teste geradas durante as sessões de TDD são equivalentes às suítes de teste sistemáticos, pois ambos os métodos produzem resultados similares.**
  - Está errado porque os testes do TDD não são tão completos quanto os testes sistemáticos.
  
- **c. As suítes de teste geradas durante as sessões de TDD são inferiores às suítes de teste sistemáticos apenas em projetos pequenos e simples.**
  - Está errado porque os testes gerados no TDD tendem a ser menos abrangentes em projetos de qualquer tamanho.