# Plano de Estudos Acelerado para Desenvolvedor Full-Stack

Este plano foi desenhado para te levar do conhecimento intermediário em JavaScript a um nível júnior competitivo no mercado, com foco em projetos práticos e tecnologias em alta demanda.

## Fase 1: Fundamentos Avançados e Ferramentas Essenciais

O objetivo aqui é solidificar a base que todo desenvolvedor Full-Stack precisa, independentemente da tecnologia.

### Git e GitHub (Controle de Versão)

- [x] Entender a diferença entre Git e GitHub.
- [x] Dominar o fluxo básico: `git init`, `git add`, `git commit`, `git status`.
- [x] Trabalhar com branches: `git branch`, `git checkout`, `git merge`.
- [x] Resolver conflitos de merge.
- [x] Conectar um repositório local a um remoto: `git remote add`, `git push`, `git pull`.
- [x] Criar Pull Requests (PRs) no GitHub.
- [ ] Escrever boas mensagens de commit (Conventional Commits).

#### Projetos Práticos de Git:

1.  **Básico:** Crie um repositório para o seu portfólio. Adicione os arquivos do seu site (HTML/CSS/JS), faça commits para cada seção adicionada (ex: "feat: add header section") e suba para o GitHub.
2.  **Intermediário:** Crie um novo branch chamado `develop`. Crie um outro branch a partir do `develop` chamado `feature/add-contact-form`. Implemente um formulário de contato nessa feature branch, faça commits, e depois faça o merge para `develop` via Pull Request no GitHub.
3.  **Avançado:** Convide um colega para colaborar no projeto do portfólio. Peça para ele criar uma nova feature em um branch separado. Simule um conflito de merge (ambos alterando a mesma linha de código) e resolva-o localmente antes de completar o merge.

---

## Fase 2: Dominando o Frontend com React.js

React é a biblioteca mais pedida para frontend. Dominá-la é crucial.

### React: Do Básico ao Avançado

- [x] **Setup e Fundamentos:**
    - [x] Entender o que é React e a Virtual DOM.
    - [x] Configurar um projeto com Vite (ferramenta moderna e rápida).
    - [x] Entender JSX e sua sintaxe.
    - [x] Criar componentes funcionais.
    - [x] Entender a diferença entre Props e State.
- [x] **Hooks Essenciais:**
    - [x] `useState`: Gerenciar o estado local do componente.
    - [x] `useEffect`: Lidar com efeitos colaterais (chamadas de API, manipulação do DOM).
    - [ ] `useContext`: Compartilhar estado globalmente sem "prop drilling".
- [x] **Renderização e Listas:**
    - [x] Renderização condicional.
    - [x] Mapear arrays para renderizar listas de componentes (uso de `key`).
- [ ] **Roteamento:**
    - [ ] Usar a biblioteca `react-router-dom` para criar navegação entre páginas (Single Page Application).
- [x] **Requisições HTTP:**
    - [x] Fazer chamadas a APIs externas com `fetch` API ou `axios`.
    - [x] Lidar com estados de loading, success e error.
- [ ] **Gerenciamento de Estado Avançado (Opcional, mas recomendado):**
    - [ ] Entender os conceitos do Redux com Redux Toolkit.
    - [ ] Alternativas como Zustand ou Jotai.
- [ ] **Estilização:**
    - [ ] CSS Modules.
    - [ ] Styled-components ou Tailwind CSS (muito popular).

#### Projetos Práticos com React:

1.  **Básico: Aplicação de "Lista de Tarefas" (To-Do List)**
    * **Funcionalidades:** Adicionar, remover e marcar tarefas como concluídas.
    * **Conceitos aplicados:** Componentes, `useState` para a lista de tarefas, renderização de listas, passagem de props.
    * **Desafio extra:** Salvar as tarefas no `localStorage` do navegador para que não se percam ao recarregar a página (usando `useEffect`).

