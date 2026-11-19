## Cenário 09: Gerenciamento financeiro

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

### Caso de Teste 01: Conta a receber em dinheiro

| ID | Descrição |
| :------- | :--------- |
| C09-CT01 | Lançar recebimento sem exigir bandeira. |

| **Pré-condições** |
| :---------------- |
| Menu Contas a Receber. |

| **Passos** |
| :--------- |
| **DADO** que nova conta usa tipo dinheiro |
| **E** preenche valores e datas |
| **QUANDO** salvar |
| **ENTÃO** conta é registrada |

| **Critérios de aceitação** |
| :------------------------- |
| Dinheiro não exige bandeira. |

---

### Caso de Teste 02: Filtro por status

| ID | Descrição |
| :------- | :--------- |
| C09-CT02 | Filtrar Pendente/Recebido. |

| **Pré-condições** |
| :---------------- |
| Lista com contas. |

| **Passos** |
| :--------- |
| **DADO** que o filtro de status é usado |
| **E** seleciona Pendente |
| **QUANDO** buscar |
| **ENTÃO** só pendentes listam |

| **Critérios de aceitação** |
| :------------------------- |
| Filtro coerente. |

---

### Caso de Teste 03: Card Total a Pagar

| ID | Descrição |
| :------- | :--------- |
| C09-CT03 | Card deve somar pendências. |

| **Pré-condições** |
| :---------------- |
| Conta a pagar pendente na lista. |

| **Passos** |
| :--------- |
| **DADO** que Contas a Pagar está aberta |
| **E** há pendência visível |
| **QUANDO** ler o card Total a Pagar |
| **ENTÃO** valor > 0 coerente |

| **Critérios de aceitação** |
| :------------------------- |
| Card alinhado à lista. |
