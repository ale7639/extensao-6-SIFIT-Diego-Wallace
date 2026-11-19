# Schema do MySQL informado na aula

Este arquivo registra a inspeção somente leitura do banco indicado no material da Extensão.

Banco: `u339572246_alfa1`
Host: `srv795.hstgr.io` porta `3306`
Capturado em: 2026-11-19T18:28:59.045Z
Tabelas: 43

O schema não contém tabelas da academia (matrícula, presença, ficha de treino, caixa, avaliação). As tabelas abaixo são de uma loja virtual: produtos, pedidos, banners, artigos, marcas e clientes de e-commerce. A contagem em `clientes` foi 1 registro (maior id 433). No SIFIT, a listagem de alunos mostra códigos acima disso e chama a API `https://backendsifit.centrion.com.br/api/`. A senha de acesso não é versionada neste repositório.

| Tabela | Linhas estimadas | Comentário |
| --- | ---: | --- |
| artigos | 15 |  |
| atributos | 170 |  |
| authentication_methods | 0 |  |
| banners | 9 |  |
| cartoes | 0 |  |
| categorias | 29 |  |
| categoria_artigos | 4 |  |
| cidades | 5585 |  |
| clientes | 1 |  |
| combos | 3 |  |
| configuracoes | 2 |  |
| contatos | 0 |  |
| cupons | 3 |  |
| empresa | 0 |  |
| enderecos | 0 |  |
| estados | 27 |  |
| estoques | 0 |  |
| failed_jobs | 0 |  |
| grupos | 12 |  |
| identity_link_intents | 0 |  |
| imagens_produtos | 0 |  |
| instagram_accounts | 0 |  |
| instagram_posts | 0 |  |
| marcas | 7 |  |
| melhor_envio | 0 |  |
| migrations | 24 |  |
| newsletter | 0 |  |
| paginas | 0 |  |
| parceiros | 4 |  |
| parcelamento | 0 |  |
| password_reset_tokens | 0 |  |
| pedidos | 0 |  |
| perguntas | 0 |  |
| personal_access_tokens | 391 |  |
| produtos | 0 |  |
| produtos_3d | 0 |  |
| produtos_pedidos | 0 |  |
| security_events | 0 |  |
| sessions | 0 |  |
| social_accounts | 0 |  |
| social_auth_codes | 0 |  |
| users | 1 |  |
| valores_variacoes | 0 |  |

## artigos

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | bigint(20) unsigned | NO | PRI | auto_increment |
| categoria_artigo_id | bigint(20) unsigned | YES | MUL |  |
| titulo | varchar(150) | NO |  |  |
| urn | varchar(255) | NO |  |  |
| resumo | varchar(300) | NO |  |  |
| conteudo | longtext | NO |  |  |
| imagem_capa | varchar(255) | YES |  |  |
| status | enum('RASCUNHO','PUBLICADO') | NO |  |  |
| data_publicacao | timestamp | YES |  |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |

Relacionamentos:

- `categoria_artigo_id` → `categoria_artigos.id`

## atributos

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | bigint(20) unsigned | NO | PRI | auto_increment |
| produto_id | bigint(20) unsigned | NO | MUL |  |
| nome | varchar(255) | NO |  |  |
| valor | varchar(255) | NO |  |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |

Relacionamentos:

- `produto_id` → `produtos.id`

## authentication_methods

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | bigint(20) unsigned | NO | PRI | auto_increment |
| account_type | varchar(255) | NO | MUL |  |
| account_id | bigint(20) unsigned | NO |  |  |
| type | varchar(40) | NO |  |  |
| reference | varchar(255) | YES |  |  |
| status | varchar(30) | NO |  |  |
| verified_at | timestamp | YES |  |  |
| last_used_at | timestamp | YES |  |  |
| data | longtext | YES |  |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |

## banners

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | bigint(20) unsigned | NO | PRI | auto_increment |
| categoria | enum('PRINCIPAL','CENTRAL') | NO |  |  |
| ordem | int(10) unsigned | NO |  |  |
| nome | varchar(150) | NO |  |  |
| titulo | varchar(255) | YES |  |  |
| tag | varchar(100) | YES |  |  |
| descricao | text | YES |  |  |
| imagem | varchar(255) | NO |  |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |
| imagem_cel | varchar(255) | NO |  |  |
| url | varchar(255) | YES |  |  |

