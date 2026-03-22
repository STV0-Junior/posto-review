# Posto Review

Aplicativo colaborativo para motoristas encontrarem, cadastrarem e avaliarem postos de combustivel com base em experiencias reais de abastecimento.

## Visao do Projeto

A proposta do Posto Review e criar uma rede de confianca onde qualquer usuario possa:

- localizar postos proximos em um mapa;
- cadastrar postos que ainda nao existem na base;
- avaliar a qualidade do combustivel, atendimento e preco;
- consultar opinioes de outros motoristas antes de abastecer.

O foco principal nao e apenas mostrar onde abastecer, mas ajudar o usuario a tomar uma decisao melhor com base na reputacao real de cada posto.

## Problema que o App Resolve

Muitos motoristas escolhem postos sem ter referencia confiavel sobre:

- qualidade do combustivel;
- atendimento;
- preco praticado;
- seguranca para abastecer em locais desconhecidos;
- experiencia de outros usuarios em viagens.

O app tenta resolver isso com uma base colaborativa de avaliacoes geolocalizadas.

## Objetivo do MVP

Entregar uma primeira versao funcional onde o usuario consiga:

1. criar conta e fazer login;
2. visualizar postos no mapa;
3. cadastrar um novo posto;
4. avaliar um posto com nota e comentario;
5. consultar a media das avaliacoes;
6. visualizar informacoes basicas do posto.

## Funcionalidades Principais

### 1. Mapa Interativo

- exibicao de postos proximos com base na localizacao atual;
- marcadores no mapa com resumo da avaliacao;
- abertura do detalhe do posto ao tocar no marcador.

### 2. Cadastro de Postos

- nome do posto;
- endereco ou coordenadas;
- bandeira, se houver;
- fotos opcionais;
- observacoes adicionais.

### 3. Avaliacoes

- nota de 1 a 5;
- comentario textual;
- criterio de avaliacao por qualidade, preco e atendimento;
- media geral por posto.

### 4. Autenticacao

- cadastro de usuario;
- login;
- associacao das avaliacoes ao perfil do usuario.

### 5. Moderacao Basica

- denuncia de conteudo inadequado;
- identificacao de posto duplicado;
- revisao futura por administradores.

## Diferenciais da Ideia

- foco em confianca comunitaria;
- utilidade real para motoristas em viagens;
- crescimento organico da base por contribuicao dos usuarios;
- possibilidade futura de reputacao por usuario e ranking de postos.

## Stack Sugerida

Esta e uma trilha tecnica inicial. Pode ser ajustada conforme o escopo e o tempo disponivel.

| Camada | Sugestao | Motivo |
| --- | --- | --- |
| App mobile | React Native com Expo | Rapido para iniciar, bom ecossistema e entrega Android/iOS |
| Backend | Node.js com Express ou Fastify | API simples, boa produtividade e integracao facil |
| Banco | PostgreSQL com PostGIS | Ideal para consultas geograficas |
| Autenticacao | Firebase Auth ou JWT proprio | Implementacao mais rapida no inicio |
| Mapas | Google Maps | Boa documentacao e suporte no mobile |
| Armazenamento de imagens | Firebase Storage ou S3 | Upload simples e escalavel |

## Estrutura Inicial do Produto

Uma possivel divisao de modulos:

```text
mobile/
backend/
database/
docs/
```

Sugestao de responsabilidade:

- `mobile/`: app React Native;
- `backend/`: API, autenticacao e regras de negocio;
- `database/`: scripts e modelos do banco;
- `docs/`: wireframes, decisoes e backlog.

## Fluxo de Uso Esperado

1. O usuario abre o app e permite acesso a localizacao.
2. O mapa mostra postos proximos.
3. O usuario escolhe um posto existente ou cadastra um novo.
4. Depois do abastecimento, ele envia uma nota e um comentario.
5. O sistema atualiza a media do posto.
6. Outros motoristas consultam essas informacoes antes de abastecer.

## Modelo de Dados Basico

### Usuario

- id
- nome
- email
- senha ou provedor de autenticacao
- data_criacao

### Posto

- id
- nome
- bandeira
- endereco
- latitude
- longitude
- fotos
- data_criacao

### Avaliacao

- id
- usuario_id
- posto_id
- nota_geral
- nota_combustivel
- nota_atendimento
- nota_preco
- comentario
- data_criacao

## Roadmap Sugerido

### Fase 1

- definicao do escopo;
- prototipo de telas;
- configuracao do repositorio;
- escolha final da stack.

### Fase 2

- autenticacao;
- mapa com geolocalizacao;
- listagem e detalhe de postos.

### Fase 3

- cadastro de postos;
- envio de avaliacoes;
- exibicao de media por posto.

### Fase 4

- upload de fotos;
- moderacao;
- melhoria de busca e filtros.

## Proximos Passos Praticos

Se a ideia for sair do conceito e ir para construcao, a sequencia recomendada e:

1. fechar a stack oficial do projeto;
2. desenhar as telas principais;
3. modelar o banco de dados;
4. criar o backend com as entidades principais;
5. iniciar o app mobile com autenticacao e mapa;
6. integrar cadastro e avaliacoes.

## Possiveis Evolucoes Futuras

- filtros por nota, preco ou bandeira;
- favoritos;
- ranking de melhores postos por regiao;
- reputacao de usuarios;
- historico de abastecimentos;
- alertas de posto suspeito;
- integracao com rotas de viagem.

## Status

Projeto em fase de definicao e documentacao inicial.

## Observacao

Este README serve como base de direcionamento do produto. Conforme o projeto evoluir, o ideal e complementar este arquivo com:

- instrucoes de instalacao;
- como rodar mobile e backend;
- variaveis de ambiente;
- padrao de contribuicao;
- arquitetura definitiva.
