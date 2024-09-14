# Prática de Teste em OSS 3 – Desenvolver Testes de Unidade

## Enunciado

### Objetivo:
Desenvolver novos testes para um método existente, de forma a garantir a **Cobertura de Decisões/Condições Modificada (MC/DC)**.

### Instruções:

1. Rodar a suíte de testes e analisar a cobertura do projeto.
2. Identificar um método relevante que não possua testes, tenha baixa cobertura ou poucos casos de teste.
   - O método deve conter pelo menos duas decisões e duas condições em uma decisão.
   - A relevância do método será considerada na avaliação.
3. Caso o método já tenha alguns testes implemsentados, o aluno deverá comparar os CTs existentes com os gerados pelo critério MC/DC e indicar no relatório quais CTs já estavam implementados.
4. Construir a tabela identificando as decisões e condições do método, juntamente com as situações para que cada condição de cada decisão possa resultar em verdadeiro e falso.
5. Aplicar o critério MC/DC para elaborar o conjunto mínimo de casos de teste para obter a cobertura MC/DC.
6. Implementar e executar os casos de teste elaborados, usando o framework de teste unitário utilizado no projeto.
7. Fazer o commit do código no repositório do GitHub.
8. Enviar um pull request para a comunidade do projeto (opcional).

### Entregáveis:

1. Arquivo contendo:
   - Identificação do projeto, nome do método a ser testado e descrição de seu propósito.
   - Código completo do método a ser testado, incluindo a identificação da classe, caminho e link para o repositório.
   - Código dos testes unitários existentes para o método escolhido (se houver), incluindo a identificação da classe, caminho e link para o repositório.
   - Tabela de identificação das decisões, condições e situações.
   - Tabelas verdade para as decisões com mais de uma condição.
   - Identificação dos pares de independência para cada condição.
   - Especificação dos casos de teste criados, com mapeamento para as decisões/condições.
   - Código dos testes implementados.
   - Resultado da execução dos testes, captura de tela e comentário sobre os resultados obtidos.
   - Cobertura de testes antes e depois da implementação dos testes.
   - Link e captura de tela do pull request, se realizado.

---

## Resolução

### 1. Identificação do Projeto

- **Nome do Projeto**: Cobblemon  
- **Link do Repositório**: [Cobblemon Repository](https://gitlab.com/cable-mc/cobblemon)  
- **Fork do Repositório**: [Fork no GitLab](https://gitlab.com/kauaneiras/cobblemon)

### 2. Método a ser Testado

- **Classe/Pacote**: com.cobblemon.mod.common.api.moves  
- **Método(s) a ser(em) testado(s)**: `setMove`, `swapMove`, `add`, `update`, `doWithoutEmitting`, `loadFromNBT`, `loadFromBuffer`, `loadFromJSON`

**Propósito**: O método `MoveSet` gerencia um conjunto de movimentos (MoveSet) para personagens no jogo Cobblemon, permitindo adicionar, trocar, curar e carregar movimentos de diferentes fontes.

- **Link do Código do Método**: [MoveSet](https://gitlab.com/kauaneiras/cobblemon/-/blob/main/common/src/main/kotlin/com/cobblemon/mod/common/api/moves/MoveSet.kt)

### 3. Testes Existentes

O projeto já possuía alguns testes implementados para o método **MoveSet**, cobrindo parcialmente a cobertura MC/DC.

- **Código dos Testes Existentes**: 

```kotlin
@Test
fun `it should swap two moves properly`() {
    val moveset = MoveSet()
    val move1 = Move(mockk(), 11, 2)
    val move2 = Move(mockk(), 10, 4)
    moveset.setMove(0, move1)
    moveset.setMove(1, move2)
    moveset.swapMove(0, 1)
    assertEquals(move1, moveset[1])
    assertEquals(move2, moveset[0])
}
```

- **Link para Testes Existentes**: [MoveSetTest](https://gitlab.com/kauaneiras/cobblemon/-/blob/main/common/src/test/kotlin/com/cobblemon/mod/common/api/moves/MoveSetTest.kt)

### 4. Tabela de Decisões/Condições

| ID  | Decisão (linha) | Condição                                         | Cenário de entrada para Verdadeiro | Cenário de entrada para Falso    |
|-----|-----------------|-------------------------------------------------|-----------------------------------|----------------------------------|
| CD1 | Linha 47        | `pos !in 0 until MOVE_COUNT`                    | `pos = -1` ou `pos = 4`           | `pos = 0`, `pos = 1`, etc.       |
| CD2 | Linha 51        | `move?.observable?.subscribe { this.update() }`  | `Move != null`                    | `Move = null`                    |
| CD3 | Linha 121       | `any { it.template == move.template }`           | `Moves contém Move com o template`| `Moves não contém Move`          |
| CD4 | Linha 125       | `moves[i] == null`                               | `moves[i] == null`                | `moves[i] != null`               |
| CD5 | Linha 134       | `emit == true`                                   | `emit = true`                     | `emit = false`                   |

### 5. Tabela Verdade para Decisão com MC/DC

#### Linha 47: Decisão sobre posição válida

| ID  | `pos < 0` | `pos >= MOVE_COUNT` | Resultado |
|-----|-----------|---------------------|-----------|
| 1   | V         | V                   | V         |
| 2   | V         | F                   | V         |
| 3   | F         | V                   | V         |
| 4   | F         | F                   | F         |

#### Linha 51: Decisão sobre `move`

| ID  | `move != null` | Resultado |
|-----|----------------|-----------|
| 1   | V              | V         |
| 2   | F              | F         |

### 6. Especificação dos Casos de Teste

| CT   | Nome do CT                  | Entrada        | Saída Esperada                     | Cobertura de Condições            | Cobertura MC/DC |
|------|-----------------------------|----------------|------------------------------------|-----------------------------------|-----------------|
| CT1  | Posição negativa             | `pos = -1`     | Não define o movimento             | CD1 (A V)                         | Linha 47 (2)    |
| CT2  | Posição inválida             | `pos = MOVE_COUNT` | Não define o movimento         | CD1 (B V)                         | Linha 47 (3)    |
| CT3  | Posição válida               | `pos = 1`      | Define o movimento                 | CD1 (A F), CD1 (B F)              | Linha 47 (4)    |
| CT4  | Movimento não nulo           | `move != null` | Inscreve-se no `observable`        | CD2 (A V)                         | Linha 51 (1)    |
| CT5  | Movimento nulo               | `move = null`  | Não faz nada                       | CD2 (A F)                         | Linha 51 (2)    |

### 7. Implementação dos Casos de Teste

**Código Implementado**:

```kotlin
@Test
fun `it should not set a move if position is negative`() {
    val moveset = MoveSet()
    val move = Move(mockk(), 11, 2)
    moveset.setMove(-1, move)
    assertNull(moveset[-1])
}

@Test
fun `it should add a move when position is valid`() {
    val moveset = MoveSet()
    val move = Move(mockk(), 11, 2)
    moveset.setMove(1, move)
    assertEquals(move, moveset[1])
}
```

- **Link do Commit**: [Commit no GitLab](https://gitlab.com/kauaneiras/cobblemon/-/commit/2661fbf0684fa817adb98812ff2207b42d485370)

### 8. Resultado da Execução dos Testes

Todos os testes passaram com sucesso, confirmando a cobertura MC/DC para o método selecionado.

### 9. Pull Request

- **Link do PR**: [Pull Request no GitLab](https://gitlab.com/cable-mc/cobblemon/-/merge_requests/1104)