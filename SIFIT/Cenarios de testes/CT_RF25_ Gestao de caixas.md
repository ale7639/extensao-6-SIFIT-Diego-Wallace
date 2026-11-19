## Cenário 25: Gestão de caixas

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

---

### Caso de Teste 01: Listar caixas

| ID | Descrição |
| :------- | :--------- |
| C25-CT01 | Consultar caixas por período. |

| **Pré-condições** |
| :---------------- |
| Menu Caixas. |

| **Passos** |
| :--------- |
| **DADO** que a lista carrega |
| **E** filtros de data/status existem |
| **QUANDO** buscar período atual |
| **ENTÃO** caixas listados |

| **Critérios de aceitação** |
| :------------------------- |
| Consulta ok. |

---

### Caso de Teste 02: Abrir sem local

| ID | Descrição |
| :------- | :--------- |
| C25-CT02 | Validar local obrigatório. |

| **Pré-condições** |
| :---------------- |
| Abrir Caixa. |

| **Passos** |
| :--------- |
| **DADO** que o local não foi selecionado |
| **E** demais dados quaisquer |
| **QUANDO** confirmar abertura |
| **ENTÃO** validação de local |

| **Critérios de aceitação** |
| :------------------------- |
| Sem erro genérico de servidor. |

---

### Caso de Teste 03: Filtro status Aberto

| ID | Descrição |
| :------- | :--------- |
| C25-CT03 | Filtrar caixas abertos. |

| **Pré-condições** |
| :---------------- |
| Lista carregada. |

| **Passos** |
| :--------- |
| **DADO** que status Aberto é escolhido |
| **E** período amplo |
| **QUANDO** buscar |
| **ENTÃO** só abertos |

| **Critérios de aceitação** |
| :------------------------- |
| Filtro ok. |
