## Cenário 27: Gestão de atividades

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

---

### Caso de Teste 01: Nova atividade

| ID | Descrição |
| :------- | :--------- |
| C27-CT01 | Cadastrar DW-Atividade com pontos. |

| **Pré-condições** |
| :---------------- |
| Menu Atividades. |

| **Passos** |
| :--------- |
| **DADO** que Nova Atividade está aberta |
| **E** informa nome e pontuação |
| **QUANDO** salvar |
| **ENTÃO** atividade listada |

| **Critérios de aceitação** |
| :------------------------- |
| Cadastro ok. |

---

### Caso de Teste 02: Busca

| ID | Descrição |
| :------- | :--------- |
| C27-CT02 | Buscar atividade DW. |

| **Pré-condições** |
| :---------------- |
| Lista carregada. |

| **Passos** |
| :--------- |
| **DADO** que o nome DW-Atividade é buscado |
| **E** código vazio |
| **QUANDO** buscar |
| **ENTÃO** resultado correspondente |

| **Critérios de aceitação** |
| :------------------------- |
| Busca ok. |
