# 🎬 StreamList — Plataforma de Filmes

## 👤 Identificação

**Aluno:** Elyabe da Silva Batista
**Projeto:** StreamList — Plataforma de Filmes
**Tema:** Descoberta, organização e gerenciamento de filmes

---

## 📖 Sobre o Projeto

O **StreamList** é uma aplicação web responsiva desenvolvida para auxiliar na **descoberta, consulta e organização de filmes**.

A plataforma permite pesquisar filmes, visualizar informações detalhadas e organizar conteúdos em diferentes listas, como:

* 🎬 Quero assistir
* ❤️ Favoritos
* ✅ Já assistidos
* 📁 Listas personalizadas

O projeto possui finalidade **informativa e organizacional**, não oferecendo streaming ou reprodução de filmes.

As informações dos filmes serão obtidas através da **API pública do TMDB (The Movie Database)**.

---

## 🎯 Objetivo

O objetivo do StreamList é proporcionar uma experiência simples e organizada para que o usuário possa:

* Descobrir novos filmes;
* Pesquisar filmes;
* Visualizar informações detalhadas;
* Organizar filmes em listas;
* Criar listas personalizadas;
* Marcar filmes como favoritos;
* Alterar o status dos filmes;
* Avaliar filmes;
* Filtrar conteúdos.

---

## 🧩 Escopo

### Funcionalidades

* 🔎 Pesquisa de filmes
* 🎬 Visualização de detalhes
* 📚 Organização em listas
* ❤️ Favoritos
* ⭐ Avaliação
* 🔄 Alteração de status
* 📁 Listas personalizadas
* 📝 Registro de filmes
* ✏️ Edição de filmes
* 🗑️ Exclusão de filmes
* 🔍 Filtros
* 👤 Perfil
* 📱 Interface responsiva

### Fora do escopo

* Séries
* Episódios
* Temporadas
* Streaming
* Reprodução de filmes
* Assinaturas
* Pagamentos
* Autenticação
* Administração
* Moderação
* Comentários públicos
* Chat
* Rede social

---

## 🛠️ Tecnologias

| Tecnologia          | Utilização                                  |
| ------------------- | ------------------------------------------- |
| **HTML5**           | Estrutura da aplicação                      |
| **CSS3**            | Personalizações visuais                     |
| **JavaScript ES6+** | Lógica e interatividade                     |
| **Bootstrap 5**     | Framework CSS, componentes e responsividade |
| **TMDB API**        | Dados dos filmes                            |

---

## 🅱️ Bootstrap 5

O **Bootstrap 5** é o framework CSS oficial utilizado como base para a interface do StreamList.

Ele será utilizado principalmente para:

* Sistema de grid;
* Responsividade;
* Navbar;
* Cards;
* Modais;
* Botões;
* Formulários;
* Badges;
* Dropdowns.

### Componentes destacados no protótipo

* **Navbar**
* **Card**
* **Modal**

O CSS próprio do projeto será utilizado para complementar e personalizar a identidade visual.

---

## 🎨 Design System

O StreamList utiliza uma identidade visual chamada **Cinematic Dark Grid**, baseada em uma interface escura com elementos em roxo e detalhes em laranja.

### 🎨 Paleta de Cores

| Token         | Valor     | Utilização                          |
| ------------- | --------- | ----------------------------------- |
| **Primary**   | `#6C63FF` | Ações e destaques principais        |
| **Secondary** | `#222634` | Superfícies e elementos secundários |
| **Tertiary**  | `#FFA502` | Destaques complementares            |
| **Neutral**   | `#0F1117` | Fundo principal                     |

### 🔤 Tipografia

**Inter**

Utilizada em títulos, textos, botões, menus e demais elementos da interface.

---

## 📱 Responsividade

O StreamList foi projetado para funcionar em diferentes tamanhos de tela:

* 📱 **Mobile**
* 📲 **Tablet**
* 🖥️ **Desktop**

A interface adapta elementos como:

* Navegação;
* Cards;
* Grids;
* Formulários;
* Filtros;
* Informações dos filmes;
* Botões;
* Espaçamentos.

A responsividade será implementada utilizando o sistema de breakpoints do **Bootstrap 5**.

---

## 🔌 API

### TMDB — The Movie Database

O StreamList utilizará a API pública do TMDB como fonte de informações dos filmes.

Os dados utilizados poderão incluir:

* ID;
* Título;
* Sinopse;
* Pôster;
* Data de lançamento;
* Gêneros;
* Avaliação;
* Informações relacionadas.

### Fluxo

```text
Usuário
   ↓
StreamList
   ↓
JavaScript
   ↓
TMDB API
   ↓
Dados dos filmes
   ↓
Interface
```

---

## 🎨 Protótipo

O protótipo do StreamList foi desenvolvido no **Google Stitch**.

A aplicação possui versões responsivas para:

* Mobile;
* Tablet;
* Desktop.

### Telas principais

* 🏠 Descobrir
* 🔎 Buscar
* 🎬 Detalhes do Filme
* 📚 Minhas Listas
* 📝 Registrar/Editar Filme
* 👤 Perfil

### Fluxo principal

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
```

---

## 📚 Documentação

A documentação do projeto está disponível na pasta `docs/`.

### PRD — Product Requirements Document

Documento responsável pela definição do produto, contendo:

* Objetivo;
* Público-alvo;
* Funcionalidades;
* User Stories;
* Regras de negócio;
* Escopo;
* MVP.

→ [`docs/prd.md`](docs/prd.md)

### Architecture — Technical Specification

Documento responsável pela especificação técnica do projeto, contendo:

* Arquitetura;
* Tecnologias;
* Bootstrap 5;
* TMDB API;
* Design System;
* Design Tokens;
* Responsividade;
* Componentes;
* Estrutura do projeto.

→ [`docs/architecture.md`](docs/architecture.md)

---

## 📁 Estrutura do Projeto

```text
StreamList/
│
├── docs/
│   ├── prd.md
│   └── architecture.md
│
├── README.md
│
└── src/
    ├── index.html
    ├── css/
    ├── js/
    └── assets/
```

A estrutura de implementação poderá ser ajustada durante a próxima etapa do projeto.

---

## 🚧 Status do Projeto

### 1ª Entrega — Concepção, Prototipação e Documentação

* [x] Definição do tema
* [x] Definição do escopo
* [x] Criação do repositório
* [x] Criação do PRD
* [x] Criação da especificação técnica
* [x] Definição da API
* [x] Definição do Bootstrap 5
* [x] Definição do Design System
* [x] Definição da paleta de cores
* [x] Definição da tipografia
* [x] Criação do protótipo
* [x] Protótipo Mobile
* [x] Protótipo Tablet
* [x] Protótipo Desktop
* [x] Responsividade
* [x] Navegação entre telas
* [x] Identificação dos componentes Bootstrap
* [ ] Gravação do vídeo de apresentação
* [ ] Entrega no Moodle

---

## 🎥 Apresentação

A apresentação da primeira entrega deverá demonstrar:

### GitHub

* Repositório público;
* PRD;
* Architecture;
* Tema;
* API utilizada;
* Bootstrap 5.

### Protótipo

* Versão Mobile;
* Versão Tablet;
* Versão Desktop;
* Navegação;
* Fluxo principal;
* Design System;
* Paleta de cores;
* Tipografia;
* Componentes Bootstrap.

### Vídeo

O vídeo de apresentação será disponibilizado como **não listado no YouTube** para a entrega da atividade.

---


