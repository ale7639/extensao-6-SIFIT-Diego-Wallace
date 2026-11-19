## Cenário 11: Gestão de colaboradores

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

---

### Caso de Teste 01: Cadastro válido

| ID | Descrição |
| :------- | :--------- |
| C11-CT01 | Cadastrar colaborador DW-Colab. |

| **Pré-condições** |
| :---------------- |
| Menu Colaboradores. |

| **Passos** |
| :--------- |
| **DADO** que Novo Colaborador está aberto |
| **E** preenche nome, login único e CPF válido |
| **QUANDO** salvar |
| **ENTÃO** colaborador entra na lista |

| **Critérios de aceitação** |
| :------------------------- |
| Registro ativo listado. |

---

### Caso de Teste 02: CPF inválido

| ID | Descrição |
| :------- | :--------- |
| C11-CT02 | Rejeitar CPF 111.111.111-11. |

| **Pré-condições** |
| :---------------- |
| Formulário aberto. |

| **Passos** |
| :--------- |
| **DADO** que o CPF é inválido |
| **E** demais campos ok |
| **QUANDO** salvar |
| **ENTÃO** sistema rejeita |

| **Critérios de aceitação** |
| :------------------------- |
| Validação de CPF. |

---

### Caso de Teste 03: Login duplicado

| ID | Descrição |
| :------- | :--------- |
| C11-CT03 | Não permitir login já usado. |

| **Pré-condições** |
| :---------------- |
| Colaborador existente. |

| **Passos** |
| :--------- |
| **DADO** que o login já existe |
| **E** novo cadastro reutiliza o login |
| **QUANDO** salvar |
| **ENTÃO** erro de unicidade |

| **Critérios de aceitação** |
| :------------------------- |
| Login único. |
