## Cenário 24: Gestão de tipos de documentos

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

---

### Caso de Teste 01: Novo tipo

| ID | Descrição |
| :------- | :--------- |
| C24-CT01 | Cadastrar DW-Doc. |

| **Pré-condições** |
| :---------------- |
| Menu Tipos de Documento. |

| **Passos** |
| :--------- |
| **DADO** que Novo Tipo está aberto |
| **E** informa nome e aplicação |
| **QUANDO** salvar |
| **ENTÃO** tipo listado |

| **Critérios de aceitação** |
| :------------------------- |
| Cadastro ok. |

---

### Caso de Teste 02: Filtro aplicação

| ID | Descrição |
| :------- | :--------- |
| C24-CT02 | Filtrar por aplicação. |

| **Pré-condições** |
| :---------------- |
| Lista carregada. |

| **Passos** |
| :--------- |
| **DADO** que a aplicação Colaborador é escolhida |
| **E** busca |
| **QUANDO** aplicar filtro |
| **ENTÃO** só tipos da aplicação |

| **Critérios de aceitação** |
| :------------------------- |
| Filtro ok. |
