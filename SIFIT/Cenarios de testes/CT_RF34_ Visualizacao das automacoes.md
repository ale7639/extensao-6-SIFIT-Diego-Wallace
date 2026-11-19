## Cenário 34: Visualização das automações

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

---

### Caso de Teste 01: Listar automações

| ID | Descrição |
| :------- | :--------- |
| C34-CT01 | Abrir Inteligência e ver ativas. |

| **Pré-condições** |
| :---------------- |
| Menu Inteligência. |

| **Passos** |
| :--------- |
| **DADO** que a tela carrega |
| **E** frequência e última execução aparecem |
| **QUANDO** observar |
| **ENTÃO** automações listadas |

| **Critérios de aceitação** |
| :------------------------- |
| Painel legível. |

---

### Caso de Teste 02: Ver resultados

| ID | Descrição |
| :------- | :--------- |
| C34-CT02 | Acessar atalho de resultados. |

| **Pré-condições** |
| :---------------- |
| Automação listada. |

| **Passos** |
| :--------- |
| **DADO** que Ver resultados está disponível |
| **E** a ação é acionada |
| **QUANDO** clicar |
| **ENTÃO** navega para resultados |

| **Critérios de aceitação** |
| :------------------------- |
| Atalho funcional. |
