## Cenário 22: Gestão de tipos de pagamento

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

---

### Caso de Teste 01: Cadastro ativo

| ID | Descrição |
| :------- | :--------- |
| C22-CT01 | Criar DW-Pix como Ativo. |

| **Pré-condições** |
| :---------------- |
| Menu Tipos de Pagamento. |

| **Passos** |
| :--------- |
| **DADO** que Novo está aberto |
| **E** nome DW-Pix e status Ativo |
| **QUANDO** salvar |
| **ENTÃO** aparece Ativo na lista |

| **Critérios de aceitação** |
| :------------------------- |
| Status preservado. |

---

### Caso de Teste 02: Sem nome

| ID | Descrição |
| :------- | :--------- |
| C22-CT02 | Bloquear tipo sem nome. |

| **Pré-condições** |
| :---------------- |
| Formulário aberto. |

| **Passos** |
| :--------- |
| **DADO** que o nome está vazio |
| **E** demais campos ok |
| **QUANDO** salvar |
| **ENTÃO** bloqueio |

| **Critérios de aceitação** |
| :------------------------- |
| Nome obrigatório. |

---

### Caso de Teste 03: Filtro status

| ID | Descrição |
| :------- | :--------- |
| C22-CT03 | Filtrar Ativo/Inativo. |

| **Pré-condições** |
| :---------------- |
| Tipos existentes. |

| **Passos** |
| :--------- |
| **DADO** que o filtro de status é usado |
| **E** seleciona Ativo |
| **QUANDO** buscar |
| **ENTÃO** retorna ativos |

| **Critérios de aceitação** |
| :------------------------- |
| Filtro funcional. |
