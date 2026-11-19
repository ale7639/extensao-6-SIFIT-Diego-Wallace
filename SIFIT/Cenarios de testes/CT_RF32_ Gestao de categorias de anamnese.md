## Cenário 32: Gestão de categorias de anamnese

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

---

### Caso de Teste 01: Nova categoria

| ID | Descrição |
| :------- | :--------- |
| C32-CT01 | Cadastrar DW-Cat-Saude. |

| **Pré-condições** |
| :---------------- |
| Menu Categorias. |

| **Passos** |
| :--------- |
| **DADO** que Nova Categoria está aberta |
| **E** informa nome |
| **QUANDO** salvar |
| **ENTÃO** categoria listada |

| **Critérios de aceitação** |
| :------------------------- |
| Cadastro ok. |

---

### Caso de Teste 02: Filtro status

| ID | Descrição |
| :------- | :--------- |
| C32-CT02 | Filtrar categorias ativas. |

| **Pré-condições** |
| :---------------- |
| Lista carregada. |

| **Passos** |
| :--------- |
| **DADO** que status Ativo é escolhido |
| **E** busca |
| **QUANDO** aplicar |
| **ENTÃO** só ativas |

| **Critérios de aceitação** |
| :------------------------- |
| Filtro ok. |
