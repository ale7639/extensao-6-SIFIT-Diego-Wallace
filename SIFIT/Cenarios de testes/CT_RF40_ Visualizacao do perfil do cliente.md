## Cenário 40: Visualização do perfil do cliente

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

---

### Caso de Teste 01: Abrir perfil

| ID | Descrição |
| :------- | :--------- |
| C40-CT01 | Abrir perfil a partir de Clientes. |

| **Pré-condições** |
| :---------------- |
| Cliente existente. |

| **Passos** |
| :--------- |
| **DADO** que a lista de clientes está aberta |
| **E** um cliente é selecionado |
| **QUANDO** abrir perfil |
| **ENTÃO** dados pessoais e matrícula aparecem |

| **Critérios de aceitação** |
| :------------------------- |
| Perfil completo. |

---

### Caso de Teste 02: Últimas presenças

| ID | Descrição |
| :------- | :--------- |
| C40-CT02 | Conferir bloco de presenças. |

| **Pré-condições** |
| :---------------- |
| Perfil aberto. |

| **Passos** |
| :--------- |
| **DADO** que há check-in conhecido no ambiente |
| **E** bloco Últimas Presenças é lido |
| **QUANDO** comparar com histórico |
| **ENTÃO** presenças coerentes |

| **Critérios de aceitação** |
| :------------------------- |
| Histórico alinhado. |
