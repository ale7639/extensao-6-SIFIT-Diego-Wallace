# Análise de requisitos funcionais — SIFIT

**Entrega:** extensão 6 pontos (dupla)  
**Autores:** Diego Santos Gonçalves (14523) e Wallace Gabriel (14542)  
**Sistema:** SIFIT — Sistema para Academias  
**Ambiente:** https://sifit.centrion.com.br  
**Levantamento:** novembro/2026

Os requisitos abaixo foram derivados da exploração das telas do ambiente de aula. Cada RF alimenta os cenários `CT_RFxx` desta pasta.

---

## RF01 — Autenticação

O sistema deve autenticar o usuário com login e senha, rejeitar credenciais inválidas com mensagem clara e respeitar a opção **Manter conectado** quando marcada.

---

## RF02 — Página inicial

Após o login, a home deve apresentar saudação, filtros de período e indicadores (clientes ativos/ausentes, matrículas, desistências, valores em aberto), além de navegação pelo menu lateral.

---

## RF03 — Clientes

Permitir listar, filtrar e cadastrar alunos. Campos mínimos esperados no cadastro: nome, status, sexo e data de nascimento. Deve ser possível abrir o perfil do cliente.

---

## RF04 — Matrículas

Permitir vincular cliente a plano, com modalidade, datas, tipo de pagamento e cálculo de valores. A lista deve exibir cliente, plano e status.

---

## RF05 — Planos

Cadastrar e consultar planos (valor, periodicidade, status e quantidade de alunos). Exibir ranking dos planos com mais alunos.

---

## RF06 — Avaliações físicas

Agendar e listar avaliações com aluno, personal, data/hora e status (Pendente/Realizado).

---

## RF07 — Fichas de treino

Montar fichas por aluno/personal/objetivo, usando biblioteca de exercícios organizada por grupo muscular.

---

## RF08 — Turmas e check-in

Organizar turmas (nome, horário, dias) e registrar presença/check-in, com consulta por período.

---

## RF09 — Financeiro

Controlar contas a receber e a pagar, com filtros por data/status e totais do período.

---

## RF10 — Relatórios

Gerar relatórios (clientes, matrículas, contas etc.) com intervalo de datas e download/visualização.

---

## RF11 — Colaboradores

Cadastrar equipe (nome, status, login). Exibir totais de cadastrados, ativos e personais.

---

## RF12 — Funções

Cadastrar funções (interno/externo, personal, avaliador) e filtrar a listagem.

---

## RF13 — Fornecedores

Cadastrar e buscar fornecedores por código/nome/status.

---

## RF14 — Prospecção

Acompanhar leads por estágio (novo contato, interessado, aula experimental, proposta, fechado).

---

## RF15 — Produtos

Cadastrar produtos de venda ou pontuação, com filtros por tipo e status.

---

## RF16 — Grupos musculares

Consultar grupos (superiores, inferiores, aeróbio) com paginação e filtros.

---

## RF17 — Objetivos de treino

Cadastrar objetivos usados nas fichas de treino.

---

## RF18 — Modelos de ficha

Consultar modelos reutilizáveis ao criar fichas de treino.

---

## RF19 — Grupos de planos

Agrupar planos (descrição, status, exibição na home, tipo de caixa).

---

## RF20 — Modelos de contrato

Cadastrar e listar modelos de contrato da academia.

---

## RF21 — Despesas fixas

Cadastrar despesas recorrentes e visualizar total listado.

---

## RF22 — Tipos de pagamento

Cadastrar formas de pagamento (débito/crédito) com status ativo/inativo.

---

## RF23 — Bandeiras de cartão

Cadastrar e listar bandeiras aceitas.

---

## RF24 — Tipos de documento

Cadastrar tipos usados em contas, fornecedores ou colaboradores.

---

## RF25 — Caixas

Abrir/fechar caixas, filtrar por período e status (aberto/fechado).

---

## RF26 — Pagar.me

Exibir painel de recebimentos da integração (saldo, gráficos, transações). Sem executar saques reais no escopo desta extensão.

---

## RF27 — Atividades

Cadastrar atividades que geram pontos para alunos.

---

## RF28 — Pontuação

Criar campanhas de pontuação (mensal/período) com status.

---

## RF29 — Enquetes

Criar e listar enquetes, com cards de ativas/inativas e respostas.

---

## RF30 — Fichas de anamnese

Aplicar questionários de saúde a alunos e acompanhar status.

---

## RF31 — Modelos de anamnese

Montar modelos com perguntas e preview.

---

## RF32 — Categorias de anamnese

Organizar perguntas em categorias.

---

## RF33 — Perguntas de anamnese

Cadastrar perguntas usadas nos modelos.

---

## RF34 — Inteligência e automação

Listar automações (risco de evasão, aniversariantes etc.) com frequência e última execução.

---

## RF35 — Resultados da inteligência

Exibir cards e histórico do que as automações identificaram, com filtro de período.

---

## RF36 — Aplicativo

Gerir comunicação com alunos (notificações, posts e denúncias) no painel web. App mobile fora do escopo de execução.

---

## RF37 — Configurações

Ajustar parâmetros da academia (home, biometria, avaliação, pagamento, integrações, design).

---

## RF38 — SifitBox

Quando a academia estiver marcada como Box, gerenciar aulas/turmas/categorias de crossfit.

---

## RF39 — Dashboard

Exibir gráficos gerenciais e blocos da Inteligência Sifit.

---

## RF40 — Perfil do cliente

Mostrar visão consolidada do aluno (dados, risco, matrícula, presenças, financeiro e ações rápidas).

---

## Fora do escopo desta análise (execução)

- Pagamentos/saques reais via Pagar.me
- App nativo do aluno em celular
- Envio real de WhatsApp
- Testes de performance/carga
- Alteração destrutiva em massa no ambiente compartilhado da turma
