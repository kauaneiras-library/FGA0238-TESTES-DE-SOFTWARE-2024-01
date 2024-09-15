# Módulo 4: Test-Driven Development (TDD) e Dublês de Teste (Mocks)

## Introdução

Neste módulo, exploramos duas práticas fundamentais para o desenvolvimento de software com testes automatizados: o **Desenvolvimento Orientado por Testes** (TDD) e o uso de **Dublês de Teste** (Mocks). Ambas as técnicas são essenciais para garantir que o código seja escrito de forma robusta e confiável, permitindo que os desenvolvedores identifiquem erros logo no início e isolem componentes para testes mais eficientes.

## Test-Driven Development (TDD)

O **TDD** é uma abordagem de desenvolvimento que inverte a ordem comum: primeiro, escrevemos testes para o código que ainda não existe, e depois desenvolvemos o código para que os testes passem. Esse método é conhecido por melhorar a qualidade do código e garantir que a lógica esteja correta desde o início.

### Ciclo do TDD: Red, Green, Refactor

O TDD é baseado em um ciclo contínuo de três etapas: **Red**, **Green** e **Refactor**. Vamos entender cada uma dessas etapas de forma detalhada:

1. **Red (Vermelho)**
   - **O que é?**: Nessa etapa, o desenvolvedor escreve um teste para uma nova funcionalidade ou comportamento, sabendo que o teste irá falhar (ficará "vermelho"). Isso é esperado, pois o código funcional ainda não foi escrito.
   - **Objetivo**: Garantir que o teste realmente falhe, o que confirma que a funcionalidade ainda não foi implementada e o teste está verificando o comportamento correto.
   - **Exemplo**: Se você está criando uma função de soma, primeiro escreveria um teste que verifica se `soma(2, 3)` retorna 5, mas sem implementar a função.

2. **Green (Verde)**
   - **O que é?**: Nesta etapa, o desenvolvedor escreve o código mínimo necessário para fazer o teste passar (ficar "verde"). O foco aqui não é a perfeição, mas sim garantir que o teste passe.
   - **Objetivo**: Escrever o código mais simples possível para resolver o problema.
   - **Exemplo**: Após escrever o teste, você implementa a função `soma` com a lógica básica que retorna o resultado correto (por exemplo, `return a + b`).

3. **Refactor (Refatorar)**
   - **O que é?**: Com o teste passando, é hora de melhorar o código, tornando-o mais limpo e eficiente. Isso pode envolver a remoção de duplicações, simplificação de lógicas e aprimoramento da estrutura.
   - **Objetivo**: Melhorar o design do código sem alterar seu comportamento. Ao final da refatoração, os testes devem continuar passando.
   - **Exemplo**: Talvez você perceba que pode simplificar ou reorganizar o código sem mudar sua funcionalidade.

### Benefícios do TDD

- **Confiança no Código**: O TDD garante que cada pedaço de código que você escreve tem um teste que o valida. Isso ajuda a encontrar e corrigir bugs cedo.
- **Design Melhorado**: Pensar nos testes antes de escrever o código leva a um design mais modular e limpo, pois você precisa garantir que o código seja facilmente testável.
- **Documentação Viva**: Os testes criados no TDD funcionam como uma forma de documentação, pois mostram como o código deve se comportar em diferentes situações.
- **Manutenção Facilitada**: Quando o código é testado desde o início, alterações futuras podem ser feitas com mais segurança, já que os testes avisarão se algo importante quebrou.

### Desafios do TDD

- **Curva de Aprendizado**: Desenvolvedores que não estão acostumados a escrever testes antes podem achar o TDD difícil no início.
- **Manutenção dos Testes**: À medida que o código evolui, os testes precisam ser mantidos atualizados. Isso pode ser trabalhoso em grandes projetos.
- **Disciplina Necessária**: Seguir o ciclo Red-Green-Refactor rigorosamente exige disciplina, já que o desenvolvedor precisa sempre pensar em testes antes de qualquer implementação.

---

## Dublês de Teste (Mocks)