## cartoes

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | int(11) | NO | PRI | auto_increment |
| cliente_id | bigint(20) unsigned | YES | MUL |  |
| pagarme_id | varchar(255) | YES |  |  |
| created_at | timestamp | NO |  |  |
| updated_at | timestamp | NO |  | on update current_timestamp() |

Relacionamentos:

- `cliente_id` → `clientes.id`

## categorias

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | bigint(20) unsigned | NO | PRI | auto_increment |
| grupo_id | bigint(20) unsigned | NO | MUL |  |
| nome | varchar(80) | NO |  |  |
| urn | varchar(255) | NO |  |  |
| status | enum('ATIVO','INATIVO') | NO |  |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |
| imagem | varchar(255) | YES |  |  |

Relacionamentos:

- `grupo_id` → `grupos.id`

## categoria_artigos

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | bigint(20) unsigned | NO | PRI | auto_increment |
| nome | varchar(80) | NO |  |  |
| urn | varchar(255) | NO |  |  |
| status | enum('ATIVO','INATIVO') | NO |  |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |

## cidades

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | int(10) unsigned | NO | PRI | auto_increment |
| nome | varchar(255) | NO |  |  |
| codigo_ibge | int(11) | NO |  |  |
| estado_id | int(10) unsigned | NO | MUL |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |

Relacionamentos:

- `estado_id` → `estados.id`

## clientes

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | bigint(20) unsigned | NO | PRI | auto_increment |
| nome | varchar(255) | NO |  |  |
| status | varchar(255) | NO |  |  |
| email | varchar(255) | NO | UNI |  |
| cpf | varchar(20) | YES | UNI |  |
| cnpj | varchar(255) | YES | UNI |  |
| tipo_pessoa | enum('FISICA','JURIDICA') | NO |  |  |
| data_nascimento | date | YES |  |  |
| telefone_principal | varchar(20) | YES |  |  |
| telefone_alternativo | varchar(20) | YES |  |  |
| parceiro_id | bigint(20) unsigned | YES | MUL |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |
| password | varchar(255) | YES |  |  |
| password_set_at | timestamp | YES |  |  |
| remember_token | varchar(100) | YES |  |  |
| pagarme_id | varchar(255) | YES |  |  |
| token | varchar(255) | YES |  |  |
| data_admissao | date | YES |  |  |
| avatar | varchar(2048) | YES |  |  |
| avatar_source | varchar(30) | YES |  |  |
| session_version | int(10) unsigned | NO |  |  |

Relacionamentos:

- `parceiro_id` → `parceiros.id`

## combos

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | int(11) | NO | PRI | auto_increment |
| descricao | varchar(255) | NO |  |  |
| produto_1 | bigint(20) unsigned | NO | MUL |  |
| produto_2 | bigint(20) unsigned | NO | MUL |  |
| valor_total | float | YES |  |  |
| destaque | enum('SIM','NAO') | YES |  |  |
| status | enum('ATIVO','INATIVO') | YES |  |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |
| parcelas | int(11) | YES |  |  |

Relacionamentos:

- `produto_1` → `produtos.id`
- `produto_2` → `produtos.id`

## configuracoes

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | bigint(20) unsigned | NO | PRI | auto_increment |
| chave | varchar(100) | NO | UNI |  |
| valor | varchar(255) | YES |  |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |

## contatos

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | bigint(20) unsigned | NO | PRI | auto_increment |
| nome | varchar(255) | NO |  |  |
| email | varchar(255) | NO |  |  |
| telefone | varchar(255) | NO |  |  |
| status | enum('LIDO','NAO_LIDO') | NO |  |  |
| mensagem | text | NO |  |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |

