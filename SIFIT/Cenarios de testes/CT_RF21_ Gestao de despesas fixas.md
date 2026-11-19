## Cenário 21: Gestão de despesas fixas

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

---

### Caso de Teste 01: Listar despesas

| ID | Descrição |
| :------- | :--------- |
| C21-CT01 | Ver despesas e total. |

| **Pré-condições** |
| :---------------- |
| Menu Despesas Fixas. |

| **Passos** |
| :--------- |
| **DADO** que a lista carrega |
| **E** card de total está visível |
| **QUANDO** comparar total e itens |
| **ENTÃO** total coerente |

| **Critérios de aceitação** |
| :------------------------- |
| Soma alinhada. |

---

### Caso de Teste 02: Filtro recorrência

| ID | Descrição |
| :------- | :--------- |
| C21-CT02 | Filtrar por recorrência. |

| **Pré-condições** |
| :---------------- |
| Lista carregada. |

| **Passos** |
| :--------- |
| **DADO** que a recorrência é escolhida |
| **E** status qualquer |
| **QUANDO** buscar |
| **ENTÃO** lista filtrada |

| **Critérios de aceitação** |
| :------------------------- |
| Filtro ok. |
