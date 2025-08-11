# Projeto Cora - Frontend

Um projeto React com TypeScript e Vite para o desenvolvimento do projeto Cora, integrado ao backend NestJS.

## 📋 Pré-requisitos

Antes de começar, certifique-se de ter instalado em sua máquina:

* [Node.js](https://nodejs.org/) (versão 16 ou superior)
* [Git](https://git-scm.com/)

---

## 🚀 Instalação e Configuração

### 1. Clone o repositório

```bash
git clone https://github.com/SEU-USUARIO/projetocora-frontend.git
cd projetocora-frontend
```

---

### 2. Configuração do ambiente

Crie um arquivo `.env` na raiz do projeto com as seguintes variáveis:

```env
VITE_API_BASE_URL=http://localhost:3000
```

> **Importante:**
>
> * `VITE_API_BASE_URL` é a URL base do backend.
> * Mantenha o arquivo `.env` fora do GitHub.
> * Use o `.env.example` como modelo para sua equipe.

---

### 3. Instalar dependências

```bash
npm install
```

---

## 🏃‍♂️ Executando a aplicação

### Modo de desenvolvimento

```bash
npm run dev
```

A aplicação estará disponível em `http://localhost:5173`.

---

### Build de produção

```bash
npm run build
npm run preview
```

---

## 🧪 Testes

O projeto utiliza **Cypress** para testes de ponta a ponta (E2E).

### Abrir interface do Cypress

```bash
npm run test:e2e
```

### Executar testes em modo headless

```bash
npx cypress run
```

---

## 📁 Estrutura do Projeto

```
src/
├── assets/         # Imagens, ícones, fontes
├── components/     # Componentes reutilizáveis
├── controllers/    # Lógica de interação entre UI e serviços
├── pages/          # Páginas da aplicação
├── services/       # Integração com APIs
├── styles/         # Estilos globais
├── tests/          # Testes unitários e E2E
├── App.tsx
└── main.tsx
```

---

## 🔌 Integração com Backend

O frontend se comunica com o backend NestJS via **HTTP** usando a URL definida em `VITE_API_BASE_URL`.

Exemplo de uso no código:

```ts
const apiUrl = import.meta.env.VITE_API_BASE_URL;

fetch(`${apiUrl}/users`)
  .then(res => res.json())
  .then(data => console.log(data));
```

---

## 🛠️ Tecnologias Utilizadas

* **React** - Biblioteca de UI
* **TypeScript** - Linguagem de programação
* **Vite** - Bundler e Dev Server
* **Cypress** - Testes E2E
* **Testing Library** - Testes de integração
* **MVC adaptado** - Organização do código

---
