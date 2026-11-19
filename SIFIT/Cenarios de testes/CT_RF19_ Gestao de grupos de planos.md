## Cenário 19: Gestão de grupos de planos

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

---

### Caso de Teste 01: Listar grupos

| ID | Descrição |
| :------- | :--------- |
| C19-CT01 | Consultar grupos de planos. |

| **Pré-condições** |
| :---------------- |
| Menu Grupos. |

| **Passos** |
| :--------- |
| **DADO** que a lista carrega |
| **E** filtros estão disponíveis |
| **QUANDO** observar status e tipo de caixa |
| **ENTÃO** grupos exibidos |

| **Critérios de aceitação** |
| :------------------------- |
| Listagem ok. |

---

### Caso de Teste 02: Filtro status

| ID | Descrição |
| :------- | :--------- |
| C19-CT02 | Filtrar grupos ativos. |

| **Pré-condições** |
| :---------------- |
| Lista carregada. |

| **Passos** |
| :--------- |
| **DADO** que status Ativo é escolhido |
| **E** demais filtros limpos |
| **QUANDO** buscar |
| **ENTÃO** só ativos |

| **Critérios de aceitação** |
| :------------------------- |
| Filtro ok. |
