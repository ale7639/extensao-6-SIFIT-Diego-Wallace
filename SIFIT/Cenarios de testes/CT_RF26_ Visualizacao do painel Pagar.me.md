## Cenário 26: Visualização do painel Pagar.me

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

---

### Caso de Teste 01: Abrir painel

| ID | Descrição |
| :------- | :--------- |
| C26-CT01 | Visualizar saldos e gráficos. |

| **Pré-condições** |
| :---------------- |
| Menu Pagar.me. |

| **Passos** |
| :--------- |
| **DADO** que o painel carrega |
| **E** cards de saldo estão visíveis |
| **QUANDO** observar |
| **ENTÃO** painel exibido |

| **Critérios de aceitação** |
| :------------------------- |
| Tela abre sem erro. |

---

### Caso de Teste 02: Sem saque real

| ID | Descrição |
| :------- | :--------- |
| C26-CT02 | Confirmar que não há saque no escopo. |

| **Pré-condições** |
| :---------------- |
| Painel aberto. |

| **Passos** |
| :--------- |
| **DADO** que a dupla apenas consulta |
| **E** não aciona saque |
| **QUANDO** encerrar visualização |
| **ENTÃO** nenhuma operação financeira real |

| **Critérios de aceitação** |
| :------------------------- |
| Escopo de visualização respeitado. |
