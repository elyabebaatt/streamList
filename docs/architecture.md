# StreamList — Architecture & Technical Specification

## 1. Identificação

**Projeto:** StreamList — Plataforma de Filmes
**Aluno:** Elyabe da Silva Batista
**Tema:** Descoberta, organização e gerenciamento de filmes

---

## 2. Visão Técnica

O StreamList é uma aplicação web responsiva voltada para a descoberta, consulta e organização de filmes.

A aplicação será desenvolvida utilizando tecnologias front-end e uma API externa para obtenção das informações dos filmes.

A arquitetura será baseada em:

* HTML5;
* CSS3;
* JavaScript ES6+;
* Bootstrap 5;
* TMDB API.

Nesta etapa, não será utilizado backend próprio ou banco de dados próprio.

---

## 3. Arquitetura

A aplicação seguirá uma arquitetura baseada em front-end e serviço externo.

```text
┌─────────────────────┐
│       Usuário       │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│   StreamList Web    │
│                     │
│ HTML5               │
│ CSS3                │
│ JavaScript ES6+     │
│ Bootstrap 5         │
└──────────┬──────────┘
           │
           │ Requisições HTTP
           ▼
┌─────────────────────┐
│      TMDB API       │
│                     │
│ Dados dos filmes    │
│ Pôsteres            │
│ Gêneros             │
│ Avaliações          │
│ Sinopses            │
└─────────────────────┘
```

---

## 4. Tecnologias

### HTML5

Utilizado para a estruturação semântica das páginas e dos elementos da aplicação.

### CSS3

Utilizado para personalizações visuais específicas do StreamList e complementação dos estilos fornecidos pelo Bootstrap.

### JavaScript ES6+

Responsável pela lógica da aplicação, interações, manipulação dos dados, filtros e comunicação com a API.

### Bootstrap 5

Framework CSS oficial do projeto.

Será utilizado para:

* Sistema de grid;
* Responsividade;
* Navbar;
* Cards;
* Botões;
* Formulários;
* Modais;
* Badges;
* Dropdowns;
* Outros componentes da interface.

### TMDB API

API externa utilizada como fonte de informações sobre os filmes.

---

## 5. Framework CSS Oficial

O **Bootstrap 5** é o framework CSS oficial do StreamList.

A aplicação utilizará o sistema de grid, breakpoints e componentes disponibilizados pelo framework, juntamente com CSS próprio para personalizações da identidade visual.

### Componentes principais

Os principais componentes previstos no protótipo e na futura implementação são:

* Navbar;
* Card;
* Modal;
* Button;
* Form;
* Badge;
* Dropdown;
* Alert;
* Input Group.

---

## 6. Design System

O StreamList utiliza uma identidade visual chamada **Cinematic Dark Grid**.

O conceito combina uma interface escura com elementos em roxo e detalhes em laranja, criando uma estética relacionada ao universo cinematográfico.

O Design System definido na prototipação deverá ser mantido durante a implementação.

---

## 7. Design Tokens

### 7.1 Paleta de Cores

| Token     | Valor     | Utilização                                        |
| --------- | --------- | ------------------------------------------------- |
| Primary   | `#6C63FF` | Ações principais, destaques e elementos ativos    |
| Secondary | `#222634` | Superfícies e elementos secundários               |
| Tertiary  | `#FFA502` | Destaques complementares e informações de atenção |
| Neutral   | `#0F1117` | Fundo principal                                   |

### Primary

```text
#6C63FF
```

Utilizada principalmente em:

* Botões principais;
* Links;
* Elementos ativos;
* Destaques;
* Ações importantes.

### Secondary

```text
#222634
```

Utilizada principalmente em:

* Cards;
* Superfícies;
* Elementos secundários;
* Áreas de navegação.

### Tertiary

```text
#FFA502
```

Utilizada principalmente em:

* Badges;
* Destaques complementares;
* Informações de atenção;
* Elementos secundários de destaque.

### Neutral

```text
#0F1117
```

Utilizada como fundo principal da aplicação.

---

## 8. Tipografia

