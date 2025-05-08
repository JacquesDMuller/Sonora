# Lista de Tarefas - Sonora App

## Fase 1: Integração Principal com API do Spotify e Funcionalidades Essenciais

### Configuração e Autenticação com API do Spotify
- [X] **Tarefa 1.1:** Pesquisar e definir o fluxo de autenticação OAuth 2.0 para a API do Spotify (Client Credentials Flow para acesso geral a dados públicos, Authorization Code Flow se interações específicas do usuário no Spotify forem necessárias no futuro).
- [X] **Tarefa 1.2:** Criar um módulo de serviço no frontend (`src/services/spotifyAPI.js` ou `src/services/spotifyAPI.ts`) para encapsular todas as chamadas à API do Spotify.
- [X] **Tarefa 1.3:** Implementar a obtenção e o refresh de tokens de acesso para a API do Spotify.
- [X] **Tarefa 1.4:** Armazenar de forma segura as credenciais da API (Client ID, Client Secret) - preferencialmente via variáveis de ambiente no backend, se um backend for usado para proxying, ou diretamente no frontend para um app client-side (menos seguro, mas comum para APIs públicas).

### Busca e Catálogo de Músicas (Integrado ao Spotify)
- [X] **Tarefa 2.1:** Implementar funcionalidade de busca na `SearchPage.jsx` para pesquisar álbuns, artistas e músicas usando o endpoint de busca do Spotify.
    - [X] Exibir resultados de forma clara, mostrando capa, nome e artista.
    - [X] Implementar sugestões de busca (autocomplete) conforme o usuário digita.
- [X] **Tarefa 2.2:** Desenvolver a `DetailPage.jsx` para exibir informações detalhadas de um álbum/música obtidas do Spotify:
    - [X] Capa do álbum.
    - [X] Nome do álbum/música.
    - [X] Artista(s).
    - [X] Lista de faixas com duração.
    - [X] Data de lançamento.
    - [X] Popularidade (se disponível).
    - [X] Link direto para ouvir no Spotify ("Abrir no Spotify").
- [ ] **Tarefa 2.3:** Criar/Modificar uma página de artista para exibir:
    - [ ] Nome e imagem do artista (do Spotify).
    - [ ] Discografia principal (top álbuns/singles do Spotify).
    - [ ] Link para o perfil do artista no Spotify.
- [ ] **Tarefa 2.4:** Implementar a funcionalidade "Novos Lançamentos" na `HomePage.jsx` ou em uma seção de descoberta, utilizando o endpoint correspondente da API do Spotify.
- [ ] **Tarefa 2.5:** Implementar a funcionalidade "Explorar por Gênero" utilizando os gêneros disponíveis na API do Spotify.

### Sistema de Review e Avaliação (Vinculado a Itens do Spotify)
- [X] **Tarefa 3.1:** No `DetailPage.jsx` (ou componente dedicado), permitir que usuários registrem uma avaliação por estrelas (0.5 a 5) para um álbum/música (identificado pelo ID do Spotify).
- [X] **Tarefa 3.2:** Permitir que usuários escrevam um review (texto) para o álbum/música.
- [X] **Tarefa 3.3:** Permitir que usuários adicionem a data em que ouviram o álbum/música.
- [X] **Tarefa 3.4:** Definir como e onde os reviews e avaliações serão armazenados (inicialmente pode ser no estado local/contexto do React para prototipagem, mas idealmente em um backend/localStorage para persistência).
- [X] **Tarefa 3.5:** Exibir a média de avaliações da comunidade (se houver backend) ou as avaliações do usuário na página do álbum/música.
### Perfil do Usuário e Listas (Vinculado a Itens do Spotify)
- [X] **Tarefa 4.1:** Na `ProfilePage.jsx`, exibir a lista de álbuns/músicas que o usuário avaliou ou fez review.
- [X] **Tarefa 4.2:** Implementar a funcionalidade "Favoritos": permitir que o usuário marque álbuns/músicas (do Spotify) como favoritos.
    - [X] Exibir a lista de favoritos no perfil do usuário.
- [X] **Tarefa 4.3:** Implementar a funcionalidade "Quero Ouvir" (Watchlist Musical): permitir que o usuário adicione álbuns/músicas (do Spotify) a uma lista de "quero ouvir".
    - [X] Exibir esta lista no perfil do usuário ou na `ListsPage.jsx`.
## Fase 2: Funcionalidades Sociais e Adicionais (Pós-Integração Spotify)

- [ ] **Tarefa 5.1:** Implementar sistema de Tags para reviews.
- [ ] **Tarefa 5.2:** Implementar compartilhamento de reviews em redes sociais (links genéricos).
- [ ] **Tarefa 5.3:** Desenvolver feed de atividades na `HomePage.jsx` (inicialmente com atividades locais do usuário).
- [ ] **Tarefa 5.4:** Implementar estatísticas básicas no perfil do usuário (ex: gêneros mais ouvidos com base nos itens avaliados, média de avaliações).
- [ ] **Tarefa 5.5:** Implementar Diário de Escuta cronológico.
- [ ] **Tarefa 5.6:** (Opcional - Requer Backend) Implementar funcionalidades sociais: seguir usuários, feed personalizado, comentários em reviews, likes, menções.
- [ ] **Tarefa 5.7:** (Opcional) Implementar recomendações básicas (ex: "se você gostou disso, talvez goste daquilo" com base nos dados do Spotify ou localmente).

## Fase 3: Melhorias e Opcionais

- [ ] **Tarefa 6.1:** Revisar e garantir responsividade completa e experiência mobile otimizada.
- [ ] **Tarefa 6.2:** (Opcional) Configurar como Progressive Web App (PWA).
- [ ] **Tarefa 6.3:** (Opcional) Implementar importação/exportação de dados (ex: de/para CSV).
- [ ] **Tarefa 6.4:** Implementar tema claro/escuro (se ainda não existir ou precisar de melhorias).

Este `todo.md` será atualizado conforme o progresso.
