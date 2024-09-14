# Atividades de Aplicação em Equipe 4 (AAE-4): TDD - Os Abandonados

## Enunciado

**Objetivo**: Desenvolver um pequeno sistema para manter uma agenda dos eventos que deseja assistir nos Jogos Olímpicos.

### Requisitos do Usuário para o Agendador dos Jogos Olímpicos:

1. **Adicionar Evento**:
   - O sistema deve permitir que o usuário adicione um evento à agenda, fornecendo o nome do evento, a hora de início e a hora de término.
   - O usuário deve ser solicitado a inserir o nome do evento, a hora de início e a hora de término no formato "YYYY-MM-DD HH:MM".
   - O sistema deve verificar conflitos de agendamento antes de adicionar o evento. Se um conflito for detectado, o sistema não deve adicionar o evento e deve informar o usuário.

2. **Remover Evento**:
   - O sistema deve permitir que o usuário remova um evento da agenda, fornecendo o nome do evento.

3. **Mostrar Agenda**:
   - O sistema deve permitir que o usuário visualize a agenda atual, listando todos os eventos com seus respectivos horários de início e término.

4. **Lidar com Entradas Inválidas**:
   - O sistema deve lidar com entradas inválidas de forma adequada e informar o usuário sobre quaisquer erros, como formatos de data incorretos ou ações inválidas.

5. **Sair**:
   - O sistema deve permitir que o usuário saia da aplicação.

---

## Resolução

### Funcionalidade: Adicionar Evento

#### Ciclo 1:
- **Código de Teste**: Implementação do primeiro teste para a funcionalidade de adicionar evento, incluindo as validações de formato de data e hora.
- **Código Implementado**: Primeira versão do código de adição de evento.

#### Ciclo 2:
- **Código de Teste**: Adição de novos casos de teste para verificar conflitos de agendamento.
- **Código Implementado**: Implementação da verificação de conflitos ao adicionar eventos à agenda.

#### Ciclo 3:
- **Código de Teste**: Expansão do teste para incluir casos de sucesso e erro ao adicionar eventos.
- **Código Implementado**: Refatoração do código de adição de eventos para melhorar a legibilidade e garantir o tratamento correto de conflitos.

#### Ciclo 4:
- **Código de Teste**: Testes adicionais para entradas inválidas, como formato de data incorreto.
- **Código Implementado**: Tratamento de entradas inválidas e verificação de formato de data/hora.

---

### Funcionalidade: Remover Evento

#### Ciclo 5:
- **Código de Teste**: Testes para a funcionalidade de remoção de eventos da agenda.
- **Código Implementado**: Implementação inicial da funcionalidade de remoção de eventos.

#### Ciclo 6:
- **Código de Teste**: Testes de borda para remoção de eventos inexistentes.
- **Código Implementado**: Refatoração do código de remoção para lidar com eventos não encontrados.

---

### Funcionalidade: Mostrar Agenda

#### Ciclo 7:
- **Código de Teste**: Testes para exibir corretamente a agenda com múltiplos eventos.
- **Código Implementado**: Implementação da funcionalidade de exibição da agenda.
- **Código Refatorado**: Refatoração da função de exibição para melhorar a performance e o layout.

#### Ciclo 8:
- **Código de Teste**: Testes para quando a agenda está vazia.
- **Código Implementado**: Implementação final da funcionalidade de exibir agenda.

---

### Funcionalidade: Sair

#### Ciclo 9:
- **Código de Teste**: Teste para a funcionalidade de sair do sistema.
- **Código Implementado**: Implementação da função de sair.

---

### Código Completo

O código final, após a implementação de todas as funcionalidades e refatorações, inclui as seguintes funcionalidades:
- Adicionar evento
- Remover evento
- Mostrar agenda
- Lidar com entradas inválidas
- Sair

### Suíte de Testes

1. Suíte de testes para a funcionalidade de adicionar evento, cobrindo todos os casos de sucesso, conflitos e entradas inválidas.
2. Suíte de testes para remoção de eventos, incluindo casos de eventos inexistentes.
3. Testes para exibir a agenda e lidar com a exibição correta dos eventos.

**Execução dos testes na IDE**: Todos os testes foram executados com sucesso, conforme print da IDE.

Link para o repositório GitHub com o código completo e os testes: [GitHub AAE-4](https://github.com/VasconcelosJoao/AAE4)