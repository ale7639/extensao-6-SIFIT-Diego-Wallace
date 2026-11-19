## Cenário 10: Geração e visualização de relatórios

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

### Caso de Teste 01: Relatório de clientes

| ID | Descrição |
| :------- | :--------- |
| C10-CT01 | Gerar relatório com datas válidas. |

| **Pré-condições** |
| :---------------- |
| Menu Relatórios. |

| **Passos** |
| :--------- |
| **DADO** que tipo Clientes é escolhido |
| **E** data início <= data fim |
| **QUANDO** gerar |
| **ENTÃO** arquivo abre corretamente |

| **Critérios de aceitação** |
| :------------------------- |
| Download íntegro. |

---

### Caso de Teste 02: Datas invertidas

| ID | Descrição |
| :------- | :--------- |
| C10-CT02 | Data fim anterior à início. |

| **Pré-condições** |
| :---------------- |
| Tela de relatório. |

| **Passos** |
| :--------- |
| **DADO** que o intervalo é inválido |
| **E** fim < início |
| **QUANDO** gerar |
| **ENTÃO** sistema bloqueia ou alerta |

| **Critérios de aceitação** |
| :------------------------- |
| Não gera relatório inválido. |

---

### Caso de Teste 03: Relatório de matrículas

| ID | Descrição |
| :------- | :--------- |
| C10-CT03 | Gerar outro tipo de relatório. |

| **Pré-condições** |
| :---------------- |
| Acesso a Relatórios. |

| **Passos** |
| :--------- |
| **DADO** que tipo Matrículas é escolhido |
| **E** período válido |
| **QUANDO** gerar |
| **ENTÃO** saída utilizável |

| **Critérios de aceitação** |
| :------------------------- |
| Relatório gerado. |
