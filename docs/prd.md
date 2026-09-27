# StreamList — Product Requirements Document (PRD)

## 1. Identificação

**Projeto:** StreamList — Plataforma de Filmes  
**Aluno:** Elyabe da Silva Batista  
**Tema:** Descoberta, organização e gerenciamento de filmes

---

## 2. Visão Geral

O StreamList é uma aplicação web responsiva voltada para a descoberta, consulta e organização pessoal de filmes.

A plataforma permite que o usuário pesquise filmes, consulte informações detalhadas e organize seus conteúdos em diferentes listas, como filmes que deseja assistir, favoritos e filmes já assistidos.

As informações dos filmes serão obtidas por meio da API pública do TMDB (The Movie Database).

O StreamList possui finalidade informativa e organizacional. A aplicação não oferece reprodução ou streaming de filmes.

---

## 3. Objetivo

O objetivo do StreamList é oferecer uma interface simples, moderna e organizada para que o usuário possa:

- Descobrir filmes;
- Pesquisar filmes;
- Visualizar informações detalhadas;
- Organizar filmes em listas;
- Marcar filmes como favoritos;
- Alterar o status de acompanhamento;
- Avaliar filmes;
- Criar listas personalizadas;
- Filtrar conteúdos.

---

## 4. Público-Alvo

O StreamList é destinado a pessoas que gostam de filmes e desejam organizar seus conteúdos de forma prática.

O público pode utilizar a plataforma para:

- Encontrar novos filmes;
- Consultar informações antes de assistir;
- Manter uma lista de filmes para assistir;
- Registrar filmes já assistidos;
- Criar listas personalizadas;
- Acompanhar suas avaliações e preferências.

---

## 5. Atores

### Usuário

Pessoa que utiliza a aplicação para descobrir, pesquisar, consultar e organizar filmes.

### Sistema

Responsável pelo funcionamento da aplicação, organização dos dados e comunicação com a API TMDB.

### API TMDB

Serviço externo utilizado como fonte de informações sobre os filmes.

---

## 6. Funcionalidades

### 6.1 Descobrir Filmes

O usuário poderá visualizar filmes em destaque, populares, lançamentos e recomendações.

A tela inicial apresentará cards com informações resumidas dos filmes.

---

### 6.2 Pesquisar Filmes

O usuário poderá pesquisar filmes pelo título.

Os resultados serão apresentados em formato de cards.

---

### 6.3 Filtrar Filmes

O usuário poderá utilizar filtros para facilitar a localização de filmes.

Os filtros poderão considerar informações como:

- Gênero;
- Ano;
- Avaliação;
- Status.

---

### 6.4 Visualizar Detalhes

O usuário poderá acessar uma página específica de um filme.

Serão apresentadas informações como:

- Título;
- Pôster;
- Data de lançamento;
- Gêneros;
- Avaliação;
- Sinopse;
- Informações adicionais;
- Filmes relacionados ou semelhantes.

---

### 6.5 Adicionar Filme às Listas

O usuário poderá adicionar filmes às suas listas.

As listas padrão incluem:

- Quero assistir;
- Favoritos;
- Já assistidos.

Também será possível criar listas personalizadas.

---

### 6.6 Alterar Status

O usuário poderá definir o status de acompanhamento de um filme.

Os status disponíveis são:

- Quero assistir;
- Assistindo;
- Assistido.

---

### 6.7 Avaliar Filme

O usuário poderá registrar uma avaliação para os filmes organizados na plataforma.

---

### 6.8 Registrar Filme

O usuário poderá registrar manualmente um filme.

As informações poderão incluir:

- Título;
- Gênero;
- Ano;
- Nota;
- Status;
- Capa.

---

### 6.9 Editar Filme

O usuário poderá editar as informações de um filme previamente registrado.

---

### 6.10 Excluir Filme

O usuário poderá remover um filme de sua organização.

A ação de exclusão deverá possuir confirmação para evitar remoções acidentais.

---

### 6.11 Perfil

O usuário poderá visualizar informações relacionadas à sua organização pessoal de filmes.

O perfil poderá apresentar:

- Nome;
- Avatar;
- Quantidade de filmes favoritos;
- Quantidade de filmes assistidos;
- Quantidade de filmes para assistir;
- Listas criadas;
- Filmes avaliados.

O protótipo não contempla autenticação ou criação de contas.

---

## 7. User Stories

### US01 — Descobrir Filmes

**Como usuário,**  
quero visualizar filmes em destaque e recomendações,  
**para** descobrir novos conteúdos.

---

### US02 — Pesquisar Filme

**Como usuário,**  
quero pesquisar um filme pelo título,  
**para** encontrar rapidamente o conteúdo desejado.

---

### US03 — Visualizar Detalhes

**Como usuário,**  
quero visualizar os detalhes de um filme,  
**para** conhecer suas principais informações antes de organizá-lo.

---

### US04 — Adicionar Filme a uma Lista

**Como usuário,**  
quero adicionar um filme a uma lista,  
**para** organizar os conteúdos de acordo com meu interesse.

---

### US05 — Criar Lista Personalizada

