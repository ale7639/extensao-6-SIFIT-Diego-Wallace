## Cenário 28: Gestão de pontuações

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

---

### Caso de Teste 01: Nova campanha

| ID | Descrição |
| :------- | :--------- |
| C28-CT01 | Criar pontuação DW com período válido. |

| **Pré-condições** |
| :---------------- |
| Menu Pontuação. |

| **Passos** |
| :--------- |
| **DADO** que Nova Pontuação está aberta |
| **E** informa nome, tipo e datas válidas |
| **QUANDO** salvar |
| **ENTÃO** campanha listada |

| **Critérios de aceitação** |
| :------------------------- |
| Período coerente. |

---

### Caso de Teste 02: Sem datas

| ID | Descrição |
| :------- | :--------- |
| C28-CT02 | Evitar período 0000-00-00. |

| **Pré-condições** |
| :---------------- |
| Formulário aberto. |

| **Passos** |
| :--------- |
| **DADO** que datas ficam vazias |
| **E** nome preenchido |
| **QUANDO** salvar |
| **ENTÃO** validação de datas |

| **Critérios de aceitação** |
| :------------------------- |
| Não grava período nulo inválido. |
