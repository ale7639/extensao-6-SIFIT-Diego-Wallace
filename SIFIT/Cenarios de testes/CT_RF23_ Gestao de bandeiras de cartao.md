## Cenário 23: Gestão de bandeiras de cartão

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

---

### Caso de Teste 01: Listar bandeiras

| ID | Descrição |
| :------- | :--------- |
| C23-CT01 | Abrir tela de bandeiras. |

| **Pré-condições** |
| :---------------- |
| Menu Bandeiras. |

| **Passos** |
| :--------- |
| **DADO** que a tela carrega |
| **E** espera-se registros do ambiente |
| **QUANDO** observar lista |
| **ENTÃO** bandeiras visíveis |

| **Critérios de aceitação** |
| :------------------------- |
| Lista coerente com cadastro. |

---

### Caso de Teste 02: Nova bandeira

| ID | Descrição |
| :------- | :--------- |
| C23-CT02 | Cadastrar DW-Bandeira. |

| **Pré-condições** |
| :---------------- |
| Botão Nova Bandeira. |

| **Passos** |
| :--------- |
| **DADO** que o formulário está aberto |
| **E** informa nome DW-Bandeira |
| **QUANDO** salvar |
| **ENTÃO** bandeira listada |

| **Critérios de aceitação** |
| :------------------------- |
| Cadastro ok. |