**Como usuário,**  
quero criar listas personalizadas,  
**para** organizar filmes de acordo com meus próprios critérios.

---

### US06 — Alterar Status

**Como usuário,**  
quero alterar o status de um filme,  
**para** indicar se quero assistir, estou assistindo ou já assisti.

---

### US07 — Favoritar Filme

**Como usuário,**  
quero marcar um filme como favorito,  
**para** encontrá-lo facilmente posteriormente.

---

### US08 — Avaliar Filme

**Como usuário,**  
quero avaliar um filme,  
**para** registrar minha opinião sobre o conteúdo.

---

### US09 — Registrar Filme

**Como usuário,**  
quero registrar um filme manualmente,  
**para** adicioná-lo à minha organização.

---

### US10 — Editar Filme

**Como usuário,**  
quero editar as informações de um filme,  
**para** manter meus registros atualizados.

---

### US11 — Excluir Filme

**Como usuário,**  
quero excluir um filme,  
**para** remover conteúdos que não desejo mais manter.

---

### US12 — Filtrar Filmes

**Como usuário,**  
quero filtrar os filmes,  
**para** encontrar conteúdos de acordo com critérios específicos.

---

### US13 — Visualizar Perfil

**Como usuário,**  
quero visualizar minhas informações e estatísticas,  
**para** acompanhar minha organização de filmes.

---

## 8. Dados dos Filmes

Os principais dados utilizados pelo StreamList incluem:

| Campo | Descrição |
|---|---|
| ID | Identificador do filme |
| Título | Nome do filme |
| Sinopse | Descrição da história |
| Pôster | Imagem de divulgação |
| Data de lançamento | Data de lançamento do filme |
| Gêneros | Categorias do filme |
| Nota | Avaliação do filme |
| Status | Estado de acompanhamento |
| Avaliação pessoal | Nota atribuída pelo usuário |

---

## 9. Regras de Negócio

### RN01 — Título obrigatório

Todo filme registrado manualmente deverá possuir um título.

### RN02 — Tipo de conteúdo

O StreamList trabalha exclusivamente com filmes.

Não fazem parte do escopo séries, episódios ou temporadas.

### RN03 — Status

Um filme poderá possuir apenas um dos seguintes status:

- Quero assistir;
- Assistindo;
- Assistido.

### RN04 — Identificação

Cada filme deverá possuir um identificador único para controle interno.

### RN05 — Edição

Filmes registrados pelo usuário poderão ser editados.

### RN06 — Exclusão

Filmes poderão ser excluídos pelo usuário após confirmação da ação.

### RN07 — Avaliação

A avaliação pessoal deverá respeitar o intervalo definido pela aplicação.

### RN08 — Listas

Um filme poderá ser organizado em diferentes listas conforme as ações realizadas pelo usuário.

### RN09 — Pesquisa

A pesquisa deverá considerar o título dos filmes disponíveis.

### RN10 — Filtros

Os filtros deverão ser aplicados sobre os filmes disponíveis na aplicação.

### RN11 — API

As informações externas dos filmes serão obtidas por meio da API pública TMDB.

### RN12 — Streaming

O StreamList não realizará reprodução ou streaming de filmes.

---

## 10. Escopo

### Dentro do escopo

- Descoberta de filmes;
- Pesquisa;
- Filtros;
- Consulta de detalhes;
- Listas;
- Listas personalizadas;
- Favoritos;
- Status;
- Avaliações;
- Registro;
- Edição;
- Exclusão;
- Perfil;
- Interface responsiva;
- Integração com TMDB.

### Fora do escopo

- Séries;
- Episódios;
- Temporadas;
- Streaming;
- Reprodução de filmes;
- Assinaturas;
- Pagamentos;
- Autenticação;
- Cadastro de contas;
- Administração;
- Moderação;
- Comentários públicos;
- Chat;
- Rede social.

---

## 11. Responsividade

A aplicação deverá possuir uma interface responsiva para diferentes dispositivos.

Serão consideradas três principais categorias:

- Mobile;
- Tablet;
- Desktop.

O layout deverá adaptar:

- Navegação;
- Cards;
- Grids;
- Formulários;
- Filtros;
- Informações dos filmes;
- Botões;
- Espaçamentos.

---

## 12. MVP

A primeira versão do StreamList deverá contemplar:

- Descoberta de filmes;
- Pesquisa;
- Visualização de detalhes;
- Listas;
- Favoritos;
- Status;
- Avaliação;
- Registro;
- Edição;
- Exclusão;
- Filtros;
- Perfil;
- Responsividade;
- Integração com TMDB.

---

## 13. Telas do Protótipo

O protótipo contempla as seguintes telas principais:

1. Descobrir;
2. Buscar;
3. Detalhes do Filme;
4. Minhas Listas;
5. Registrar/Editar Filme;
6. Perfil.

Todas as telas devem possuir versões responsivas para Mobile, Tablet e Desktop.

---

## 14. Fluxo Principal

```text
Descobrir
    ↓
Buscar
    ↓
Selecionar Filme
    ↓
Detalhes do Filme
    ↓
Adicionar à Lista
    ↓
Minhas Listas
    ↓
Organizar / Alterar Status
