## Cenário 31: Gestão de modelos de anamnese

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

---

### Caso de Teste 01: Listar modelos

| ID | Descrição |
| :------- | :--------- |
| C31-CT01 | Abrir modelos e ver contagens. |

| **Pré-condições** |
| :---------------- |
| Menu Modelos de Anamnese. |

| **Passos** |
| :--------- |
| **DADO** que a lista carrega |
| **E** perguntas/aplicações são mostradas |
| **QUANDO** observar |
| **ENTÃO** modelos visíveis |

| **Critérios de aceitação** |
| :------------------------- |
| Consulta ok. |

---

### Caso de Teste 02: Preview

| ID | Descrição |
| :------- | :--------- |
| C31-CT02 | Abrir preview do modelo. |

| **Pré-condições** |
| :---------------- |
| Modelo existente. |

| **Passos** |
| :--------- |
| **DADO** que a ação Preview é usada |
| **E** modelo com perguntas |
| **QUANDO** abrir preview |
| **ENTÃO** perguntas aparecem |

| **Critérios de aceitação** |
| :------------------------- |
| Preview fiel ao cadastro. |
