## Cenário 37: Visualização das configurações

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

---

### Caso de Teste 01: Abrir abas

| ID | Descrição |
| :------- | :--------- |
| C37-CT01 | Percorrer abas principais. |

| **Pré-condições** |
| :---------------- |
| Menu Configurações. |

| **Passos** |
| :--------- |
| **DADO** que Configurações abre |
| **E** abas Home/Biometria/Pagamento existem |
| **QUANDO** navegar entre abas |
| **ENTÃO** conteúdo carrega |

| **Critérios de aceitação** |
| :------------------------- |
| Navegação ok. |

---

### Caso de Teste 02: Valor negativo ausência

| ID | Descrição |
| :------- | :--------- |
| C37-CT02 | Dias de ausência não deve aceitar negativo. |

| **Pré-condições** |
| :---------------- |
| Aba Home/presença. |

| **Passos** |
| :--------- |
| **DADO** que o campo de dias de ausência recebe -1 |
| **E** tentativa de salvar |
| **QUANDO** salvar configurações |
| **ENTÃO** valor rejeitado |

| **Critérios de aceitação** |
| :------------------------- |
| Validação de intervalo. |
