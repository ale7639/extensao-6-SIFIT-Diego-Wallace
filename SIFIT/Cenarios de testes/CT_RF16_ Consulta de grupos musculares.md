## Cenário 16: Consulta de grupos musculares

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

---

### Caso de Teste 01: Listagem

| ID | Descrição |
| :------- | :--------- |
| C16-CT01 | Abrir grupos musculares e ver tipos. |

| **Pré-condições** |
| :---------------- |
| Menu Grupos Musculares. |

| **Passos** |
| :--------- |
| **DADO** que a lista carrega |
| **E** tipos Superiores/Inferiores/Aeróbio existem |
| **QUANDO** observar cards/lista |
| **ENTÃO** grupos exibidos |

| **Critérios de aceitação** |
| :------------------------- |
| Consulta ok. |

---

### Caso de Teste 02: Filtro por tipo

| ID | Descrição |
| :------- | :--------- |
| C16-CT02 | Filtrar Superiores. |

| **Pré-condições** |
| :---------------- |
| Lista carregada. |

| **Passos** |
| :--------- |
| **DADO** que o filtro de tipo é usado |
| **E** escolhe Superiores |
| **QUANDO** buscar |
| **ENTÃO** apenas superiores |

| **Critérios de aceitação** |
| :------------------------- |
| Filtro ok. |
