## Cenário 06: Agendamento de avaliações físicas

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

### Caso de Teste 01: Agendar avaliação

| ID | Descrição |
| :------- | :--------- |
| C06-CT01 | Criar avaliação para aluno DW. |

| **Pré-condições** |
| :---------------- |
| Aluno e personal disponíveis. |

| **Passos** |
| :--------- |
| **DADO** que Nova Avaliação está aberta |
| **E** seleciona aluno, personal, data e hora |
| **QUANDO** salvar |
| **ENTÃO** avaliação fica Pendente na lista |

| **Critérios de aceitação** |
| :------------------------- |
| Registro visível com status. |

---

### Caso de Teste 02: Filtro por status

| ID | Descrição |
| :------- | :--------- |
| C06-CT02 | Filtrar Pendente/Realizado. |

| **Pré-condições** |
| :---------------- |
| Lista com avaliações. |

| **Passos** |
| :--------- |
| **DADO** que o filtro de status está disponível |
| **E** seleciona Pendente |
| **QUANDO** buscar |
| **ENTÃO** apenas pendentes aparecem |

| **Critérios de aceitação** |
| :------------------------- |
| Filtro correto. |

---

### Caso de Teste 03: Campos obrigatórios

| ID | Descrição |
| :------- | :--------- |
| C06-CT03 | Salvar avaliação incompleta. |

| **Pré-condições** |
| :---------------- |
| Formulário aberto. |

| **Passos** |
| :--------- |
| **DADO** que aluno não foi selecionado |
| **E** demais campos vazios |
| **QUANDO** salvar |
| **ENTÃO** sistema bloqueia |

| **Critérios de aceitação** |
| :------------------------- |
| Validação dos obrigatórios. |
