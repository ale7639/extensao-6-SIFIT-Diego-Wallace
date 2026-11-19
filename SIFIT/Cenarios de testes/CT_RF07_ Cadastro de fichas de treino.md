## Cenário 07: Cadastro de fichas de treino

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

### Caso de Teste 01: Criar ficha com objetivo

| ID | Descrição |
| :------- | :--------- |
| C07-CT01 | Montar ficha DW com aluno e objetivo. |

| **Pré-condições** |
| :---------------- |
| Aluno e objetivos disponíveis. |

| **Passos** |
| :--------- |
| **DADO** que Nova Ficha está aberta |
| **E** seleciona aluno, personal e objetivo |
| **QUANDO** salvar/avançar exercícios |
| **ENTÃO** ficha é criada |

| **Critérios de aceitação** |
| :------------------------- |
| Ficha listada para o aluno. |

---

### Caso de Teste 02: Ficha sem objetivo

| ID | Descrição |
| :------- | :--------- |
| C07-CT02 | Verificar se objetivos carregam. |

| **Pré-condições** |
| :---------------- |
| Formulário de ficha. |

| **Passos** |
| :--------- |
| **DADO** que o seletor de objetivo é aberto |
| **E** a lista é observada |
| **QUANDO** tentar criar sem objetivo |
| **ENTÃO** sistema deve exigir objetivo |

| **Critérios de aceitação** |
| :------------------------- |
| Não cria ficha sem objetivo válido. |

