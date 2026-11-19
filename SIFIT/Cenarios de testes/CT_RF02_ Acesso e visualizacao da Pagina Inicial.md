## Cenário 02: Acesso e visualização da Página Inicial

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

### Caso de Teste 01: Home após login

| ID | Descrição |
| :------- | :--------- |
| C02-CT01 | Verificar saudação, data e cards principais. |

| **Pré-condições** |
| :---------------- |
| Usuário autenticado. |

| **Passos** |
| :--------- |
| **DADO** que o login foi bem-sucedido |
| **E** a home carrega |
| **QUANDO** os cards são observados |
| **ENTÃO** indicadores e saudação aparecem |

| **Critérios de aceitação** |
| :------------------------- |
| Layout principal legível e navegável. |

---

### Caso de Teste 02: Consistência do valor em aberto

| ID | Descrição |
| :------- | :--------- |
| C02-CT02 | Total em aberto deve refletir mensalidades listadas. |

| **Pré-condições** |
| :---------------- |
| Home carregada. |

| **Passos** |
| :--------- |
| **DADO** que há mensalidade vencida listada |
| **E** o card em aberto é lido |
| **QUANDO** comparar lista e total |
| **ENTÃO** os valores devem ser coerentes |

| **Critérios de aceitação** |
| :------------------------- |
| Soma alinhada às pendências visíveis. |

---

### Caso de Teste 03: Filtro de período

| ID | Descrição |
| :------- | :--------- |
| C02-CT03 | Alterar período dos indicadores. |

| **Pré-condições** |
| :---------------- |
| Home carregada. |

| **Passos** |
| :--------- |
| **DADO** que o filtro de período está disponível |
| **E** um intervalo diferente é escolhido |
| **QUANDO** aplicar o filtro |
| **ENTÃO** os cards atualizam |

| **Critérios de aceitação** |
| :------------------------- |
| Indicadores reagem ao período. |
