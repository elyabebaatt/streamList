🎬 Especificação Técnica (Tech Spec) - StreamList

Este documento descreve o modelo de dados e as principais tecnologias utilizadas na aplicação StreamList — plataforma para descoberta, organização e gerenciamento de filmes.

1. Modelo de Dados (Diagrama ER)

Abaixo está o Diagrama Entidade-Relacionamento (DER) que representa a estrutura principal do StreamList.

erDiagram
    USUARIO ||--o{ LISTA : "possui"
    LISTA ||--o{ LISTA_FILME : "contém"
    FILME ||--o{ LISTA_FILME : "pertence"

    USUARIO {
        string id PK "Identificador único do usuário"
        string nome "Nome do usuário"
        string email "Endereço de e-mail"
        string senha "Credencial de acesso"
    }

    FILME {
        string id PK "Identificador único do filme"
        string titulo "Título do filme"
        string descricao "Sinopse do filme"
        string poster "URL do pôster"
        string dataLancamento "Data de lançamento"
        number nota "Avaliação do filme"
    }

    LISTA {
        string id PK "Identificador único da lista"
        string usuarioId FK "Usuário responsável pela lista"
        string nome "Nome da lista"
        string descricao "Descrição da lista"
        string dataCriacao "Data de criação da lista"
    }

    LISTA_FILME {
        string listaId PK,FK "Referência à lista"
        string filmeId PK,FK "Referência ao filme"
        string dataAdicao "Data em que o filme foi adicionado"
    }


O Usuário pode possuir diversas Listas, enquanto cada lista pode conter diversos Filmes.

Como um mesmo filme pode aparecer em diferentes listas, é utilizada a entidade intermediária Lista_Filme, responsável por representar o relacionamento muitos-para-muitos entre listas e filmes.

As informações dos filmes podem ser obtidas por meio de uma API externa de filmes, evitando a necessidade de armazenar todo o catálogo de filmes no banco de dados.

2. Dicionário de Dados
Usuário

Responsável por armazenar os dados básicos necessários para identificação e autenticação dos usuários.

id: identificador único do usuário.
nome: nome utilizado pelo usuário.
email: endereço de e-mail utilizado para identificação.
senha: credencial utilizada para autenticação.
Filme

Representa os filmes disponíveis para consulta e organização dentro do StreamList.

id: identificador único do filme.
titulo: título do filme.
descricao: sinopse ou descrição do filme.
poster: endereço da imagem utilizada como pôster.
dataLancamento: data de lançamento do filme.
nota: avaliação ou pontuação atribuída ao filme.
Lista

Representa uma coleção personalizada criada por um usuário.

id: identificador único da lista.
usuarioId: referência ao usuário proprietário da lista.
nome: nome definido para a lista. Exemplos: "Filmes para assistir", "Favoritos" ou "Terror".
descricao: descrição opcional da finalidade da lista.
dataCriacao: data em que a lista foi criada.
Lista_Filme

Entidade responsável por relacionar filmes às listas dos usuários.

listaId: referência à lista em que o filme foi adicionado.
filmeId: referência ao filme adicionado.
dataAdicao: data em que o filme foi inserido na lista.
API de Filmes

Responsável pelo fornecimento das informações do catálogo de filmes utilizado pela aplicação.

Os dados como título, pôster, sinopse, gênero, data de lançamento e avaliações podem ser obtidos por meio de uma API externa de filmes.

Essas informações não precisam necessariamente ser armazenadas integralmente no banco de dados, sendo consultadas conforme a necessidade da aplicação.

3. Versões das Tecnologias
HTML5
CSS3
JavaScript ES6+
Vue.js 3.5.42
Vite 8.2.2
Bootstrap 5.3.8
Pinia 4.0.3
Axios 1.20.0
PHP 8.5.10
MySQL 26.7
Node.js 24.20.0 LTS
NPM 11.19.0
Git 2.55.0
GitHub
The Movie Database (TMDB) API
4. Estrutura Geral

A aplicação será organizada em três partes principais:

StreamList
│
├── Frontend
│   ├── Vue 3
│   ├── Vite
│   ├── Bootstrap 5
│   ├── Pinia
│   └── Axios
│
├── Backend
│   └── PHP
│
└── Banco de Dados
    └── MySQL


O Frontend será responsável pela interface e interação com o usuário.

O Backend será responsável pela lógica da aplicação, autenticação e comunicação com o banco de dados.

O MySQL será responsável pelo armazenamento dos dados persistentes dos usuários e suas listas.

A comunicação entre Frontend e Backend será realizada por meio de requisições HTTP.
