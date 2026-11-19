## Cenário 30: Aplicação de fichas de anamnese

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

---

### Caso de Teste 01: Aplicar anamnese

| ID | Descrição |
| :------- | :--------- |
| C30-CT01 | Aplicar modelo a aluno DW. |

| **Pré-condições** |
| :---------------- |
| Menu Anamneses. |

| **Passos** |
| :--------- |
| **DADO** que Nova Anamnese está aberta |
| **E** seleciona aluno e modelo |
| **QUANDO** concluir |
| **ENTÃO** ficha gravada na lista |

| **Critérios de aceitação** |
| :------------------------- |
| Persistência ok. |

---

### Caso de Teste 02: Sem aluno

| ID | Descrição |
| :------- | :--------- |
| C30-CT02 | Bloquear aplicação sem aluno. |

| **Pré-condições** |
| :---------------- |
| Formulário aberto. |

| **Passos** |
| :--------- |
| **DADO** que aluno não foi selecionado |
| **E** modelo qualquer |
| **QUANDO** salvar |
| **ENTÃO** validação |

| **Critérios de aceitação** |
| :------------------------- |
| Aluno obrigatório. |

---

### Caso de Teste 03: Filtro status

| ID | Descrição |
| :------- | :--------- |
| C30-CT03 | Filtrar Concluído/Pendente. |

| **Pré-condições** |
| :---------------- |
| Lista com fichas. |

| **Passos** |
| :--------- |
| **DADO** que o status é escolhido |
| **E** busca |
| **QUANDO** aplicar |
| **ENTÃO** lista filtrada |

| **Critérios de aceitação** |
| :------------------------- |
| Filtro ok. |
