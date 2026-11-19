## Cenário 13: Gestão de fornecedores

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

---

### Caso de Teste 01: Cadastro DW-Forn

| ID | Descrição |
| :------- | :--------- |
| C13-CT01 | Cadastrar fornecedor com CNPJ válido. |

| **Pré-condições** |
| :---------------- |
| Menu Fornecedores. |

| **Passos** |
| :--------- |
| **DADO** que Novo Fornecedor está aberto |
| **E** preenche nome e CNPJ válido |
| **QUANDO** salvar |
| **ENTÃO** fornecedor listado |

| **Critérios de aceitação** |
| :------------------------- |
| Cadastro ok. |

---

### Caso de Teste 02: CNPJ inválido

| ID | Descrição |
| :------- | :--------- |
| C13-CT02 | Rejeitar CNPJ inválido. |

| **Pré-condições** |
| :---------------- |
| Formulário aberto. |

| **Passos** |
| :--------- |
| **DADO** que o CNPJ é inválido |
| **E** nome preenchido |
| **QUANDO** salvar |
| **ENTÃO** validação |

| **Critérios de aceitação** |
| :------------------------- |
| CNPJ rejeitado. |
