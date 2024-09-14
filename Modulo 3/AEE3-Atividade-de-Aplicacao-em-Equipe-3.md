# Atividades de Aplicação em Equipe 3 (AAE-3): Teste Caixa-Branca - Os Abandonados

## Enunciado

**Objetivo**: Elaborar a menor quantidade de casos de teste para o método abaixo de forma a garantir a cobertura de decisões/condições modificada (MC/DC).

### Instruções:

1. Construir a tabela identificando as decisões e condições do método, juntamente com as situações para que cada condição de cada decisão possa resultar em True e False.
   
2. Aplicar o método de cobertura de decisões/condições modificada (MC/DC) para elaborar os casos de teste (dados de entrada e saídas esperadas) atendendo às situações identificadas na tabela.
   
   - Elaborar a tabela verdade para as decisões com mais de uma condição.
   - Identificar TODOS os pares de independência de cada condição.
   - Elaborar os casos de teste a partir dos cenários identificados nos pares de independência e das situações para verdadeiro e falso obtidas no passo 1.

3. Deve ser elaborado o menor conjunto de casos de teste que garanta 100% de cobertura MC/DC.

### Entrega:
A atividade deve ser realizada em equipe e entregue até o final do dia, contendo as seguintes informações:

1. Tabela de identificação das decisões/condições e situações para verdadeiro e falso.
2. Tabela verdade para cada uma das decisões envolvendo mais de uma condição, com identificação dos pares de independência para cada condição, conforme o critério MC/DC.
3. Especificação dos casos de teste criados (com rastreabilidade para os cenários identificados).

---

## Resolução:

### 1. Tabela de Decisões/Condições

| ID  | Decisão (linha) | Condição                               | Situação para Verdadeiro | Situação para Falso                     |
|-----|-----------------|----------------------------------------|--------------------------|-----------------------------------------|
| 1   | 14              | `employees == null`                    | employees == null        | employees != null                      |
| 2   | 14              | `employees.isEmpty()`                  | Lista employees está vazia| Lista employees não está vazia         |
| 3   | 18              | `employee.getRole().equals("Manager")` | Há empregado "Manager"   | Não há empregado "Manager"             |
| 4   | 20              | `employee.getRole().equals("Senior")`  | Há empregado "Senior"    | Não há empregado "Senior"              |
| 5   | 22              | `employee.getRole().equals("Junior")`  | Há empregado "Junior"    | Não há empregado "Junior"              |
| 6   | 26              | `managerCount >= 1`                    | managerCount >= 1        | managerCount < 1                       |
| 7   | 26              | `seniorCount >= 2`                     | seniorCount >= 2         | seniorCount <= 1                       |
| 8   | 26              | `juniorCount >= 3`                     | juniorCount >= 3         | juniorCount <= 2                       |
| 9   | 26              | `managerCount >= 2`                    | managerCount >= 2        | managerCount < 2                       |

---

### 2. Tabela Verdade para cada uma das decisões envolvendo mais de uma condição

#### Decisão Linha 14

| Teste | Condição A (employees == null) | Condição B (employees.isEmpty()) | A or B |
|-------|-------------------------------|----------------------------------|--------|
| 1     | V                             | V                                | V      |
| 2     | V                             | F                                | V      |
| 3     | F                             | V                                | V      |
| 4     | F                             | F                                | F      |

**Pares de independência Linha 14**:
- Para A: Testes 2, 4
- Para B: Testes 3, 4

**Casos de teste Linha 14**:
- **Teste 2 (VF => V)**: A lista é nula, mas não está vazia.
- **Teste 3 (FV => V)**: A lista não é nula, mas está vazia.
- **Teste 4 (FF => F)**: A lista não é nula e não está vazia.

#### Decisão Linha 26

| Teste | Condição A (managerCount >= 1) | Condição B (seniorCount >= 2) | Condição C (juniorCount >= 3) | Condição D (managerCount >= 2) | (A and B and C) or D |
|-------|-------------------------------|-------------------------------|-------------------------------|-------------------------------|---------------------|
| 1     | V                             | V                             | V                             | V                             | V                   |
| 2     | V                             | V                             | V                             | F                             | V                   |
| 3     | V                             | V                             | F                             | V                             | V                   |
| 4     | V                             | V                             | F                             | F                             | F                   |
| 5     | V                             | F                             | V                             | V                             | V                   |
| 6     | V                             | F                             | V                             | F                             | F                   |
| 7     | V                             | F                             | F                             | V                             | V                   |
| 8     | V                             | F                             | F                             | F                             | F                   |
| 9     | F                             | V                             | V                             | V                             | V                   |
| 10    | F                             | V                             | V                             | F                             | F                   |
| 11    | F                             | V                             | F                             | V                             | V                   |
| 12    | F                             | V                             | F                             | F                             | F                   |
| 13    | F                             | F                             | V                             | V                             | V                   |
| 14    | F                             | F                             | V                             | F                             | F                   |
| 15    | F                             | F                             | F                             | V                             | V                   |
| 16    | F                             | F                             | F                             | F                             | F                   |

**Pares de independência Linha 26**:
- Para A: Testes 2, 10
- Para B: Testes 2, 6
- Para C: Testes 2, 4
- Para D: Testes 5, 6

**Casos de teste Linha 26**:
- **Teste 2 (VVVF => V)**: Manager >= 1, Senior >= 2, Junior >= 3, Manager < 2.
- **Teste 4 (VVFF => F)**: Manager >= 1, Senior >= 2, Junior < 3, Manager < 2.
- **Teste 5 (VFVV => V)**: Manager >= 1, Senior < 2, Junior >= 3, Manager >= 2.
- **Teste 6 (VFVF => F)**: Manager >= 1, Senior < 2, Junior >= 3, Manager < 2.
- **Teste 10 (FVVF => F)**: Manager < 1, Senior >= 2, Junior >= 3, Manager < 2.

---

### 3. Casos de Teste Criados

| Caso de Teste | Entrada | Saída Esperada | Cenários |
|---------------|---------|----------------|----------|
| 1             | employees = null | false          | 1V, 2F   |
| 2             | employees = []  | true           | 1F, 2V   |
| 3             | employees = [Sofia (Manager), Lucas (Senior), Isabela (Junior), Mateus (Supervisor), Laura (Senior), Gabriel (Junior), Julia (Junior)] | true | 1F, 2F, 3V, 4V, 5V, 6V, 7V, 8V, 9F |
| 4             | employees = [Sofia (Manager), Lucas (Senior), Laura (Senior)] | false | 1F, 2F, 3V, 4V, 5F, 6V, 7V, 8F, 9F |
| 5             | employees = [Sofia (Manager), Lucas (Manager), Isabela (Junior), Gabriel (Junior), Julia (Junior)] | true | 1F, 2F, 3V, 4V, 5V, 6V, 7F, 8V, 9V |
| 6             | employees = [Sofia (Manager), Lucas (Senior), Laura (Junior), Gabriel (Junior), Julia (Junior)] | false | 1F, 2F, 3V, 4V, 5F, 6V, 7F, 8V, 9F |
| 7             | employees = [Sofia (Senior), Lucas (Senior), Laura (Junior), Gabriel (Junior), Julia (Junior)] | false | 1F, 2F, 3F, 4V, 5V, 6F, 7V, 8V, 9F |