Os **dublês de teste** (ou **Test Doubles**) são usados para substituir partes reais do sistema durante os testes. Isso é útil quando você quer isolar uma parte do código para testar de forma mais eficaz, sem depender de outros componentes que podem ser difíceis de configurar ou lentos para rodar.

Existem **cinco tipos principais de dublês de teste**:

1. **Dummy Objects (Objetos Dummy)**
   - **O que são?**: São usados para preencher parâmetros necessários em um teste, mas nunca realmente utilizados no teste em si.
   - **Exemplo**: Se um método precisa de um objeto como parâmetro, mas o teste não usa esse objeto, você pode passar um Dummy que só existe para preencher o requisito.

2. **Fake Objects (Objetos Fake)**
   - **O que são?**: São versões simplificadas dos componentes reais que funcionam em um ambiente de teste, mas não serviriam para produção.
   - **Exemplo**: Um banco de dados em memória que simula o comportamento de um banco de dados real, mas de maneira muito mais rápida e simples.

3. **Stubs**
   - **O que são?**: São objetos que fornecem respostas predefinidas para chamadas de métodos durante o teste.
   - **Exemplo**: Um stub pode ser configurado para sempre retornar `true` quando um determinado método for chamado, independentemente do que acontece no código real.

4. **Spies**
   - **O que são?**: São objetos que registram informações sobre como foram usados durante o teste, permitindo verificar interações específicas.
   - **Exemplo**: Um spy pode registrar quantas vezes um método foi chamado e com quais parâmetros, permitindo verificar se o código está chamando o método corretamente.

5. **Mocks**
   - **O que são?**: São objetos mais complexos que permitem configurar expectativas sobre como devem ser usados e verificá-las depois.
   - **Exemplo**: Você pode criar um mock que espera que um método seja chamado exatamente três vezes, e com parâmetros específicos. Se isso não acontecer, o teste falha.

### Vantagens dos Mocks

- **Isolamento**: Mocks permitem testar uma unidade de código sem depender de outros componentes. Isso torna os testes mais rápidos e confiáveis.
- **Facilidade para Simular Cenários Complexos**: Com Mocks, você pode simular cenários complicados que seriam difíceis de configurar no ambiente real.
- **Cobertura de Testes Melhorada**: Ao isolar cada unidade de código, você pode focar em cobrir cada uma delas de forma mais detalhada.

### Desvantagens dos Mocks

- **Manutenção**: Em sistemas grandes, manter todos os mocks atualizados pode ser complicado, especialmente quando há mudanças na interface do código.
- **Testes Frágeis**: Mocks podem levar a testes frágeis que quebram facilmente com pequenas mudanças no código, pois estão muito acoplados à implementação.
- **Falso Senso de Segurança**: Mocks testam as interações esperadas, mas podem não cobrir completamente o comportamento real do sistema.

---

## Exemplo Prático: Construção de uma Calculadora de Imposto de Renda

No exemplo da calculadora de imposto de renda, o desenvolvimento foi guiado pelo TDD:

1. **Escrevendo Testes Primeiro**: O desenvolvedor escreveu testes para diferentes cenários de cálculo de imposto, como faixas de renda e deduções. Os testes falhavam inicialmente, pois o código ainda não havia sido implementado.
2. **Escrevendo o Código para Passar os Testes**: Em seguida, o código da calculadora foi escrito, começando com o cálculo básico de imposto. A cada etapa, o desenvolvedor escrevia o código mínimo necessário para passar os testes.
3. **Refatoração**: Após o código passar em todos os testes, o desenvolvedor refatorou partes da calculadora para torná-la mais eficiente e fácil de entender, sem quebrar os testes já existentes.

---

## Conclusão

O **Módulo 4** destaca a importância de técnicas como o **TDD** e o uso de **Mocks** para melhorar a qualidade e a confiabilidade do software. O **TDD** incentiva os desenvolvedores a pensar primeiro nos testes, o que resulta em código mais bem estruturado e menos propenso a erros. Já os **dublês de teste** (Mocks, Stubs, Spies, etc.) permitem testar unidades de código de forma isolada, simulando dependências e tornando o processo de teste mais eficiente. Essas ferramentas e práticas ajudam a garantir que o software seja robusto, fácil de manter e confiável.