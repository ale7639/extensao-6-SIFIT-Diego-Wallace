## Cenário 38: Gestão do SifitBox

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

---

### Caso de Teste 01: Visibilidade Box

| ID | Descrição |
| :------- | :--------- |
| C38-CT01 | Verificar se menus Box aparecem conforme config. |

| **Pré-condições** |
| :---------------- |
| Config Box conhecida. |

| **Passos** |
| :--------- |
| **DADO** que a dupla acessa o menu |
| **E** observa Aulas/Turmas Box |
| **QUANDO** abrir se disponível |
| **ENTÃO** telas coerentes com a flag Box |

| **Critérios de aceitação** |
| :------------------------- |
| Comportamento alinhado à configuração. |

---

### Caso de Teste 02: Gerar aulas

| ID | Descrição |
| :------- | :--------- |
| C38-CT02 | Acionar Gerar aulas se disponível. |

| **Pré-condições** |
| :---------------- |
| Tela de Aulas Box. |

| **Passos** |
| :--------- |
| **DADO** que o botão Gerar aulas existe |
| **E** período informado |
| **QUANDO** gerar |
| **ENTÃO** aulas geradas ou mensagem clara |

| **Critérios de aceitação** |
| :------------------------- |
| Feedback ao usuário. |
