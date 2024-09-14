# Atividades de Aplicação em Equipe 3 (AAE-3): Teste Caixa-Preta - VolunTies

## Enunciado

Objetivo: Elaborar casos de teste para uma dada funcionalidade aplicando os critérios de teste **caixa-preta**.

### Instruções:

1. Leia atentamente a especificação de requisitos da funcionalidade a ser testada (material anexo). Caso tenha dúvidas sobre a especificação, questione o usuário/cliente (professora).

2. Identifique as condições de entrada e as condições de saída da funcionalidade, seus tipos e domínio de entrada.

3. A partir das condições de entrada e de saída, identifique as partições e as classes de equivalência válidas e inválidas.

4. Analise os valores limites de todas as partições.

5. Escreva casos de teste cobrindo o máximo de classes válidas, usando os valores limites.

6. Escreva um caso de teste para cada classe inválida, usando os valores limites.

---

## Resolução:

### Partições e Classes de Equivalência

| Condições de Entrada | Classes Válidas | Classes Inválidas |
|----------------------|-----------------|------------------|
| **Origem (O)**       | Cidades pertencentes à lista de origens (1). | Qualquer informação que não pertença à lista de origens (2). |
| **Destino (D)**       | Cidades pertencentes à lista de destinos e diferentes da cidade de origem (3). | Qualquer informação que não pertença à lista de destinos (4) ou igual à cidade de origem (5). |
| **Data da Viagem (DV)** | DV deve ser entre o dia atual e 2 anos a partir do dia atual (6). | DV anterior ao dia atual (7) e DV após 2 anos a partir do dia atual (8). |
| **Número de Passageiros (N)** | 1 <= N <= 180 (9). | N < 1 (10) e N > 180 (11). |
| **Assento (A)** | O assento (A) é composto por 3 caracteres no formato A = LN, onde: <br> - L ∈ {A, B, C, D, E, F}; <br> - N é um número de dois dígitos, começando com zero (0) se necessário e indo de 01 até 30 (12). | O assento (A) é inválido quando: <br> - Dígitos de A ≠ 3 (13); <br> - L ∉ {A, B, C, D, E, F} (14); <br> - Dígitos de N ≠ 2 (15); <br> - N < 1 ou N > 30 (16, 17). |

### Casos de Teste:

| Caso de Teste | O           | D             | DV          | N   | A    | Saída Esperada | Classes |
|---------------|-------------|---------------|-------------|-----|------|----------------|---------|
| 1             | Brasília     | São Paulo     | 30/04/2024  | 1   | A01  | Reserva concluída com sucesso. Voo de Brasília com destino a São Paulo, no dia 30/04/2024, com 1 passageiro. Seu assento é A01. | 1, 3, 6, 9, 12 |
| 2             | Fortaleza    | Rio de Janeiro| 30/04/2026  | 180 | F30  | Reserva concluída com sucesso. Voo de Fortaleza com destino ao Rio de Janeiro, no dia 30/04/2026, com 180 passageiros. Seu assento é F30. | 1, 3, 6, 9, 12 |
| 3             | GHH          | São Paulo     | 30/04/2024  | 1   | A01  | Falha na reserva, escolha uma origem válida. | 2 |
| 4             | Brasília     | GSS           | 30/04/2024  | 3   | A02  | Falha na reserva, escolha um destino válido. | 4 |
| 5             | Brasília     | Brasília      | 30/04/2024  | 3   | A03  | Falha na reserva, cidade de origem igual à cidade de destino. | 5 |
| 6             | Brasília     | São Paulo     | 29/04/2024  | 6   | A04  | Falha na reserva, data inválida. | 7 |
| 7             | Brasília     | São Paulo     | 01/05/2026  | 6   | A05  | Falha na reserva, data inválida. | 8 |
| 8             | Brasília     | São Paulo     | 30/04/2024  | 0   | A06  | Falha na reserva, número de passageiros menor que o mínimo. | 10 |
| 9             | Brasília     | São Paulo     | 30/04/2024  | 181 | A07  | Falha na reserva, número de passageiros maior que o máximo. | 11 |
| 10            | Florianópolis| Salvador      | 02/03/2025  | 2   | A300 | Falha na reserva, assento com mais de 3 dígitos. | 13 |
| 11            | Florianópolis| Salvador      | 02/03/2025  | 2   | A3   | Falha na reserva, assento com numeração diferente de 3 dígitos. | 13, 15 |
| 12            | Florianópolis| Salvador      | 02/03/2025  | 2   | P19  | Falha na reserva, letra do assento inválida. | 14 |
| 13            | Salvador     | Brasília      | 02/04/2025  | 1   | A1   | Falha na reserva, número de dígitos do assento inválido. | 13, 15 |
| 14            | Salvador     | Brasília      | 02/04/2025  | 1   | A00  | Falha na reserva, número do assento menor que 01. | 16 |
| 15            | Salvador     | Brasília      | 02/04/2025  | 1   | A31  | Falha na reserva, número do assento maior que 30. | 17 |