## cupons

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | int(10) unsigned | NO | PRI | auto_increment |
| codigo | varchar(10) | YES |  |  |
| desconto | float | YES |  |  |
| data_inicial | date | YES |  |  |
| validade | date | YES |  |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |
| nome | varchar(200) | NO |  |  |
| status | enum('ATIVO','CANCELADO','VENCIDO') | NO |  |  |
| tipo_desconto | enum('PERCENTUAL','VALOR') | NO |  |  |
| parceiro_id | bigint(20) unsigned | YES | MUL |  |
| valido_apenas_primeira_compra | enum('SIM','NAO') | NO |  |  |

Relacionamentos:

- `parceiro_id` → `parceiros.id`

## empresa

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | bigint(20) unsigned | NO | PRI | auto_increment |
| instagram | varchar(120) | YES |  |  |
| facebook | varchar(120) | YES |  |  |
| endereco | varchar(255) | NO |  |  |
| numero | varchar(10) | NO |  |  |
| cidade_uf | varchar(100) | NO |  |  |
| telefone | varchar(20) | NO |  |  |
| whatsapp | varchar(20) | YES |  |  |
| cep | varchar(20) | NO |  |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |
| meta_descricao | varchar(255) | YES |  |  |
| meta_nome | varchar(255) | YES |  |  |
| twitter | varchar(100) | YES |  |  |
| sobre_nos | text | NO |  |  |
| email | varchar(255) | YES |  |  |
| numero_telefone | varchar(20) | YES |  |  |
| juros | float | YES |  |  |
| texto_resumido | text | NO |  |  |
| bairro | varchar(80) | YES |  |  |

## enderecos

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | bigint(20) unsigned | NO | PRI | auto_increment |
| cliente_id | bigint(20) unsigned | NO | MUL |  |
| cidade_id | bigint(20) unsigned | NO |  |  |
| cep | varchar(20) | NO |  |  |
| logradouro | varchar(255) | NO |  |  |
| numero | varchar(10) | NO |  |  |
| bairro | varchar(255) | NO |  |  |
| complemento | varchar(255) | YES |  |  |
| telefone | varchar(20) | YES |  |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |
| principal | enum('SIM','NAO') | YES |  |  |
| nome | varchar(100) | NO |  |  |

Relacionamentos:

- `cliente_id` → `clientes.id`

## estados

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | int(10) unsigned | NO | PRI | auto_increment |
| nome | varchar(255) | NO |  |  |
| uf | char(2) | NO |  |  |
| codigo_uf | int(11) | NO |  |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |

## estoques

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | bigint(20) unsigned | NO | PRI | auto_increment |
| quantidade | int(11) | NO |  |  |
| quantidade_reservada | int(11) | NO |  |  |
| produto_id | bigint(20) unsigned | NO | MUL |  |
| valor_variacao_id | bigint(20) unsigned | YES | MUL |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |

Relacionamentos:

- `produto_id` → `produtos.id`
- `valor_variacao_id` → `valores_variacoes.id`

## failed_jobs

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | bigint(20) unsigned | NO | PRI | auto_increment |
| uuid | varchar(255) | NO | UNI |  |
| connection | text | NO |  |  |
| queue | text | NO |  |  |
| payload | longtext | NO |  |  |
| exception | longtext | NO |  |  |
| failed_at | timestamp | NO |  |  |

## grupos

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | bigint(20) unsigned | NO | PRI | auto_increment |
| nome | varchar(255) | NO |  |  |
| urn | varchar(255) | NO |  |  |
| status | enum('ATIVO','INATIVO') | NO |  |  |
| destaque1 | enum('SIM','NAO') | NO |  |  |
| destaque2 | enum('SIM','NAO') | NO |  |  |
| imagem | varchar(255) | NO |  |  |
| ordem | int(10) unsigned | NO |  |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |

## identity_link_intents

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | char(36) | NO | PRI |  |
| account_type | varchar(255) | NO | MUL |  |
| account_id | bigint(20) unsigned | NO |  |  |
| provider | varchar(50) | NO |  |  |
| connection_key | varchar(80) | NO |  |  |
| state_hash | varchar(64) | NO |  |  |
| code_challenge | varchar(64) | NO |  |  |
| session_id_hash | varchar(64) | NO |  |  |
| expires_at | timestamp | NO |  |  |
| consumed_at | timestamp | YES |  |  |
| provider_subject | varchar(255) | YES |  |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |

