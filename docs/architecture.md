# 🎬 StreamList — Tech Spec

> Especificação técnica da aplicação **StreamList**, uma plataforma web para descoberta, consulta e organização de filmes.

---

## 📋 Sumário

* [Visão Geral](#-visão-geral)
* [Arquitetura](#-arquitetura)
* [Tecnologias](#-tecnologias)
* [API de Filmes](#-api-de-filmes)
* [Modelo de Dados](#-modelo-de-dados)
* [Estrutura do Projeto](#-estrutura-do-projeto)
* [Fluxo da Aplicação](#-fluxo-da-aplicação)

---

# 🎯 Visão Geral

O **StreamList** é uma aplicação web desenvolvida para facilitar a **descoberta e organização de filmes**.

A aplicação permitirá que o usuário:

* 🔎 Pesquise filmes;
* 🎬 Consulte informações sobre filmes;
* ⭐ Visualize avaliações;
* 📝 Consulte sinopses;
* 🖼️ Visualize pôsteres;
* 🎭 Consulte gêneros;
* 📋 Organize filmes de acordo com a proposta da aplicação.

As informações dos filmes serão obtidas através da **The Movie Database (TMDB)**, que será utilizada como fonte externa de dados.

---

# 🏗️ Arquitetura

A aplicação será desenvolvida seguindo uma arquitetura simples, composta pelo **frontend** e por uma **API externa de filmes**.

```text
┌─────────────────────────────┐
│          STREAMLIST         │
│                             │
│          FRONTEND           │
│                             │
│ HTML5                       │
│ CSS3                        │
│ JavaScript                  │
│ Framework CSS               │
└──────────────┬──────────────┘
               │
               │ Requisições HTTP
               ▼
┌─────────────────────────────┐
│          TMDB API           │
│                             │
│ Catálogo de filmes          │
│ Informações dos filmes      │
│ Pôsteres                    │
│ Avaliações                  │
│ Gêneros                     │
└─────────────────────────────┘
```

### Responsabilidades

| Componente        | Responsabilidade                                        |
| ----------------- | ------------------------------------------------------- |
| **Frontend**      | Interface, navegação, exibição e interação com os dados |
| **JavaScript**    | Lógica e comunicação com a API                          |
| **Framework CSS** | Componentes visuais e responsividade                    |
| **TMDB API**      | Fornecimento das informações dos filmes                 |

---

# 🛠️ Tecnologias

O StreamList utilizará somente as seguintes tecnologias:

| Tecnologia        | Utilização                          |
| ----------------- | ----------------------------------- |
| **HTML5**         | Estrutura da aplicação              |
| **CSS3**          | Estilização da interface            |
| **JavaScript**    | Lógica, interações e consumo da API |
| **Framework CSS** | Componentes e responsividade        |
| **TMDB API**      | Fornecimento dos dados dos filmes   |

> **Versões:** serão utilizadas as versões mais recentes e estáveis das tecnologias e do framework CSS escolhidos no momento do desenvolvimento.

---

# 🌐 API de Filmes

O **StreamList** utilizará a **The Movie Database (TMDB)** como fonte principal das informações relacionadas aos filmes.

A API será responsável por fornecer os dados utilizados na interface da aplicação.

## 🎬 Dados utilizados

| Informação             | Utilização                        |
| ---------------------- | --------------------------------- |
| **Título**             | Exibição do nome do filme         |
| **Sinopse**            | Apresentação da história do filme |
| **Pôster**             | Exibição da imagem do filme       |
| **Data de lançamento** | Informação sobre o lançamento     |
| **Avaliação**          | Exibição da nota do filme         |
| **Gêneros**            | Classificação dos filmes          |
| **Identificador**      | Identificação única do filme      |

## 🔄 Funcionamento

O frontend realizará requisições à API do TMDB para obter os dados dos filmes.

```text
Usuário
   │
   │ Pesquisa / interação
   ▼
StreamList
   │
   │ Requisição HTTP
   ▼
TMDB API
   │
   │ Dados do filme
   ▼
StreamList
   │
   │ Renderização
   ▼
Usuário
```

Os dados serão obtidos dinamicamente através da API, não sendo necessário criar um banco de dados próprio para armazenar o catálogo de filmes.

---

# 🗃️ Modelo de Dados

Como o StreamList será desenvolvido como uma aplicação **frontend integrada diretamente à API do TMDB**, não haverá um banco de dados próprio nesta versão do projeto.

Dessa forma, o modelo de dados utilizado pela aplicação será baseado nas informações fornecidas pela API.

## 🎬 Filme

Cada filme será representado pelos principais dados retornados pela TMDB.

| Campo          | Tipo   | Descrição                            |
| -------------- | ------ | ------------------------------------ |
| `id`           | number | Identificador único do filme na TMDB |
| `title`        | string | Título do filme                      |
| `overview`     | string | Sinopse ou descrição                 |
| `poster_path`  | string | Caminho para o pôster                |
| `release_date` | string | Data de lançamento                   |
| `vote_average` | number | Avaliação média do filme             |
| `genre_ids`    | array  | Identificadores dos gêneros          |

### Exemplo conceitual

```text
FILME
│
├── id
├── title
├── overview
├── poster_path
├── release_date
├── vote_average
└── genre_ids
```

> Os nomes dos campos poderão variar conforme os endpoints utilizados da API do TMDB.

---

# 📁 Estrutura do Projeto

A estrutura inicial do projeto será organizada da seguinte forma:

```text
StreamList/
│
├── index.html
│
├── css/
│   └── style.css
│
├── js/
│   └── script.js
│
├── assets/
│   └── imagens/
│
└── README.md
```

A estrutura poderá ser modificada durante o desenvolvimento conforme a necessidade de organização dos arquivos.

---

# 🔄 Fluxo da Aplicação

O funcionamento principal do StreamList seguirá o seguinte fluxo:

```text
              ┌──────────────┐
              │    Usuário   │
              └──────┬───────┘
                     │
                     ▼
              ┌──────────────┐
              │  StreamList  │
              │  Frontend    │
              └──────┬───────┘
                     │
                     │ JavaScript
                     │
                     ▼
              ┌──────────────┐
              │   TMDB API   │
              └──────┬───────┘
                     │
                     │ Dados
                     ▼
              ┌──────────────┐
              │  StreamList  │
              │  Renderiza   │
              │  os filmes   │
              └──────┬───────┘
                     │
                     ▼
              ┌──────────────┐
              │    Usuário   │
              └──────────────┘
```

---

# 📱 Interface e Responsividade

A interface será desenvolvida seguindo uma abordagem **responsiva**, permitindo a utilização da aplicação em diferentes tamanhos de tela.

O framework CSS escolhido será utilizado para auxiliar na construção de:

* 📱 Layouts responsivos;
* 🎬 Cards de filmes;
* 🔘 Botões;
* 🧭 Componentes de navegação;
* 📋 Elementos de organização;
* 🖥️ Adaptação para diferentes dispositivos.

---

# 🔒 Considerações

Nesta versão do projeto:

* Não haverá backend próprio;
* Não haverá banco de dados próprio;
* Não haverá PHP;
* Não haverá framework JavaScript;
* Os dados dos filmes serão obtidos através da TMDB;
* O JavaScript será responsável pela comunicação e manipulação dos dados recebidos;
* O framework CSS será utilizado para auxiliar na construção da interface.

A aplicação poderá futuramente receber novas funcionalidades e uma estrutura de backend caso o escopo do projeto seja expandido.

---

# 📌 Resumo Técnico

```text
                        STREAMLIST

                 ┌───────────────────┐
                 │      FRONTEND     │
                 │                   │
                 │      HTML5        │
                 │       CSS3        │
                 │    JavaScript     │
                 │   Framework CSS   │
                 └─────────┬─────────┘
                           │
                       HTTP / API
                           │
                           ▼
                 ┌───────────────────┐
                 │     TMDB API      │
                 │                   │
                 │ Filmes            │
                 │ Pôsteres          │
                 │ Sinopses          │
                 │ Avaliações        │
                 │ Gêneros           │
                 └───────────────────┘
```

---

## 📄 Documentação Relacionada

| Documento                              | Descrição                         |
| -------------------------------------- | --------------------------------- |
| [`README.md`](../README.md)            | Apresentação geral do projeto     |
| [`PRD.md`](./prd.md)                   | Requisitos e definição do produto |
| [`architecture.md`](./architecture.md) | Arquitetura da aplicação          |
| `tech-spec.md`                         | Especificação técnica do projeto  |

---

**StreamList** — *Organize. Descubra. Assista.* 🎬
