# 📄 Product Requirements Document (PRD) - StreamList

## 1. Visão Geral e Objetivo

O **StreamList** é uma aplicação web responsiva para gerenciamento pessoal de filmes e séries.

O objetivo do sistema é permitir que o usuário organize os conteúdos que deseja assistir, está assistindo ou já assistiu, mantendo uma lista pessoal com informações relevantes sobre cada filme ou série.

A aplicação terá como foco uma interface simples e intuitiva, permitindo cadastrar, consultar, editar, excluir e organizar os conteúdos adicionados à lista.

---

## 2. Atores do Sistema

* **Visitante:** Usuário que acessa a aplicação e pode visualizar a página inicial e consultar as informações apresentadas pelo sistema.

* **Usuário:** Pessoa responsável por cadastrar e organizar seus filmes e séries dentro do StreamList.

* **Sistema:** Responsável por armazenar, organizar e apresentar os conteúdos cadastrados pelo usuário.

---

## 3. Histórias de Usuário e Escopo

A seguir estão as principais funcionalidades previstas para o projeto, apresentadas sob a perspectiva do usuário final.

### 🎬 Épico 1: Gerenciamento de Conteúdos

* **US01 - Cadastrar Conteúdo:** Como um usuário, quero cadastrar um filme ou série na minha lista para organizar os conteúdos que pretendo acompanhar.

  * **Critérios de Aceitação:**

    * O título deve ser informado.
    * O tipo do conteúdo deve ser selecionado.
    * O status deve ser informado.
    * O formulário deve impedir o cadastro de informações obrigatórias inválidas ou vazias.

* **US02 - Visualizar Conteúdos:** Como um usuário, quero visualizar os filmes e séries cadastrados para consultar minha lista.

  * **Critérios de Aceitação:**

    * Os conteúdos cadastrados devem ser exibidos em uma listagem.
    * Cada conteúdo deve apresentar suas principais informações.
    * Os conteúdos devem ser apresentados de forma organizada e responsiva.

* **US03 - Editar Conteúdo:** Como um usuário, quero editar um conteúdo cadastrado para corrigir ou atualizar suas informações.

  * **Critérios de Aceitação:**

    * O usuário deve conseguir selecionar um conteúdo existente.
    * As informações atuais devem ser carregadas no formulário.
    * As alterações devem ser salvas no conteúdo correspondente.

* **US04 - Excluir Conteúdo:** Como um usuário, quero excluir um conteúdo da minha lista quando não quiser mais mantê-lo cadastrado.

  * **Critérios de Aceitação:**

    * O usuário deve conseguir selecionar um conteúdo para exclusão.
    * O conteúdo removido não deve continuar aparecendo na listagem.

### 📋 Épico 2: Organização da Lista

* **US05 - Alterar Status:** Como um usuário, quero definir o status de um filme ou série para acompanhar meu progresso.

  * **Critérios de Aceitação:**

    * O conteúdo deve possuir um status.
    * Os status disponíveis devem ser:

      * `Quero assistir`
      * `Assistindo`
      * `Assistido`

* **US06 - Pesquisar Conteúdo:** Como um usuário, quero pesquisar um filme ou série pelo título para encontrar rapidamente um conteúdo específico.

  * **Critérios de Aceitação:**

    * A pesquisa deve considerar o título do conteúdo.
    * A listagem deve apresentar apenas os resultados correspondentes à pesquisa.

* **US07 - Filtrar Conteúdos:** Como um usuário, quero filtrar os conteúdos cadastrados para encontrar itens de acordo com suas características.

  * **Critérios de Aceitação:**

    * Deve ser possível utilizar filtros relacionados aos dados cadastrados.
    * A listagem deve ser atualizada de acordo com os filtros utilizados.

### ⭐ Épico 3: Avaliação dos Conteúdos

* **US08 - Avaliar Conteúdo:** Como um usuário, quero atribuir uma nota a um filme ou série para registrar minha avaliação pessoal.

  * **Critérios de Aceitação:**

    * O conteúdo poderá possuir uma nota.
    * A nota deverá respeitar o intervalo definido pela aplicação.

---

## 4. Dados de um Conteúdo

Cada filme ou série cadastrado no StreamList deverá possuir as seguintes informações:

* **id:** identificador único do conteúdo;
* **título:** nome do filme ou série;
* **tipo:** identifica se o conteúdo é um filme ou uma série;
* **gênero:** gênero principal do conteúdo;
* **ano:** ano de lançamento;
* **nota:** avaliação atribuída pelo usuário;
* **status:** situação atual do conteúdo na lista;
* **capa:** imagem utilizada para representar visualmente o conteúdo.

---

## 5. Regras de Negócio

* **RN01:** Todo conteúdo cadastrado deve possuir um título.

* **RN02:** Todo conteúdo deve possuir um tipo, podendo ser `Filme` ou `Série`.

* **RN03:** Todo conteúdo deve possuir um status.

* **RN04:** O status de um conteúdo deverá ser um dos seguintes:

  * `Quero assistir`
  * `Assistindo`
  * `Assistido`

* **RN05:** Os campos obrigatórios do cadastro devem ser preenchidos corretamente antes que um conteúdo seja registrado.

* **RN06:** Cada conteúdo deve possuir um identificador único.

* **RN07:** Um conteúdo cadastrado poderá ser editado posteriormente.

* **RN08:** Um conteúdo excluído não deverá continuar disponível na listagem.

* **RN09:** A nota atribuída a um conteúdo deverá respeitar o intervalo definido pela aplicação.

* **RN10:** A pesquisa e os filtros devem considerar os conteúdos atualmente cadastrados na lista.

---

## 6. Limites do Escopo

O StreamList terá como foco o gerenciamento pessoal de filmes e séries.

Não fazem parte do escopo inicial do projeto:

* reprodução de filmes ou séries;
* contratação ou gerenciamento de assinaturas de serviços de streaming;
* sistema de pagamento;
* sistema de autenticação de usuários;
* interação social entre usuários;
* avaliações públicas ou comentários de outros usuários.

---

## 7. Objetivo do MVP

A primeira versão do StreamList deverá permitir que o usuário:

1. Cadastre filmes e séries;
2. Visualize os conteúdos cadastrados;
3. Pesquise e filtre a lista;
4. Altere informações dos conteúdos;
5. Exclua conteúdos;
6. Controle o status de acompanhamento;
7. Registre uma avaliação pessoal.

O projeto será desenvolvido progressivamente durante a disciplina, incorporando posteriormente os requisitos técnicos definidos nas demais etapas da avaliação.
