## Cenário 08: Turmas e check-in

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

### Caso de Teste 01: Cadastro de turma

| ID | Descrição |
| :------- | :--------- |
| C08-CT01 | Criar turma DW-Manha com horário válido. |

| **Pré-condições** |
| :---------------- |
| Menu Turmas. |

| **Passos** |
| :--------- |
| **DADO** que Nova Turma está aberta |
| **E** informa nome, dias e horários distintos |
| **QUANDO** salvar |
| **ENTÃO** turma aparece na lista |

| **Critérios de aceitação** |
| :------------------------- |
| Turma ativa listada. |

---

### Caso de Teste 02: Horário inválido

| ID | Descrição |
| :------- | :--------- |
| C08-CT02 | Início igual ao fim. |

| **Pré-condições** |
| :---------------- |
| Formulário de turma. |

| **Passos** |
| :--------- |
| **DADO** que início e fim são iguais |
| **E** demais campos ok |
| **QUANDO** salvar |
| **ENTÃO** validação de intervalo |

| **Critérios de aceitação** |
| :------------------------- |
| Rejeita horário inválido. |

---

### Caso de Teste 03: Check-in por código

| ID | Descrição |
| :------- | :--------- |
| C08-CT03 | Registrar presença e conferir status. |

| **Pré-condições** |
| :---------------- |
| Turma e aluno ativos. |

| **Passos** |
| :--------- |
| **DADO** que o check-in é informado |
| **E** o código do cliente é usado |
| **QUANDO** confirmar |
| **ENTÃO** presença fica confirmada |

| **Critérios de aceitação** |
| :------------------------- |
| Status Presente e contagem atualizada. |
