# Extensão QA — SIFIT (dupla Diego–Wallace)

Documentação de testes manuais do **SIFIT — Sistema para Academias**, entrega da **extensão 6 pontos** da disciplina de Qualidade de Software.

Este repositório é a entrega **em dupla**. A estrutura segue o padrão de trabalho de QA visto na turma (análise → plano → cenários CT_RFxx → bugs → relatório), com conteúdo, escopo e autoria próprios da dupla.

## Integrantes

| Nome | RA |
| --- | --- |
| Diego Santos Gonçalves | 14523 |
| Wallace Gabriel | 14542 |

Professor: Adnys Lougan  
Sistema: [https://sifit.centrion.com.br](https://sifit.centrion.com.br)

## Objetivo

- Validar requisitos funcionais do SIFIT em ambiente de aula
- Registrar defeitos com passos e severidade
- Organizar evidências e o relatório final da execução em dupla

## Estrutura

```
SIFIT/
  1-Analise-de-requisitos.md
  2-Plano-de-testes.md
  3-Relatorio-de-Bugs.md
  4-Relatorio-dos-testes.md
  Cenarios de testes/
    CT_RF01_ ... CT_RF40_
```

## Metodologia

- Técnicas: caminho feliz, testes negativos, exploratório, particionamento
- Formato dos cenários: BDD (DADO / QUANDO / ENTÃO)
- Ferramentas: Chrome, DevTools, Markdown, GitHub
- Divisão da dupla: Diego (login, operação, financeiro e relatórios); Wallace (treino, engajamento, anamnese, inteligência e configurações). Ambos revisaram o relatório final.

## Status

- Análise de requisitos
- Plano de testes
- Cenários CT_RF01 a CT_RF40
- Execução e registro de bugs
- Relatório final

## Resultados (resumo)

| Indicador | Valor |
| --- | --- |
| Requisitos funcionais | 40 |
| Casos de teste executados | 96 |
| Passou | 68 |
| Passou com ressalva | 14 |
| Falhou | 12 |
| Bloqueado | 2 |
| Bugs registrados | 24 |

Detalhes em [SIFIT/4-Relatorio-dos-testes.md](SIFIT/4-Relatorio-dos-testes.md) e [SIFIT/3-Relatorio-de-Bugs.md](SIFIT/3-Relatorio-de-Bugs.md).

## Nota sobre o trabalho em grupo

A turma também produziu material de referência em equipe maior. **Esta entrega é da dupla Diego–Wallace para a extensão de 6 pontos**: textos, dados de teste, divisão de papéis, cronograma e relatório foram reescritos pela dupla e não são cópia literal do repositório de cinco integrantes.
