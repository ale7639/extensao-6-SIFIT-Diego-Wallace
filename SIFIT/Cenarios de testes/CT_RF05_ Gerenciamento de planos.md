## Cenário 05: Gerenciamento de planos

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

### Caso de Teste 01: Cadastro de plano DW

| ID | Descrição |
| :------- | :--------- |
| C05-CT01 | Criar plano DW-Mensal-Dupla. |

| **Pré-condições** |
| :---------------- |
| Menu Planos. |

| **Passos** |
| :--------- |
| **DADO** que Novo Plano está aberto |
| **E** preenche nome, valor e periodicidade |
| **QUANDO** salvar |
| **ENTÃO** plano aparece na lista |

| **Critérios de aceitação** |
| :------------------------- |
| Plano listado com valor. |

---

### Caso de Teste 02: Plano sem grupo

| ID | Descrição |
| :------- | :--------- |
| C05-CT02 | Salvar plano omitindo grupo. |

| **Pré-condições** |
| :---------------- |
| Formulário aberto. |

| **Passos** |
| :--------- |
| **DADO** que grupo não foi selecionado |
| **E** demais campos ok |
| **QUANDO** salvar |
| **ENTÃO** validação clara deve ocorrer |

| **Critérios de aceitação** |
| :------------------------- |
| Erro específico de grupo, não genérico. |

---

### Caso de Teste 03: Ranking versus lista

| ID | Descrição |
| :------- | :--------- |
| C05-CT03 | Comparar quantidade de alunos. |

| **Pré-condições** |
| :---------------- |
| Planos com alunos. |

| **Passos** |
| :--------- |
| **DADO** que ranking e lista estão visíveis |
| **E** escolhe um plano |
| **QUANDO** comparar contagens |
| **ENTÃO** números coincidem |

| **Critérios de aceitação** |
| :------------------------- |
| Consistência ranking × lista. |
