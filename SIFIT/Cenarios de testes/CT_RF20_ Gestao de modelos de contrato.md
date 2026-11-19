## Cenário 20: Gestão de modelos de contrato

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

---

### Caso de Teste 01: Listar contratos

| ID | Descrição |
| :------- | :--------- |
| C20-CT01 | Abrir Modelos de Contrato. |

| **Pré-condições** |
| :---------------- |
| Menu correspondente. |

| **Passos** |
| :--------- |
| **DADO** que a tela abre |
| **E** há modelos esperados no ambiente |
| **QUANDO** observar lista |
| **ENTÃO** modelos aparecem |

| **Critérios de aceitação** |
| :------------------------- |
| Lista não vazia se houver cadastro. |

---

### Caso de Teste 02: Adicionar modelo

| ID | Descrição |
| :------- | :--------- |
| C20-CT02 | Cadastrar DW-Contrato. |

| **Pré-condições** |
| :---------------- |
| Botão Adicionar disponível. |

| **Passos** |
| :--------- |
| **DADO** que o formulário está aberto |
| **E** preenche nome DW-Contrato |
| **QUANDO** salvar |
| **ENTÃO** modelo listado |

| **Critérios de aceitação** |
| :------------------------- |
| Cadastro ok. |
