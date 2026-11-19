## Cenário 03: Gestão de clientes

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

### Caso de Teste 01: Cadastro de cliente DW

| ID | Descrição |
| :------- | :--------- |
| C03-CT01 | Cadastrar cliente com dados válidos e prefixo DW-. |

| **Pré-condições** |
| :---------------- |
| Acesso ao menu Clientes. |

| **Passos** |
| :--------- |
| **DADO** que a tela Novo Cliente está aberta |
| **E** preenche Nome DW-Aluno-Diego, sexo e nascimento |
| **QUANDO** salvar |
| **ENTÃO** o cliente aparece na lista |

| **Critérios de aceitação** |
| :------------------------- |
| Cliente DW-Aluno-Diego listado. |

---

### Caso de Teste 02: Validação de obrigatórios

| ID | Descrição |
| :------- | :--------- |
| C03-CT02 | Salvar sem campos obrigatórios. |

| **Pré-condições** |
| :---------------- |
| Formulário de cliente aberto. |

| **Passos** |
| :--------- |
| **DADO** que os obrigatórios estão vazios |
| **E** nenhum dado é informado |
| **QUANDO** tentar cadastrar |
| **ENTÃO** validações devem aparecer |

| **Critérios de aceitação** |
| :------------------------- |
| Bloqueio com mensagens nos campos. |

---

### Caso de Teste 03: Busca por nome

| ID | Descrição |
| :------- | :--------- |
| C03-CT03 | Localizar cliente DW pela busca. |

| **Pré-condições** |
| :---------------- |
| Cliente DW cadastrado ou existente. |

| **Passos** |
| :--------- |
| **DADO** que Clientes está aberto |
| **E** informa DW-Aluno no campo Nome |
| **QUANDO** buscar |
| **ENTÃO** resultado correspondente é listado |

| **Critérios de aceitação** |
| :------------------------- |
| Busca retorna o cliente esperado. |
