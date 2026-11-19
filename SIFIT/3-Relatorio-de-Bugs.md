# Relatório de bugs — SIFIT

**Software:** SIFIT — Sistema para Academias  
**QA:** Diego Santos Gonçalves (14523) e Wallace Gabriel (14542)  
**Entrega:** extensão 6 pontos (dupla)  
**Janela de execução:** 15/11/2026 a 19/11/2026  
**Ambiente:** Windows 11 · Chrome · https://sifit.centrion.com.br

Os bugs abaixo foram reencontrados ou revalidados pela dupla durante a execução dos cenários `CT_RFxx`. IDs usam o prefixo **DW-BUG**.

---

### DW-BUG-001 — “Manter conectado” não preserva a sessão

| Campo | Valor |
| --- | --- |
| Severidade | Média |
| Prioridade | Média |
| Status | Aberto |
| Caso | C01-CT03 |
| Executor | Diego |

**Passos:** login válido com “Manter conectado” → fechar aba → reabrir `sifit.centrion.com.br`.  
**Esperado:** home sem novo login.  
**Obtido:** tela de login; checkbox desmarcado.

---

### DW-BUG-002 — Contagem de ausentes divergente entre Home e Clientes

| Campo | Valor |
| --- | --- |
| Severidade | Média |
| Prioridade | Média |
| Status | Aberto |
| Caso | C02-CT01 / C03-CT03 |
| Executor | Diego |

**Passos:** comparar card “Clientes Ausentes” na home com o card “Ausentes” em Clientes no mesmo instante.  
**Esperado:** mesmo total.  
**Obtido:** valores diferentes (ex.: home > 0 e Clientes = 0).

---

### DW-BUG-003 — Total em aberto zerado com mensalidade vencida listada

| Campo | Valor |
| --- | --- |
| Severidade | Alta |
| Prioridade | Alta |
| Status | Aberto |
| Caso | C02-CT02 |
| Executor | Diego |

**Passos:** observar card “em aberto” e a lista de mensalidades pendentes na home.  
**Esperado:** soma das vencidas no total.  
**Obtido:** total R$ 0,00 com vencida visível.

---

### DW-BUG-004 — Paginação não acompanha o filtro de busca

| Campo | Valor |
| --- | --- |
| Severidade | Baixa |
| Prioridade | Baixa |
| Status | Aberto |
| Caso | C03-CT03 |
| Executor | Diego |

**Passos:** buscar cliente `DW-Aluno` e observar paginação.  
**Esperado:** páginas coerentes com o total filtrado.  
**Obtido:** várias páginas e botão “Próxima” com 1 resultado.

---

### DW-BUG-005 — Filtros pré-preenchidos não batem com a lista

| Campo | Valor |
| --- | --- |
| Severidade | Média |
| Prioridade | Média |
| Status | Aberto |
| Caso | C03-CT01 |
| Executor | Diego |

**Passos:** abrir Clientes sem limpar filtros.  
**Esperado:** lista coerente com filtros exibidos.  
**Obtido:** filtros preenchidos e lista inconsistente até limpar/buscar de novo.

---

### DW-BUG-006 — Erro genérico ao salvar plano sem grupo

| Campo | Valor |
| --- | --- |
| Severidade | Média |
| Prioridade | Média |
| Status | Aberto |
| Caso | C05-CT02 |
| Executor | Diego |

**Passos:** Novo Plano → preencher obrigatórios → omitir grupo → salvar.  
**Esperado:** validação de campo.  
**Obtido:** mensagem genérica de erro.

---

### DW-BUG-007 — Ranking de planos diverge da lista

| Campo | Valor |
| --- | --- |
| Severidade | Média |
| Prioridade | Média |
| Status | Aberto |
| Caso | C05-CT03 |
| Executor | Diego |

**Passos:** comparar quantidade de alunos no ranking e na grade de planos.  
**Esperado:** mesma quantidade para o mesmo plano.  
**Obtido:** números diferentes.

---

### DW-BUG-008 — Objetivo de treino não cadastra

| Campo | Valor |
| --- | --- |
| Severidade | Alta |
| Prioridade | Alta |
| Status | Aberto |
| Caso | C17-CT01 |
| Executor | Wallace |

**Passos:** Novo Objetivo `DW-Obj-Hipertrofia` → salvar.  
**Esperado:** objetivo na lista.  
**Obtido:** falha no fluxo; lista permanece sem o registro.

---

### DW-BUG-009 — Ficha de treino bloqueada por objetivos vazios

| Campo | Valor |
| --- | --- |
| Severidade | Alta |
| Prioridade | Alta |
| Status | Aberto |
| Caso | C07-CT01 |
| Executor | Wallace |

**Passos:** Nova Ficha → abrir seletor de objetivo.  
**Esperado:** objetivos disponíveis.  
**Obtido:** lista vazia; criação impossibilitada (efeito colateral do DW-BUG-008).

---

### DW-BUG-010 — Turma aceita horário inicial = horário final

| Campo | Valor |
| --- | --- |
| Severidade | Média |
| Prioridade | Média |
| Status | Aberto |
| Caso | C08-CT02 |
| Executor | Wallace |

**Passos:** cadastrar turma com início e fim iguais.  
**Esperado:** validação de intervalo.  
**Obtido:** cadastro aceito.

---

### DW-BUG-011 — Check-in confirmado permanece Pendente na UI

| Campo | Valor |
| --- | --- |
| Severidade | Alta |
| Prioridade | Alta |
| Status | Aberto |
| Caso | C08-CT03 |
| Executor | Wallace |

**Passos:** realizar check-in e consultar presença do aluno.  
**Esperado:** status Presente/confirmado.  
**Obtido:** permanece Pendente e não conta no total.

