


```md
# StreamList — Architecture & Technical Specification

## 1. Identificação

**Projeto:** StreamList — Plataforma de Filmes  
**Aluno:** Elyabe da Silva Batista

---

## 2. Visão Técnica

O StreamList será uma aplicação web responsiva voltada para descoberta, consulta e organização de filmes.

A aplicação utilizará tecnologias de desenvolvimento front-end e uma API externa para obtenção das informações dos filmes.

A arquitetura será baseada em:

- HTML5;
- CSS3;
- JavaScript ES6+;
- Bootstrap 5;
- TMDB API.

Não será utilizado backend próprio ou banco de dados próprio nesta etapa do projeto.

---

## 3. Arquitetura

A aplicação seguirá uma arquitetura simples baseada em front-end e serviço externo.

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
