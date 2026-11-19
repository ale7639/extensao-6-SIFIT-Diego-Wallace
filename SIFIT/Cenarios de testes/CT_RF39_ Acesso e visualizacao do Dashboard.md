## Cenário 39: Acesso e visualização do Dashboard

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

---

### Caso de Teste 01: Abrir Dashboard

| ID | Descrição |
| :------- | :--------- |
| C39-CT01 | Ver gráficos e bloco de inteligência. |

| **Pré-condições** |
| :---------------- |
| Menu Dashboard. |

| **Passos** |
| :--------- |
| **DADO** que a tela abre |
| **E** gráficos carregam |
| **QUANDO** observar título e blocos |
| **ENTÃO** Dashboard legível com título correto |

| **Critérios de aceitação** |
| :------------------------- |
| Título e gráficos corretos. |

---

### Caso de Teste 02: Bloco inteligência

| ID | Descrição |
| :------- | :--------- |
| C39-CT02 | Conferir cards de risco/aniversariantes. |

| **Pré-condições** |
| :---------------- |
| Dashboard aberto. |

| **Passos** |
| :--------- |
| **DADO** que o bloco Inteligência está visível |
| **E** cards são lidos |
| **QUANDO** observar |
| **ENTÃO** valores exibidos |

| **Critérios de aceitação** |
| :------------------------- |
| Bloco presente. |
