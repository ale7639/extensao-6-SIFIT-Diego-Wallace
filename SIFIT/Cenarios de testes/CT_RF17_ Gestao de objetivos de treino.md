## Cenário 17: Gestão de objetivos de treino

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

---

### Caso de Teste 01: Novo objetivo

| ID | Descrição |
| :------- | :--------- |
| C17-CT01 | Cadastrar DW-Obj-Hipertrofia. |

| **Pré-condições** |
| :---------------- |
| Menu Objetivos. |

| **Passos** |
| :--------- |
| **DADO** que Novo Objetivo está aberto |
| **E** informa o nome DW-Obj-Hipertrofia |
| **QUANDO** salvar |
| **ENTÃO** objetivo na lista |

| **Critérios de aceitação** |
| :------------------------- |
| Objetivo cadastrado. |

---

### Caso de Teste 02: Busca por nome

| ID | Descrição |
| :------- | :--------- |
| C17-CT02 | Localizar objetivo DW. |

| **Pré-condições** |
| :---------------- |
| Lista de objetivos. |

| **Passos** |
| :--------- |
| **DADO** que o campo nome é preenchido |
| **E** busca DW-Obj |
| **QUANDO** buscar |
| **ENTÃO** resultado correspondente |

| **Critérios de aceitação** |
| :------------------------- |
| Busca funcional. |
