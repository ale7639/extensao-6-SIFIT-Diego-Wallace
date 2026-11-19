## Cenário 14: Gestão de leads na prospecção

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

---

### Caso de Teste 01: Adicionar lead

| ID | Descrição |
| :------- | :--------- |
| C14-CT01 | Cadastrar lead DW-Lead. |

| **Pré-condições** |
| :---------------- |
| Menu Prospecção. |

| **Passos** |
| :--------- |
| **DADO** que Adicionar Lead está aberto |
| **E** informa nome e estágio Novo Contato |
| **QUANDO** salvar |
| **ENTÃO** lead na lista |

| **Critérios de aceitação** |
| :------------------------- |
| Lead visível no estágio. |

---

### Caso de Teste 02: Filtro por estágio

| ID | Descrição |
| :------- | :--------- |
| C14-CT02 | Filtrar Interessado. |

| **Pré-condições** |
| :---------------- |
| Leads existentes. |

| **Passos** |
| :--------- |
| **DADO** que o filtro de estágio é usado |
| **E** seleciona Interessado |
| **QUANDO** aplicar |
| **ENTÃO** lista filtrada |

| **Critérios de aceitação** |
| :------------------------- |
| Filtro por estágio ok. |
