## Cenário 36: Gestão do aplicativo

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

---

### Caso de Teste 01: Abrir painel app

| ID | Descrição |
| :------- | :--------- |
| C36-CT01 | Consultar usuários e posts. |

| **Pré-condições** |
| :---------------- |
| Menu Aplicativo. |

| **Passos** |
| :--------- |
| **DADO** que a tela carrega |
| **E** cards de usuários/posts existem |
| **QUANDO** observar |
| **ENTÃO** painel web exibido |

| **Critérios de aceitação** |
| :------------------------- |
| Consulta ok (sem app mobile). |

---

### Caso de Teste 02: Listar notificações

| ID | Descrição |
| :------- | :--------- |
| C36-CT02 | Ver notificações existentes. |

| **Pré-condições** |
| :---------------- |
| Painel aberto. |

| **Passos** |
| :--------- |
| **DADO** que a área de notificações é aberta |
| **E** lista/carregamento ocorre |
| **QUANDO** observar |
| **ENTÃO** notificações listadas ou vazias sem erro |

| **Critérios de aceitação** |
| :------------------------- |
| Tela estável. |