## imagens_produtos

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | bigint(20) unsigned | NO | PRI | auto_increment |
| produto_id | bigint(20) unsigned | NO | MUL |  |
| imagem | varchar(255) | NO |  |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |
| numero | int(11) | YES |  |  |
| imagem_thumb | varchar(255) | YES |  |  |

Relacionamentos:

- `produto_id` → `produtos.id`

## instagram_accounts

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | bigint(20) unsigned | NO | PRI | auto_increment |
| empresa_id | bigint(20) unsigned | YES | MUL |  |
| instagram_user_id | varchar(255) | YES | MUL |  |
| instagram_business_id | varchar(255) | YES | MUL |  |
| facebook_page_id | varchar(255) | YES | MUL |  |
| username | varchar(255) | YES |  |  |
| name | varchar(255) | YES |  |  |
| profile_picture | text | YES |  |  |
| access_token | text | NO |  |  |
| refresh_token | text | YES |  |  |
| expires_at | timestamp | YES |  |  |
| status | varchar(255) | NO | MUL |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |

Relacionamentos:

- `empresa_id` → `empresa.id`

## instagram_posts

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | bigint(20) unsigned | NO | PRI | auto_increment |
| empresa_id | bigint(20) unsigned | YES | MUL |  |
| instagram_post_id | varchar(255) | NO | UNI |  |
| caption | text | YES |  |  |
| media_type | varchar(255) | YES | MUL |  |
| media_url | text | YES |  |  |
| thumbnail_url | text | YES |  |  |
| permalink | text | YES |  |  |
| timestamp | timestamp | YES | MUL |  |
| username | varchar(255) | YES |  |  |
| raw_json | longtext | YES |  |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |

Relacionamentos:

- `empresa_id` → `empresa.id`

## marcas

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | int(11) | NO | PRI | auto_increment |
| nome | varchar(80) | NO |  |  |
| logo | varchar(255) | YES |  |  |
| status | enum('INATIVO','ATIVO') | NO |  |  |
| created_at | timestamp | NO |  |  |
| updated_at | timestamp | NO |  | on update current_timestamp() |

## melhor_envio

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | int(11) | NO | PRI | auto_increment |
| token | text | YES |  |  |
| refresh_token | text | YES |  |  |
| client_id | varchar(45) | YES |  |  |
| client_secret | varchar(45) | YES |  |  |
| redirect_uri | varchar(45) | YES |  |  |
| erro | text | YES |  |  |
| created_at | datetime | YES |  |  |
| updated_at | datetime | YES |  |  |

## migrations

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | int(10) unsigned | NO | PRI | auto_increment |
| migration | varchar(255) | NO |  |  |
| batch | int(11) | NO |  |  |

## newsletter

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | bigint(20) unsigned | NO | PRI | auto_increment |
| email | varchar(255) | YES | UNI |  |
| whatsapp | varchar(255) | YES | UNI |  |
| telefone | varchar(255) | YES |  |  |
| preferencia_contato | varchar(255) | NO |  |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |

## paginas

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | int(11) | NO | PRI | auto_increment |
| nome | varchar(255) | NO |  |  |
| sobre | text | NO |  |  |
| created_at | timestamp | NO |  |  |
| updated_at | timestamp | NO |  | on update current_timestamp() |

## parceiros

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | bigint(20) unsigned | NO | PRI | auto_increment |
| nome | varchar(200) | NO |  |  |
| email | varchar(255) | YES |  |  |
| telefone | varchar(20) | YES |  |  |
| codigo | varchar(20) | YES | UNI |  |
| status | enum('ATIVO','INATIVO') | NO |  |  |
| observacoes | text | YES |  |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |

## parcelamento

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | int(11) | NO | PRI | auto_increment |
| parcelas | int(11) | YES |  |  |
| taxas | float | YES |  |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |

## password_reset_tokens

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| email | varchar(255) | NO | PRI |  |
| token | varchar(255) | NO |  |  |
| created_at | timestamp | YES |  |  |

