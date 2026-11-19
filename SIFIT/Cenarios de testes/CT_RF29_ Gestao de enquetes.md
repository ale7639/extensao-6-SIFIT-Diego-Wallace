## Cenário 29: Gestão de enquetes

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

---

### Caso de Teste 01: Nova enquete

| ID | Descrição |
| :------- | :--------- |
| C29-CT01 | Cadastrar enquete DW. |

| **Pré-condições** |
| :---------------- |
| Menu Enquetes. |

| **Passos** |
| :--------- |
| **DADO** que Nova Enquete está aberta |
| **E** informa pergunta DW |
| **QUANDO** salvar |
| **ENTÃO** enquete na lista |

| **Critérios de aceitação** |
| :------------------------- |
| Cadastro ok. |

---

### Caso de Teste 02: Filtro status

| ID | Descrição |
| :------- | :--------- |
| C29-CT02 | Filtrar ativas. |

| **Pré-condições** |
| :---------------- |
| Lista carregada. |

| **Passos** |
| :--------- |
| **DADO** que status Ativa é escolhido |
| **E** busca |
| **QUANDO** aplicar |
| **ENTÃO** só ativas |

| **Critérios de aceitação** |
| :------------------------- |
| Filtro ok. |
