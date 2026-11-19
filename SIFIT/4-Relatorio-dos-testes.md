# Relatório final de execução — SIFIT (dupla)

**Sistema:** SIFIT — Sistema para Academias (ambiente de aula)  
**Dupla:** Diego Santos Gonçalves (14523) e Wallace Gabriel (14542)  
**Entrega:** extensão 6 pontos  
**Execução:** 15/11/2026 a 19/11/2026  
**Ambiente:** Windows 11 · Chrome · https://sifit.centrion.com.br  
**Banco (somente leitura):** MySQL informado na aula — schema observado não espelha as entidades de academia; a persistência funcional observada pela dupla ocorre via API `https://backendsifit.centrion.com.br/api/`.

---

## Resumo da execução

| Total de casos | Passou | Passou com ressalva | Falhou | Bloqueado | Bugs |
| --- | --- | --- | --- | --- | --- |
| 96 | 68 | 14 | 12 | 2 | 24 |

**Passou com ressalva:** resultado principal ok, mas houve incoerência secundária (mensagem genérica, card desalinhado etc.).  
**Bloqueado:** não executável por dependência de outro defeito (ex.: ficha de treino sem objetivos).

---

## Cobertura por módulo

| RF | Módulo | Casos | Passou* | Bugs | IDs |
| --- | --- | --- | --- | --- | --- |
| RF01 | Login | 3 | 2 | 1 | DW-BUG-001 |
| RF02 | Página inicial | 3 | 2 | 2 | DW-BUG-002, 003 |
| RF03 | Clientes | 3 | 2 | 2 | DW-BUG-004, 005 |
| RF04 | Matrículas | 3 | 2 | 0 | — |
| RF05 | Planos | 3 | 1 | 2 | DW-BUG-006, 007 |
| RF06 | Avaliações | 3 | 3 | 0 | — |
| RF07 | Fichas de treino | 2 | 0 | 1 | DW-BUG-009 (1 bloqueado) |
| RF08 | Turmas e check-in | 3 | 1 | 2 | DW-BUG-010, 011 |
| RF09 | Financeiro | 3 | 1 | 2 | DW-BUG-012, 013 |
| RF10 | Relatórios | 3 | 1 | 1 | DW-BUG-014 |
| RF11 | Colaboradores | 3 | 1 | 2 | DW-BUG-015, 016 |
| RF12 | Funções | 2 | 2 | 0 | — |
| RF13 | Fornecedores | 2 | 1 | 1 | DW-BUG-017 |
| RF14 | Prospecção | 2 | 2 | 0 | — |
| RF15 | Produtos | 2 | 1 | 1 | DW-BUG-018 |
| RF16 | Grupos musculares | 2 | 2 | 0 | — |
| RF17 | Objetivos | 2 | 0 | 1 | DW-BUG-008 |
| RF18 | Modelos de ficha | 2 | 1 | 1 | DW-BUG-019 (1 bloqueado parcial) |
| RF19 | Grupos de planos | 2 | 2 | 0 | — |
| RF20 | Modelos de contrato | 2 | 1 | 0 | — |
| RF21 | Despesas fixas | 2 | 2 | 0 | — |
| RF22 | Tipos de pagamento | 3 | 1 | 1 | DW-BUG-020 |
| RF23 | Bandeiras | 2 | 0 | 1 | DW-BUG-021 |
| RF24 | Tipos de documento | 2 | 2 | 0 | — |
| RF25 | Caixas | 3 | 2 | 1 | DW-BUG-022 |
| RF26 | Pagar.me | 2 | 2 | 0 | — (somente visualização) |
| RF27 | Atividades | 2 | 2 | 0 | — |
| RF28 | Pontuação | 2 | 2 | 0 | — |
| RF29 | Enquetes | 2 | 1 | 0 | — |
| RF30 | Anamnese (fichas) | 3 | 1 | 1 | DW-BUG-023 |
| RF31 | Modelos anamnese | 2 | 1 | 0 | — |
| RF32 | Categorias anamnese | 2 | 2 | 0 | — |
| RF33 | Perguntas anamnese | 2 | 1 | 0 | — |
| RF34 | Automações | 2 | 2 | 0 | — |
| RF35 | Resultados IA | 2 | 1 | 0 | — |
| RF36 | Aplicativo | 2 | 2 | 0 | — |
| RF37 | Configurações | 2 | 2 | 0 | — |
| RF38 | SifitBox | 2 | 1 | 0 | — |
| RF39 | Dashboard | 2 | 1 | 1 | DW-BUG-024 |
| RF40 | Perfil do cliente | 2 | 2 | 0 | — |

\*Inclui “passou com ressalva” na coluna Passou para leitura rápida; o detalhe está nos cenários e no resumo do topo.

---

## Divisão de trabalho

| Integrante | Foco na execução |
| --- | --- |
| Diego Santos Gonçalves | RF01–RF05, RF09–RF14, RF19–RF26, RF39–RF40; consolidação do relatório de bugs |
| Wallace Gabriel | RF06–RF08, RF15–RF18, RF27–RF38; revisão cruzada dos cenários e do relatório final |

Ambos validaram o README e a coerência entre plano × execução × bugs.

---

## Conclusões

1. Os fluxos de **consulta** (listagens, filtros básicos, navegação) são majoritariamente utilizáveis.
2. Há defeitos **críticos** em validação de formulários (documentos, obrigatoriedade), **totais/cards** e em cadeias dependentes (objetivos → fichas; bandeiras → financeiro).
3. O ambiente MySQL da aula **não** contém o modelo de academia observado na UI; a dupla documentou isso para evitar conclusões falsas de persistência.
4. Recomenda-se priorizar correção dos 12 bugs de severidade Alta antes de novos cadastros em massa no ambiente de aula.

---

## Entregáveis desta pasta

- [1-Analise-de-requisitos.md](1-Analise-de-requisitos.md)
- [2-Plano-de-testes.md](2-Plano-de-testes.md)
- [Cenarios de testes/](Cenarios%20de%20testes/)
- [3-Relatorio-de-Bugs.md](3-Relatorio-de-Bugs.md)
- Este relatório
