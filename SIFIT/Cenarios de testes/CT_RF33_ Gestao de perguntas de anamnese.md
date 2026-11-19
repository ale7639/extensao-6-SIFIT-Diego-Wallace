## Cenário 33: Gestão de perguntas de anamnese

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

---

### Caso de Teste 01: Nova pergunta

| ID | Descrição |
| :------- | :--------- |
| C33-CT01 | Cadastrar pergunta DW com texto. |

| **Pré-condições** |
| :---------------- |
| Menu Perguntas. |

| **Passos** |
| :--------- |
| **DADO** que Nova Pergunta está aberta |
| **E** informa nome, texto e categoria se houver |
| **QUANDO** salvar |
| **ENTÃO** pergunta listada |

| **Critérios de aceitação** |
| :------------------------- |
| Cadastro ok. |

---

### Caso de Teste 02: Sem texto

| ID | Descrição |
| :------- | :--------- |
| C33-CT02 | Bloquear pergunta vazia. |

| **Pré-condições** |
| :---------------- |
| Formulário aberto. |

| **Passos** |
| :--------- |
| **DADO** que nome e texto estão vazios |
| **E** nenhum dado |
| **QUANDO** salvar |
| **ENTÃO** validação |

| **Critérios de aceitação** |
| :------------------------- |
| Campos obrigatórios. |
