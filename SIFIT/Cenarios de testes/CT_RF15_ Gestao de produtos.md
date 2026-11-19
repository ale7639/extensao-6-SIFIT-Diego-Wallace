## Cenário 15: Gestão de produtos

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

---

### Caso de Teste 01: Produto de venda

| ID | Descrição |
| :------- | :--------- |
| C15-CT01 | Cadastrar produto DW-Shake com preço. |

| **Pré-condições** |
| :---------------- |
| Menu Produtos. |

| **Passos** |
| :--------- |
| **DADO** que Novo Produto está aberto |
| **E** tipo Venda e preço > 0 |
| **QUANDO** salvar |
| **ENTÃO** produto listado |

| **Critérios de aceitação** |
| :------------------------- |
| Produto com preço. |

---

### Caso de Teste 02: Sem nome

| ID | Descrição |
| :------- | :--------- |
| C15-CT02 | Bloquear produto sem nome. |

| **Pré-condições** |
| :---------------- |
| Formulário aberto. |

| **Passos** |
| :--------- |
| **DADO** que o nome está vazio |
| **E** demais campos quaisquer |
| **QUANDO** salvar |
| **ENTÃO** bloqueio |

| **Critérios de aceitação** |
| :------------------------- |
| Nome obrigatório. |
