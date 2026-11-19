## Cenário 18: Consulta de modelos de ficha

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

---

### Caso de Teste 01: Listar modelos

| ID | Descrição |
| :------- | :--------- |
| C18-CT01 | Ver modelos existentes. |

| **Pré-condições** |
| :---------------- |
| Menu Modelos de Ficha. |

| **Passos** |
| :--------- |
| **DADO** que a tela abre |
| **E** cards/lista carregam |
| **QUANDO** observar |
| **ENTÃO** modelos visíveis |

| **Critérios de aceitação** |
| :------------------------- |
| Consulta ok. |

---

### Caso de Teste 02: Criar modelo

| ID | Descrição |
| :------- | :--------- |
| C18-CT02 | Tentar criar novo modelo. |

| **Pré-condições** |
| :---------------- |
| Acesso à criação. |

| **Passos** |
| :--------- |
| **DADO** que o formulário de modelo é aberto |
| **E** preenche título DW-Modelo |
| **QUANDO** salvar |
| **ENTÃO** modelo disponível |

| **Critérios de aceitação** |
| :------------------------- |
| Criação bem-sucedida. |