A família tipográfica oficial do projeto é:

**Inter**

A tipografia será utilizada em:

* Títulos;
* Subtítulos;
* Textos;
* Botões;
* Labels;
* Menus;
* Informações dos filmes.

A hierarquia tipográfica deverá diferenciar títulos, textos principais e informações secundárias.

---

## 9. Interface

A interface do StreamList utiliza:

* Tema escuro;
* Cards com cantos arredondados;
* Botões arredondados;
* Pôsteres de filmes;
* Badges;
* Tags;
* Campos de formulário;
* Grids;
* Navegação responsiva;
* Elementos de destaque em roxo;
* Detalhes complementares em laranja.

Todos os elementos devem manter consistência visual entre as diferentes telas e tamanhos de dispositivo.

---

## 10. Responsividade

O StreamList será desenvolvido seguindo uma abordagem responsiva.

Os principais dispositivos considerados são:

* Mobile;
* Tablet;
* Desktop.

O layout deverá adaptar:

* Navegação;
* Cards;
* Grids;
* Formulários;
* Filtros;
* Informações dos filmes;
* Botões;
* Espaçamentos.

### Mobile

No Mobile:

* A navegação principal será adaptada para uma barra inferior;
* Cards serão organizados em uma ou duas colunas;
* Formulários serão apresentados principalmente em uma coluna;
* Informações dos filmes serão reorganizadas verticalmente;
* Botões e campos serão dimensionados para interação por toque;
* Não deverá existir rolagem horizontal desnecessária.

### Tablet

No Tablet:

* Cards utilizarão mais colunas;
* Formulários poderão utilizar duas colunas;
* Informações poderão ser posicionadas lado a lado;
* A navegação e os conteúdos serão adaptados ao espaço disponível.

### Desktop

No Desktop:

* Grids utilizarão mais colunas;
* Conteúdos poderão ser apresentados lado a lado;
* A navegação será apresentada de forma mais ampla;
* A área disponível será aproveitada para apresentar mais informações simultaneamente.

---

## 11. Breakpoints

A implementação seguirá a lógica de breakpoints disponibilizada pelo Bootstrap 5:

| Breakpoint | Largura de referência | Utilização           |
| ---------- | --------------------: | -------------------- |
| `xs`       |             `< 576px` | Smartphones pequenos |
| `sm`       |             `≥ 576px` | Smartphones maiores  |
| `md`       |             `≥ 768px` | Tablets              |
| `lg`       |             `≥ 992px` | Notebooks            |
| `xl`       |            `≥ 1200px` | Desktops             |
| `xxl`      |            `≥ 1400px` | Telas grandes        |

Os componentes deverão se adaptar progressivamente conforme a largura disponível.

---

## 12. Navegação

### Mobile

A navegação principal será apresentada na parte inferior da interface, com acesso às principais áreas:

* Descobrir;
* Buscar;
* Minhas Listas;
* Perfil.

### Tablet

A navegação deverá se adaptar à largura disponível, mantendo os principais acessos visíveis e organizados.

### Desktop

A navegação será apresentada por meio de uma Navbar adequada para telas maiores.

---

## 13. API

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

---

## 14. Fluxo da API

O fluxo esperado para consulta dos filmes é:

```text
Usuário
   ↓
Interface StreamList
   ↓
JavaScript
   ↓
Requisição HTTP
   ↓
TMDB API
   ↓
Resposta JSON
   ↓
Tratamento dos dados
   ↓
Exibição dos filmes
```

---

## 15. Dados

O projeto não utilizará banco de dados próprio nesta etapa.

Os dados públicos dos filmes serão obtidos através da API TMDB.

As informações relacionadas à organização pessoal dos filmes serão tratadas conforme a evolução da implementação.

---

## 16. Telas

O protótipo contempla as seguintes áreas principais:

### Descobrir

Tela inicial para descoberta de filmes, contendo destaques, categorias, populares e recomendações.

### Buscar

Tela destinada à pesquisa e filtragem de filmes.

### Detalhes do Filme