2.  **Intermediário: Catálogo de Filmes ou Produtos (Consumindo uma API pública)**
    * **Funcionalidades:** Uma página inicial que lista filmes populares (usando a API do [The Movie Database - TMDB](https://www.themoviedb.org/documentation/api)), uma barra de busca, e uma página de detalhes para cada filme.
    * **Conceitos aplicados:** `useEffect` para buscar os dados, `useState` para loading e error, `react-router-dom` para as rotas, passagem de parâmetros pela URL (ID do filme).
    * **Isso simula um teste técnico comum:** buscar dados de uma API e exibi-los de forma organizada.

3.  **Avançado: Clone de um Dashboard (Trello ou Jira Simplificado)**
    * **Funcionalidades:** Um quadro com colunas (ex: "A Fazer", "Em Andamento", "Concluído"). O usuário pode criar cartões (tarefas), e arrastar e soltar (`drag and drop`) os cartões entre as colunas. Autenticação de usuário (pode ser simulada no início).
    * **Conceitos aplicados:** Gerenciamento de estado mais complexo (talvez com `useContext` ou Redux Toolkit), manipulação de eventos complexos, uso de uma biblioteca de `drag and drop` (como `react-beautiful-dnd`), interação com uma API backend (que você construirá na próxima fase).

---

## Fase 3: Construindo o Backend com Node.js e Express

Agora vamos criar a API que dará vida às suas aplicações frontend.

### Node.js, Express e Banco de Dados

- [ ] **Fundamentos de Node.js:**
    - [ ] Entender o que é o Node.js e seu ecossistema (NPM).
    - [ ] Módulos (CommonJS e ES Modules).
    - [ ] Programação assíncrona (Callbacks, Promises, Async/Await).
- [ ] **Express.js:**
    - [ ] Criar um servidor web básico.
    - [ ] Estrutura de Rotas (Router).
    - [ ] Entender o que são Middlewares.
    - [ ] Receber e tratar requisições (req.body, req.params, req.query).
- [ ] **APIs RESTful:**
    - [ ] Entender os princípios do REST.
    - [ ] Verbos HTTP (GET, POST, PUT, DELETE).
    - [ ] Códigos de Status HTTP.
    - [ ] Criar endpoints para um CRUD (Create, Read, Update, Delete).
- [ ] **Conexão com Banco de Dados SQL (PostgreSQL):**
    - [ ] Usar um cliente como o `pg` ou um Query Builder como o `Knex.js`.
    - [ ] Entender o que é um ORM (Object-Relational Mapping) e usar um básico como o `Prisma` (moderno e recomendado).
- [ ] **Autenticação e Autorização:**
    - [ ] Implementar login usando senhas com hash (`bcrypt`).
    - [ ] Gerar tokens de acesso com JWT (JSON Web Tokens).
    - [ ] Proteger rotas que exigem autenticação.
- [ ] **Validação de Dados:**
    - [ ] Validar os dados de entrada das requisições (usando bibliotecas como `zod` ou `yup`).

#### Projetos Práticos com Node.js (Backend):

1.  **Básico: API para um Blog**
    * **Endpoints:** `POST /posts`, `GET /posts`, `GET /posts/:id`, `PUT /posts/:id`, `DELETE /posts/:id`.
    * **Conceitos aplicados:** Estrutura de rotas com Express, CRUD completo, manipulação de JSON. No início, pode usar um array em memória para simular o banco de dados.
    * **Desafio extra:** Conectar a um banco de dados SQL real (PostgreSQL) usando Prisma.

2.  **Intermediário: API para um E-commerce (Backend do projeto de React)**
    * **Endpoints:** CRUD para produtos, CRUD para usuários, e um sistema de carrinho. Adicionar um produto ao carrinho de um usuário.
    * **Conceitos aplicados:** Relacionamento entre tabelas no banco de dados (usuários, produtos, carrinhos), validação de dados (um produto deve ter nome e preço).
    * **Teste técnico clássico:** Modelar e implementar a lógica de negócio de um sistema real.

3.  **Avançado: API para o Clone do Trello (Backend do projeto avançado de React)**
    * **Endpoints:** Autenticação de usuário completa (registro e login com JWT), CRUD para quadros, colunas e cartões. Endpoint para mover um cartão entre colunas.
    * **Conceitos aplicados:** Autenticação com JWT, middlewares de autorização, lógica de negócio complexa, transações no banco de dados para garantir consistência.

---

## Fase 4: Especialização Opcional (Mas Poderosa): Java com Spring Boot

Se você quer se destacar e ter acesso a vagas em grandes empresas, esta é a trilha.

### Java e Spring Boot

- [ ] **Revisão de Java:**
    - [ ] Orientação a Objetos (Herança, Polimorfismo, Encapsulamento).
    - [ ] Collections Framework (List, Set, Map).
    - [ ] Streams e Lambdas.
- [ ] **Maven ou Gradle (Gerenciadores de Dependência):**
    - [ ] Entender como gerenciar as bibliotecas do projeto.
- [ ] **Spring Core:**
    - [ ] Inversão de Controle (IoC) e Injeção de Dependências (DI).
    - [ ] Entender o que são Beans.
- [ ] **Spring Boot:**
    - [ ] Criar um projeto com Spring Initializr.
    - [ ] Criar uma API REST com `@RestController` e `@RequestMapping`.
    - [ ] Mapeamento de verbos HTTP (`@GetMapping`, `@PostMapping`, etc.).
- [ ] **Spring Data JPA:**
    - [ ] Conectar com um banco de dados.
    - [ ] Mapear entidades Java para tabelas do banco (`@Entity`).
    - [ ] Usar Repositórios para operações de CRUD sem escrever SQL.
- [ ] **Spring Security:**
    - [ ] Configurar autenticação e autorização básica.

#### Projetos Práticos com Spring Boot:

1.  **Básico:** Construa a mesma **API para o Blog** da fase Node.js, mas agora com Spring Boot. Isso te ajudará a comparar as abordagens.
2.  **Intermediário:** Desenvolva uma **API para um sistema de gerenciamento de usuários e seus perfis**, com autenticação e endpoints protegidos usando Spring Security.
3.  **Avançado:** Crie uma **API para um pequeno sistema bancário**, com contas, transações (depósito, saque, transferência) e validações de regras de negócio (ex: não sacar mais do que o saldo). Isso exige o uso de transações (`@Transactional`) para garantir a integridade dos dados.

---

## Fase 5: Implantação e DevOps Básico

Um desenvolvedor Full-Stack precisa saber como colocar seu projeto no ar.

- [ ] **Docker:**
    - [ ] Entender o que são contêineres.
    - [ ] Escrever um `Dockerfile` simples para sua aplicação Node.js/Java.
    - [ ] Orquestrar frontend e backend com `docker-compose`.
- [ ] **Cloud:**
    - [ ] Criar uma conta em um provedor (AWS, Heroku, DigitalOcean, Vercel).
    - [ ] Fazer o deploy do seu frontend (Vercel e Netlify são ótimos e fáceis para React).
    - [ ] Fazer o deploy do seu backend e banco de dados (Heroku, Render ou um serviço de contêiner na AWS/GCP).
- [ ] **CI/CD (Conceitos):**
    - [ ] Entender o que é Integração Contínua e Entrega Contínua.
    - [ ] Configurar GitHub Actions para rodar testes automaticamente a cada `push`.