## pedidos

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | bigint(20) unsigned | NO | PRI | auto_increment |
| codigo_rastreio | varchar(255) | YES |  |  |
| arquivo | varchar(255) | YES |  |  |
| cliente_id | bigint(20) unsigned | NO | MUL |  |
| valor_total | decimal(10,2) | NO |  |  |
| valor_frete | decimal(10,2) | NO |  |  |
| valor_produtos | decimal(10,2) | NO |  |  |
| status | enum('PAGO','PENDENTE','FATURADO','ENVIADO','CANCELADO','ENCERRADO','REJEITADO') | NO |  |  |
| data_envio | datetime | YES |  |  |
| data_faturamento | datetime | YES |  |  |
| data_entrega | datetime | YES |  |  |
| data_cancelamento | datetime | YES |  |  |
| observacao | text | YES |  |  |
| motivo_cancelamento | text | YES |  |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |
| pagarme_id | varchar(255) | YES |  |  |
| tipo_pagamento | enum('BOLETO','CARTAO','PIX') | NO |  |  |
| pix_qr_code | varchar(255) | YES |  |  |
| pix_code | varchar(255) | YES |  |  |
| pdf | varchar(255) | YES |  |  |
| boleto_code | varchar(255) | YES |  |  |
| boleto_qr_code | varchar(255) | YES |  |  |
| cep | varchar(10) | NO |  |  |
| logradouro | varchar(100) | NO |  |  |
| numero | varchar(5) | NO |  |  |
| cidade | varchar(200) | NO |  |  |
| bairro | varchar(60) | NO |  |  |
| complemento | varchar(255) | YES |  |  |
| estado | varchar(10) | NO |  |  |
| estimativa_entrega | int(11) | YES |  |  |
| tipo_frete | varchar(150) | YES |  |  |
| cupom_id | int(10) unsigned | YES | MUL |  |
| parceiro_id | bigint(20) unsigned | YES | MUL |  |

Relacionamentos:

- `cliente_id` → `clientes.id`
- `cupom_id` → `cupons.id`
- `parceiro_id` → `parceiros.id`

## perguntas

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | int(11) | NO | PRI | auto_increment |
| pergunta | varchar(255) | YES |  |  |
| resposta | text | YES |  |  |
| status | enum('ATIVO','INATIVO') | YES |  |  |
| created_at | timestamp | NO |  |  |
| updated_at | timestamp | NO |  | on update current_timestamp() |

## personal_access_tokens

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | bigint(20) unsigned | NO | PRI | auto_increment |
| tokenable_type | varchar(255) | NO | MUL |  |
| tokenable_id | bigint(20) unsigned | NO |  |  |
| name | varchar(255) | NO |  |  |
| token | varchar(64) | NO | UNI |  |
| abilities | text | YES |  |  |
| last_used_at | timestamp | YES |  |  |
| expires_at | timestamp | YES |  |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |

## produtos

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | bigint(20) unsigned | NO | PRI | auto_increment |
| categoria_id | bigint(20) unsigned | NO | MUL |  |
| ref | varchar(45) | NO |  |  |
| nome | varchar(80) | NO |  |  |
| status | enum('ATIVO','INATIVO') | NO |  |  |
| urn | varchar(60) | NO |  |  |
| preco | double(8,2) | NO |  |  |
| preco_pix | double(8,2) | NO |  |  |
| preco_desconto | double(8,2) | YES |  |  |
| parcelas | int(11) | YES |  |  |
| peso | float | YES |  |  |
| destaque1 | enum('SIM','NAO') | NO |  |  |
| destaque2 | enum('SIM','NAO') | NO |  |  |
| destaque3 | enum('SIM','NAO') | NO |  |  |
| mais_vendidos | enum('SIM','NAO') | NO |  |  |
| descricao | longtext | YES |  |  |
| medida_altura | int(11) | YES |  |  |
| medida_largura | int(11) | YES |  |  |
| medida_profundidade | int(11) | YES |  |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |
| ncm | varchar(8) | YES |  |  |
| ean | varchar(14) | YES |  |  |
| marca_id | int(11) | YES | MUL |  |
| tem_desconto | enum('SIM','NAO') | YES |  |  |
| item_unico | enum('SIM','NAO') | YES |  |  |
| peso_embalado | float | YES |  |  |
| altura_embalado | int(11) | YES |  |  |
| largura_embalado | int(11) | YES |  |  |
| profundidade_embalado | int(11) | YES |  |  |
| grupo_id | bigint(20) unsigned | YES |  |  |