Apresenta as informações completas de um filme selecionado.

### Minhas Listas

Permite visualizar e organizar filmes em diferentes listas.

### Registrar/Editar Filme

Área destinada ao registro e edição das informações dos filmes.

### Perfil

Área destinada à visualização de informações e estatísticas relacionadas à organização pessoal dos filmes.

---

## 17. Componentes do Bootstrap

O protótipo foi planejado considerando componentes que posteriormente poderão ser implementados utilizando Bootstrap 5.

### Navbar

Utilizada para navegação entre as principais áreas da aplicação.

### Card

Utilizado principalmente para apresentar filmes, listas e informações resumidas.

### Modal

Utilizado para apresentar ações ou informações sobrepostas à interface principal quando necessário.

### Outros componentes

Também poderão ser utilizados:

* Buttons;
* Forms;
* Badges;
* Dropdowns;
* Alerts;
* Input Groups;
* Containers;
* Rows;
* Columns.

---

## 18. Estrutura do Projeto

A estrutura prevista para a implementação é:

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
    │
    ├── css/
    │
    ├── js/
    │
    └── assets/
```

A estrutura poderá ser ajustada durante a etapa de desenvolvimento conforme a necessidade do projeto.

---

## 19. Responsabilidade das Tecnologias

| Tecnologia      | Responsabilidade                          |
| --------------- | ----------------------------------------- |
| HTML5           | Estrutura da aplicação                    |
| CSS3            | Personalizações visuais                   |
| JavaScript ES6+ | Lógica, interações e manipulação de dados |
| Bootstrap 5     | Componentes e responsividade              |
| TMDB API        | Fornecimento dos dados dos filmes         |

---

## 20. Restrições Técnicas

O projeto não utilizará nesta etapa:

* Vue;
* React;
* Angular;
* Tailwind CSS;
* PHP;
* Backend próprio;
* Banco de dados próprio.

O desenvolvimento será baseado em:

* HTML5;
* CSS3;
* JavaScript ES6+;
* Bootstrap 5;
* TMDB API.

---

## 21. Escopo Técnico

O StreamList será uma aplicação exclusivamente voltada para filmes.

Não fazem parte do escopo técnico:

* Séries;
* Episódios;
* Temporadas;
* Streaming;
* Reprodução de vídeos;
* Pagamentos;
* Assinaturas;
* Autenticação;
* Administração;
* Moderação;
* Rede social.

---

## 22. Segurança e Limitações

Como o projeto utiliza uma API externa, as requisições deverão respeitar as regras de utilização e os limites definidos pelo TMDB.

A aplicação não realizará reprodução de conteúdo audiovisual e não será responsável pelo fornecimento dos filmes.

---

## 23. Fluxo Principal

O fluxo principal da aplicação será:

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
```

Um fluxo alternativo será:

```text
Minhas Listas
    ↓
Selecionar Lista
    ↓
Selecionar Filme
    ↓
Visualizar Detalhes
```

---

## 24. Resumo da Arquitetura

```text
                       STREAMLIST
                           │
             ┌─────────────┴─────────────┐
             │                           │
         FRONT-END                  API EXTERNA
             │                           │
     ┌───────┼────────┐                 │
     │       │        │                 │
   HTML5    CSS3   JavaScript       TMDB API
     │       │        │                 │
     │       │        └───────┐         │
     │       │                │         │
     └───────┴──── Bootstrap 5 ─────────┘
                     │
                     ▼
              Interface Web
                     │
                     ▼
                  Usuário
```

---

## 25. Considerações Finais

A arquitetura do StreamList foi definida para manter o projeto simples, responsivo e adequado à proposta da aplicação.

O Bootstrap 5 será utilizado como base para os componentes e para o sistema de responsividade, enquanto HTML5, CSS3 e JavaScript serão responsáveis pela estrutura, personalização e comportamento da aplicação.

A TMDB API será utilizada como fonte externa dos dados dos filmes.

O Design System definido no protótipo deverá ser mantido durante a implementação, garantindo consistência entre a concepção visual e o produto desenvolvido.
