## Cenário 01: Login na plataforma

Autores da execução: Diego Santos Gonçalves e Wallace Gabriel (extensão 6 pontos — dupla). Dados de teste usam o prefixo `DW-`.

### Caso de Teste 01: Login com credenciais válidas

| ID | Descrição |
| :------- | :--------- |
| C01-CT01 | Acesso com login e senha válidos do ambiente de aula. |

| **Pré-condições** |
| :---------------- |
| Credenciais válidas disponíveis (sem registrar senha neste repositório). |

| **Passos** |
| :--------- |
| **DADO** que a dupla está na página de login do SIFIT |
| **E** preenche login e senha válidos |
| **QUANDO** clicar em Entrar |
| **ENTÃO** a Página Inicial é exibida |

| **Critérios de aceitação** |
| :------------------------- |
| Redirecionamento para a home autenticada. |

---

### Caso de Teste 02: Login com senha inválida

| ID | Descrição |
| :------- | :--------- |
| C01-CT02 | Tentativa com senha incorreta deve falhar. |

| **Pré-condições** |
| :---------------- |
| Usuário de teste existe. |

| **Passos** |
| :--------- |
| **DADO** que a dupla está na página de login |
| **E** informa login válido e senha incorreta |
| **QUANDO** clicar em Entrar |
| **ENTÃO** mensagem de erro é exibida e o acesso é negado |

| **Critérios de aceitação** |
| :------------------------- |
| Mensagem clara de credenciais inválidas. |

---

### Caso de Teste 03: Login com Manter conectado

| ID | Descrição |
| :------- | :--------- |
| C01-CT03 | Sessão deve persistir ao reabrir o navegador/aba. |

| **Pré-condições** |
| :---------------- |
| Credenciais válidas. |

| **Passos** |
| :--------- |
| **DADO** que o login é feito com Manter conectado marcado |
| **E** a aba é fechada |
| **QUANDO** o sistema é aberto novamente |
| **ENTÃO** a home deve abrir sem novo login |

| **Critérios de aceitação** |
| :------------------------- |
| Sessão mantida conforme a opção. |
