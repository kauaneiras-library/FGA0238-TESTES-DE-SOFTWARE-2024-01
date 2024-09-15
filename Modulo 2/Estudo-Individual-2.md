# Módulo 2: Técnicas de Teste de Caixa Preta e Testes de Alto Nível

## Introdução ao Teste de Caixa Preta

No **teste de caixa preta**, também conhecido como **teste funcional**, o foco está em verificar se o sistema se comporta conforme esperado, sem levar em conta o código interno ou a implementação. O que importa são as entradas e saídas do sistema. O testador não precisa saber como o código foi escrito, mas deve garantir que ele produza os resultados corretos para as entradas dadas.

Essa técnica é usada principalmente para verificar se o software cumpre seus requisitos, e é muito útil quando se trata de encontrar erros relacionados ao comportamento e funcionalidade do software. No entanto, uma desvantagem é que o teste de caixa preta pode deixar partes do código sem teste, já que o testador não vê o código em si.

## Técnicas de Elaboração de Casos de Teste de Caixa Preta

Existem várias técnicas que podem ser usadas para criar casos de teste eficazes na caixa preta. Vamos detalhar algumas delas:

### 1. **Particionamento de Equivalência**
- **O que é?**: Essa técnica divide as entradas possíveis do sistema em diferentes grupos ou "classes de equivalência". Em vez de testar cada valor de entrada individualmente, você seleciona um valor representativo de cada classe. Assim, reduz-se o número de testes, sem perder a cobertura.
- **Exemplo**: Imagine que você está testando um campo que aceita idades de 1 a 100. Em vez de testar todas as idades possíveis, você pode criar três classes: valores menores que 1 (inválidos), valores entre 1 e 100 (válidos) e valores maiores que 100 (inválidos). Dessa forma, você pode testar com um valor de cada classe, como 0, 50 e 101.

### 2. **Análise de Valor Limite (Boundary Value Analysis)**
- **O que é?**: A análise de valor limite foca nos valores que estão nas "bordas" das classes de equivalência, já que esses pontos são onde geralmente ocorrem mais erros. O objetivo é testar esses limites extremos, como o valor mais alto e o mais baixo de um intervalo.
- **Exemplo**: Se temos o mesmo campo de idades entre 1 e 100, os limites são 1 e 100. Então, testaríamos os valores 0, 1, 100 e 101, pois são os mais propensos a revelar falhas.

### 3. **Tabela de Decisão (Decision Table Testing)**
- **O que é?**: Uma tabela de decisão é usada para representar combinações de condições de entrada e suas ações correspondentes. Isso ajuda a garantir que todos os cenários possíveis, com base nas condições de entrada, sejam testados.
- **Exemplo**: Imagine um sistema bancário que faz transferências com base em várias condições, como saldo disponível e valor da transação. Uma tabela de decisão ajuda a cobrir todas as combinações possíveis de saldo e valor de transação para garantir que o comportamento do sistema esteja correto em todos os casos.

### 4. **Teste de Transição de Estados (State Transition Testing)**
- **O que é?**: Esse teste é usado para sistemas que podem mudar de estado com base em determinadas entradas. O foco é testar as transições entre esses estados, verificando se o sistema reage corretamente a essas mudanças.
- **Exemplo**: Pense em um caixa eletrônico que pode estar em diferentes estados, como "pronto para transação", "aguardando cartão" ou "processando retirada". O teste de transição verifica se o sistema muda de um estado para outro corretamente, como ao inserir o cartão ou retirar o dinheiro.

### 5. **Teste de Causa-Efeito (Cause-Effect Graphing)**
- **O que é?**: Esta técnica envolve a criação de um gráfico que mostra as relações entre causas (entradas) e efeitos (saídas) no sistema. O objetivo é garantir que as combinações certas de entradas gerem as saídas corretas.
- **Exemplo**: Se uma causa for "valor maior que 100" e o efeito for "exibir erro", o teste de causa-efeito garante que o sistema exiba o erro quando a entrada for superior a 100.

---

## Testes de Alto Nível (High-Order Testing)

Os **testes de alto nível** são uma forma de testar o software a partir de uma perspectiva mais ampla, focando no sistema como um todo, e não apenas em componentes individuais. Eles visam identificar falhas que só podem aparecer quando o sistema é testado em um ambiente mais realista.

### 1. **Testes Funcionais**
- **O que é?**: Esses testes verificam se as funcionalidades do sistema estão operando conforme esperado. Ele envolve a verificação de entradas e saídas para garantir que o comportamento funcional esteja de acordo com a especificação.
- **Exemplo**: Verificar se o sistema de login funciona corretamente, aceitando credenciais válidas e rejeitando credenciais inválidas.

### 2. **Testes de Performance**
- **O que é?**: Testes de performance medem o quão bem o sistema responde sob certas condições de carga, como múltiplos usuários acessando simultaneamente ou grandes volumes de dados sendo processados.
- **Exemplo**: Testar se um site continua rápido quando mil usuários tentam acessar ao mesmo tempo.

### 3. **Testes de Compatibilidade**
- **O que é?**: Estes testes verificam se o software funciona corretamente em diferentes ambientes, como sistemas operacionais, navegadores ou dispositivos móveis. 
- **Exemplo**: Testar se um aplicativo web funciona igualmente bem no Chrome, Firefox, Safari e outros navegadores.

### 4. **Testes de Segurança**
- **O que é?**: Testes de segurança são usados para garantir que o sistema esteja protegido contra ataques externos, como tentativas de invasão, roubo de dados ou inserção de código malicioso.
- **Exemplo**: Verificar se o sistema está vulnerável a ataques de injeção de SQL, onde um atacante pode tentar inserir comandos maliciosos em um campo de entrada.

---

## Conclusão

O **Módulo 2** explora as diversas técnicas de **teste de caixa preta** e sua importância para garantir que o software esteja funcionando corretamente para o usuário final. Além disso, os **testes de alto nível** garantem que o sistema funcione adequadamente em um contexto maior, testando não apenas funcionalidades isoladas, mas também o desempenho, compatibilidade e segurança do software. Essas técnicas são essenciais para que o software seja robusto e confiável, minimizando o risco de erros e problemas após a implantação.