---

### DW-BUG-012 — Conta a receber em dinheiro exige bandeira

| Campo | Valor |
| --- | --- |
| Severidade | Alta |
| Prioridade | Alta |
| Status | Aberto |
| Caso | C09-CT01 |
| Executor | Diego |

**Passos:** nova conta a receber → tipo dinheiro.  
**Esperado:** bandeira não obrigatória.  
**Obtido:** exige bandeira; lista de bandeiras vazia.

---

### DW-BUG-013 — Card Total a Pagar zerado com pendência na lista

| Campo | Valor |
| --- | --- |
| Severidade | Alta |
| Prioridade | Alta |
| Status | Aberto |
| Caso | C09-CT03 |
| Executor | Diego |

**Passos:** abrir Contas a Pagar com pendência visível.  
**Esperado:** card soma a pendência.  
**Obtido:** card 0.

---

### DW-BUG-014 — Relatório de clientes baixa corrompido

| Campo | Valor |
| --- | --- |
| Severidade | Alta |
| Prioridade | Alta |
| Status | Aberto |
| Caso | C10-CT01 |
| Executor | Diego |

**Passos:** gerar relatório de Clientes no período válido.  
**Esperado:** PDF/arquivo abrível.  
**Obtido:** arquivo corrompido.

---

### DW-BUG-015 — Colaborador aceita CPF inválido

| Campo | Valor |
| --- | --- |
| Severidade | Média |
| Prioridade | Média |
| Status | Aberto |
| Caso | C11-CT02 |
| Executor | Diego |

**Passos:** cadastrar colaborador com CPF `111.111.111-11`.  
**Esperado:** rejeição.  
**Obtido:** aceito.

---

### DW-BUG-016 — Login de colaborador duplicado permitido

| Campo | Valor |
| --- | --- |
| Severidade | Alta |
| Prioridade | Alta |
| Status | Aberto |
| Caso | C11-CT01 |
| Executor | Diego |

**Passos:** cadastrar segundo colaborador com login já existente.  
**Esperado:** erro de unicidade.  
**Obtido:** cadastro aceito.

---

### DW-BUG-017 — Fornecedor aceita CNPJ inválido

| Campo | Valor |
| --- | --- |
| Severidade | Média |
| Prioridade | Média |
| Status | Aberto |
| Caso | C13-CT02 |
| Executor | Diego |

**Passos:** Novo Fornecedor `DW-Forn` com CNPJ inválido.  
**Esperado:** validação.  
**Obtido:** aceito.

---

### DW-BUG-018 — Produto sem nome é salvo

| Campo | Valor |
| --- | --- |
| Severidade | Média |
| Prioridade | Média |
| Status | Aberto |
| Caso | C15-CT02 |
| Executor | Wallace |

**Passos:** Novo Produto sem nome → salvar.  
**Esperado:** bloqueio.  
**Obtido:** registro criado sem nome.

---

### DW-BUG-019 — Modelo de ficha não cria

| Campo | Valor |
| --- | --- |
| Severidade | Alta |
| Prioridade | Alta |
| Status | Aberto |
| Caso | C18-CT01 |
| Executor | Wallace |

**Passos:** tentar criar modelo de ficha.  
**Esperado:** modelo disponível na lista.  
**Obtido:** fluxo falha; criação impossível.

---

### DW-BUG-020 — Tipo de pagamento ativo aparece inativo

| Campo | Valor |
| --- | --- |
| Severidade | Alta |
| Prioridade | Alta |
| Status | Aberto |
| Caso | C22-CT01 |
| Executor | Diego |

**Passos:** cadastrar tipo `DW-Pix` como Ativo.  
**Esperado:** status Ativo na lista.  
**Obtido:** aparece Inativo.

---

### DW-BUG-021 — Lista de bandeiras vazia com registros existentes

| Campo | Valor |
| --- | --- |
| Severidade | Alta |
| Prioridade | Alta |
| Status | Aberto |
| Caso | C23-CT01 |
| Executor | Diego |

**Passos:** abrir Bandeiras de Cartão.  
**Esperado:** listar cadastradas.  
**Obtido:** lista vazia.

---

### DW-BUG-022 — Abrir caixa sem local retorna erro de servidor

| Campo | Valor |
| --- | --- |
| Severidade | Média |
| Prioridade | Média |
| Status | Aberto |
| Caso | C25-CT02 |
| Executor | Diego |

**Passos:** Abrir Caixa sem selecionar local.  
**Esperado:** validação de campo.  
**Obtido:** “Erro no servidor”.

---

### DW-BUG-023 — Anamnese aplicada não grava

| Campo | Valor |
| --- | --- |
| Severidade | Alta |
| Prioridade | Alta |
| Status | Aberto |
| Caso | C30-CT01 |
| Executor | Wallace |

**Passos:** Nova Anamnese → selecionar aluno e modelo → concluir.  
**Esperado:** ficha na listagem.  
**Obtido:** não persiste / erro ao final.

---

### DW-BUG-024 — Dashboard exibe título incorreto

| Campo | Valor |
| --- | --- |
| Severidade | Baixa |
| Prioridade | Baixa |
| Status | Aberto |
| Caso | C39-CT01 |
| Executor | Diego |

**Passos:** abrir Dashboard pelo menu.  
**Esperado:** título Dashboard.  
**Obtido:** título “Despesas Fixas” em algum bloco/cabeçalho.

---

## Resumo por severidade

| Severidade | Quantidade |
| --- | --- |
| Alta | 12 |
| Média | 10 |
| Baixa | 2 |
| **Total** | **24** |