Relacionamentos:

- `categoria_id` → `categorias.id`
- `marca_id` → `marcas.id`

## produtos_3d

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | int(11) | NO | PRI | auto_increment |
| arquivo | varchar(255) | YES |  |  |
| tipo | varchar(3) | YES |  |  |
| produto_id | bigint(20) unsigned | YES | MUL |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |

Relacionamentos:

- `produto_id` → `produtos.id`

## produtos_pedidos

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | bigint(20) unsigned | NO | PRI | auto_increment |
| pedido_id | bigint(20) unsigned | NO | MUL |  |
| produto_id | bigint(20) unsigned | NO | MUL |  |
| valor | double(8,2) | NO |  |  |
| estoque_id | bigint(20) unsigned | NO | MUL |  |
| quantidade | int(11) | NO |  |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |

Relacionamentos:

- `estoque_id` → `estoques.id`
- `pedido_id` → `pedidos.id`
- `produto_id` → `produtos.id`

## security_events

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | bigint(20) unsigned | NO | PRI | auto_increment |
| account_type | varchar(255) | YES | MUL |  |
| account_id | bigint(20) unsigned | YES |  |  |
| event | varchar(80) | NO |  |  |
| provider | varchar(50) | YES |  |  |
| ip_address | varchar(45) | YES |  |  |
| user_agent | text | YES |  |  |
| context | longtext | YES |  |  |
| occurred_at | timestamp | NO |  |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |

## sessions

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | varchar(255) | NO | PRI |  |
| user_id | bigint(20) unsigned | YES | MUL |  |
| ip_address | varchar(45) | YES |  |  |
| user_agent | text | YES |  |  |
| payload | longtext | NO |  |  |
| last_activity | int(11) | NO | MUL |  |

## social_accounts

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | bigint(20) unsigned | NO | PRI | auto_increment |
| account_type | varchar(255) | NO | MUL |  |
| account_id | bigint(20) unsigned | NO |  |  |
| provider | varchar(50) | NO | MUL |  |
| connection_key | varchar(80) | NO | MUL |  |
| issuer | varchar(255) | YES |  |  |
| subject | varchar(255) | YES |  |  |
| tenant_id | varchar(255) | YES |  |  |
| provider_id | varchar(255) | NO |  |  |
| email | varchar(255) | YES | MUL |  |
| avatar | varchar(2048) | YES |  |  |
| provider_data | longtext | YES |  |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |
| status | varchar(30) | NO |  |  |
| linked_at | timestamp | YES |  |  |
| last_authenticated_at | timestamp | YES |  |  |
| last_synced_at | timestamp | YES |  |  |
| revoked_at | timestamp | YES |  |  |

## social_auth_codes

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | bigint(20) unsigned | NO | PRI | auto_increment |
| code_hash | varchar(64) | NO | UNI |  |
| account_type | varchar(255) | NO | MUL |  |
| account_id | bigint(20) unsigned | NO |  |  |
| provider | varchar(50) | NO |  |  |
| code_challenge | varchar(64) | NO |  |  |
| session_id_hash | varchar(64) | NO |  |  |
| expires_at | timestamp | NO |  |  |
| consumed_at | timestamp | YES |  |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |

## users

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | bigint(20) unsigned | NO | PRI | auto_increment |
| nome | varchar(255) | NO |  |  |
| email | varchar(255) | NO | UNI |  |
| senha | varchar(255) | NO |  |  |
| status | enum('ATIVO','INATIVO') | NO |  |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |

## valores_variacoes

| Coluna | Tipo | Nulo | Chave | Extra |
| --- | --- | --- | --- | --- |
| id | bigint(20) unsigned | NO | PRI | auto_increment |
| nome | varchar(255) | NO |  |  |
| created_at | timestamp | YES |  |  |
| updated_at | timestamp | YES |  |  |

