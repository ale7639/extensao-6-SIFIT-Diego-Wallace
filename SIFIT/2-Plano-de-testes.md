# Plano de testes — SIFIT (dupla Diego–Wallace)

## 1. Identificação

| Campo | Conteúdo |
| --- | --- |
| Projeto | SIFIT — Sistema para Academias |
| Entrega | Extensão 6 pontos (trabalho em dupla) |
| Ambiente | https://sifit.centrion.com.br |
| Tipo | Teste funcional manual |
| Data do plano | 10/11/2026 |
| Responsáveis | Diego Santos Gonçalves (14523); Wallace Gabriel (14542) |

## 2. Objetivo

Verificar os fluxos críticos da academia no SIFIT (autenticação, alunos, matrículas, financeiro, treino, anamnese e indicadores), documentando falhas de validação, inconsistências de interface e problemas de integridade das informações.

## 3. Escopo

### Incluído

- RF01 a RF40 descritos na análise de requisitos
- Testes positivos, negativos e exploratórios em Chrome (Windows 11)
- Registro de bugs com passos e severidade
- Consulta somente leitura no MySQL de aula (`SHOW` / `information_schema` / `SELECT`), sem `INSERT`/`UPDATE`/`DELETE`

### Excluído

- Saques e cobranças reais na Pagar.me
- Aplicativo mobile do aluno
- Disparo real de WhatsApp
- Performance, segurança ofensiva e automação E2E

### Observação de escopo da dupla

Esta entrega cobre a mesma superfície funcional do sistema vista na turma, porém com **execução, redação e critérios de prioridade da dupla**. Cadastros de teste usam o prefixo `DW-` (Diego–Wallace) para não misturar com dados de outros grupos.

## 4. Ferramentas

- Google Chrome
- DevTools (rede e console)
- Markdown + GitHub
- MySQL Workbench (leitura)

## 5. Técnicas

- Particionamento de equivalência
- Análise de valor limite
- Happy path
- Testes negativos
- Exploratório guiado por menu

## 6. Critérios de aceitação

- Resultado obtido alinhado ao esperado do caso
- Mensagens de erro compreensíveis e consistentes
- Listagens e cards coerentes entre telas relacionadas

## 7. Critérios de saída

- Todos os casos do escopo executados ou justificados como bloqueados
- Bugs abertos documentados
- Relatório final publicado neste repositório

## 8. Cronograma

| Atividade | Início | Fim | Responsável |
| --- | --- | --- | --- |
| Análise de requisitos | 05/11/2026 | 09/11/2026 | Diego + Wallace |
| Plano e cenários | 10/11/2026 | 14/11/2026 | Diego + Wallace |
| Execução (operação/financeiro) | 15/11/2026 | 18/11/2026 | Diego |
| Execução (treino/anamnese/IA) | 15/11/2026 | 18/11/2026 | Wallace |
| Bugs e relatório final | 18/11/2026 | 19/11/2026 | Diego + Wallace |

## 9. Módulos e prioridade

| RF | Módulo | Prioridade | Executor principal |
| --- | --- | --- | --- |
| RF01 | Login | Alta | Diego |
| RF02 | Página inicial | Alta | Diego |
| RF03 | Clientes | Alta | Diego |
| RF04 | Matrículas | Alta | Diego |
| RF05 | Planos | Alta | Diego |
| RF06 | Avaliações | Média | Wallace |
| RF07 | Fichas de treino | Alta | Wallace |
| RF08 | Turmas e check-in | Alta | Wallace |
| RF09 | Financeiro | Alta | Diego |
| RF10 | Relatórios | Média | Diego |
| RF11 | Colaboradores | Média | Diego |
| RF12 | Funções | Baixa | Diego |
| RF13 | Fornecedores | Baixa | Diego |
| RF14 | Prospecção | Média | Diego |
| RF15 | Produtos | Baixa | Wallace |
| RF16 | Grupos musculares | Baixa | Wallace |
| RF17 | Objetivos de treino | Alta | Wallace |
| RF18 | Modelos de ficha | Média | Wallace |
| RF19 | Grupos de planos | Baixa | Diego |
| RF20 | Modelos de contrato | Média | Diego |
| RF21 | Despesas fixas | Média | Diego |
| RF22 | Tipos de pagamento | Alta | Diego |
| RF23 | Bandeiras | Média | Diego |
| RF24 | Tipos de documento | Baixa | Diego |
| RF25 | Caixas | Alta | Diego |
| RF26 | Pagar.me | Média | Diego |
| RF27 | Atividades | Baixa | Wallace |
| RF28 | Pontuação | Baixa | Wallace |
| RF29 | Enquetes | Média | Wallace |
| RF30 | Anamnese (fichas) | Alta | Wallace |
| RF31 | Modelos de anamnese | Média | Wallace |
| RF32 | Categorias de anamnese | Baixa | Wallace |
| RF33 | Perguntas de anamnese | Média | Wallace |
| RF34 | Automações | Média | Wallace |
| RF35 | Resultados IA | Média | Wallace |
| RF36 | Aplicativo (web) | Baixa | Wallace |
| RF37 | Configurações | Média | Wallace |
| RF38 | SifitBox | Baixa | Wallace |
| RF39 | Dashboard | Média | Diego |
| RF40 | Perfil do cliente | Alta | Diego |

## 10. Gestão de defeitos

Cada bug registra: ID, título, severidade, passos, esperado × obtido, ambiente, caso relacionado e status.

Severidades: **Alta** (impede fluxo crítico), **Média** (comportamento incorreto contornável), **Baixa** (cosmético ou baixa frequência).

## 11. Riscos

| Risco | Impacto | Mitigação |
| --- | --- | --- |
| Ambiente compartilhado alterado por outros alunos | Médio | Prefixo `DW-` e reexecução rápida |
| Indisponibilidade do SIFIT | Alto | Reagendar janela e registrar bloqueio |
| Um único perfil de administrador | Médio | Declarar limitação no relatório |

## 12. Entregáveis

1. Análise de requisitos
2. Plano de testes
3. Cenários CT_RF01–CT_RF40
4. Relatório de bugs
5. Relatório final de execução
