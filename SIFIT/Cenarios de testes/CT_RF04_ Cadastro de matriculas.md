## Cenário 04: Cadastro de matrículas

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

### Caso de Teste 01: Nova matrícula válida

| ID | Descrição |
| :------- | :--------- |
| C04-CT01 | Matricular cliente em plano com valores. |

| **Pré-condições** |
| :---------------- |
| Cliente e plano disponíveis. |

| **Passos** |
| :--------- |
| **DADO** que Nova Matrícula está aberta |
| **E** seleciona cliente, plano, datas e pagamento |
| **QUANDO** salvar |
| **ENTÃO** matrícula entra na lista |

| **Critérios de aceitação** |
| :------------------------- |
| Registro com cliente, plano e status. |

---

### Caso de Teste 02: Matrícula sem tipo de pagamento

| ID | Descrição |
| :------- | :--------- |
| C04-CT02 | Validar obrigatoriedade do pagamento. |

| **Pré-condições** |
| :---------------- |
| Formulário aberto. |

| **Passos** |
| :--------- |
| **DADO** que os demais campos estão ok |
| **E** tipo de pagamento fica vazio |
| **QUANDO** avançar/salvar |
| **ENTÃO** sistema impede ou alerta |

| **Critérios de aceitação** |
| :------------------------- |
| Não conclui sem tipo de pagamento. |

---

### Caso de Teste 03: Busca de matrícula

| ID | Descrição |
| :------- | :--------- |
| C04-CT03 | Filtrar matrícula por nome do aluno. |

| **Pré-condições** |
| :---------------- |
| Lista de matrículas. |

| **Passos** |
| :--------- |
| **DADO** que há matrículas cadastradas |
| **E** filtra pelo nome |
| **QUANDO** buscar |
| **ENTÃO** lista reduz ao aluno |

| **Critérios de aceitação** |
| :------------------------- |
| Filtro funcional. |
