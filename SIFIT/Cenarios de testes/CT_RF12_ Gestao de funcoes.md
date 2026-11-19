## Cenário 12: Gestão de funções

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

---

### Caso de Teste 01: Nova função

| ID | Descrição |
| :------- | :--------- |
| C12-CT01 | Cadastrar função DW-Recepcao. |

| **Pré-condições** |
| :---------------- |
| Menu Funções. |

| **Passos** |
| :--------- |
| **DADO** que Nova Função está aberta |
| **E** informa nome e tipo Interno |
| **QUANDO** salvar |
| **ENTÃO** função listada |

| **Critérios de aceitação** |
| :------------------------- |
| Função visível com tipo. |

---

### Caso de Teste 02: Filtro por tipo

| ID | Descrição |
| :------- | :--------- |
| C12-CT02 | Filtrar Interno/Externo. |

| **Pré-condições** |
| :---------------- |
| Lista com funções. |

| **Passos** |
| :--------- |
| **DADO** que o filtro de tipo é usado |
| **E** seleciona Interno |
| **QUANDO** buscar |
| **ENTÃO** só internas |

| **Critérios de aceitação** |
| :------------------------- |
| Filtro correto. |
