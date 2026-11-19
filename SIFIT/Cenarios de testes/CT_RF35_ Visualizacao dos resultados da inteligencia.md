## Cenário 35: Visualização dos resultados da inteligência

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

---

### Caso de Teste 01: Cards do período

| ID | Descrição |
| :------- | :--------- |
| C35-CT01 | Abrir resultados e ler cards. |

| **Pré-condições** |
| :---------------- |
| Menu Resultados IA. |

| **Passos** |
| :--------- |
| **DADO** que a tela carrega |
| **E** filtro padrão aplicado |
| **QUANDO** observar cards |
| **ENTÃO** métricas exibidas |

| **Critérios de aceitação** |
| :------------------------- |
| Cards legíveis. |

---

### Caso de Teste 02: Filtro Hoje

| ID | Descrição |
| :------- | :--------- |
| C35-CT02 | Aplicar filtro Hoje. |

| **Pré-condições** |
| :---------------- |
| Tela aberta. |

| **Passos** |
| :--------- |
| **DADO** que o filtro Hoje é escolhido |
| **E** cards atualizam |
| **QUANDO** aplicar |
| **ENTÃO** todos os cards refletem o filtro |

| **Critérios de aceitação** |
| :------------------------- |
| Filtro consistente. |
