# 📁 Estrutura do Projeto Front-End

Este documento descreve a estrutura de pastas e os arquivos principais do front-end do projeto **Painéis Digitais**, desenvolvido com **React**.

## 🧭 Visão Geral

O projeto utiliza **React** com **TypeScript** e segue uma arquitetura modular, facilitando a escalabilidade, legibilidade e manutenção. Para estilização, empregamos a biblioteca **Shadcn/ui**, que oferece um conjunto de componentes pré-construídos e altamente personalizáveis baseados em **Radix UI** e **TailwindCSS**. Isso permite acelerar o desenvolvimento de interfaces consistentes, acessíveis e com design moderno.

A estrutura geral é:

```
painel-digital-fe/
├── public/
├── src/
│   ├── components/
        ├── announcements
        ├── dashboard
        ├── layout
        ├── ui
│   ├── contexts/
│   ├── hooks/
│   ├── lib/
│   ├── pages/
│   ├── types/
│   ├── App.css
│   ├── App.tsx
│   ├── index.css
│   ├── main.tsx
│   ├── vite-env.d.ts
├── .gitignore
├── bun.lockb
├── components.json
├── eslint.config.js
├── index.html
├── package-lock.json
├── package.json
├── postcss.config.js
├── README.md
├── tailwind.config.ts
├── tsconfig.app.json
├── tsconfig.json
├── tsconfig.node.json
└── vite.config.ts
```
---

## 🗂️ Descrição das Pastas

### 📁 `public/`  
Arquivos estáticos (imagens, ícones, `favicon.ico`) que serão servidos diretamente pelo servidor.

---

### 📁 `src/`  
Todo o código-fonte da aplicação React:

- **`components/`** 🧩  
  Componentes reutilizáveis (botões, cards, modais, inputs), muitos deles estilizados com a lib **Shadcn/ui** (conjunto de componentes React acessíveis e personalizáveis, baseado em TailwindCSS).

- **`contexts/`** 🌐  
  Provedores de contexto React (via Context API) para compartilhamento de estado global, ex.: AuthContext, ThemeContext.

- **`hooks/`** 🪝  
  Custom Hooks que encapsulam lógicas de uso comum (ex.: `useAuth`, `useFetchTickets`, `useInterval`).

- **`lib/`** 📚  
  Funções utilitárias e wrappers externos, como instâncias de cliente HTTP (axios/fetch), config de validação (Zod schemas), helpers de formatação.

- **`pages/`** 📄  
  Diretório de rotas do React Router, ex.:  
  - `/login` → `pages/Login.tsx`  
  - `/tickets` → `pages/Tickets/index.tsx`

- **`types/`** 📝  
  Definições de interfaces e tipos TypeScript usados em todo o projeto (ex.: `User`, `Ticket`, `Anuncio`, `ApiResponse`).

- **`App.css` & `index.css`** 🎨  
  Estilos globais e reset/base do Tailwind.  
  - `index.css`: import e configuração do Tailwind  
  - `App.css`: estilos específicos de layout de componente raiz, se necessário

- **`App.tsx`** 🚀  
  Root component que monta `BrowserRouter`, `ThemeProvider` (Shadcn/ui) e define layout padrão.

- **`main.tsx`** ⚡  
  Ponto de entrada do Vite: renderiza `<App />` dentro de `document.getElementById('root')`.

- **`vite-env.d.ts`** 🔧  
  Tipagens extras do Vite (env vars, import de SVG/PNG como módulos).

---

### 🗃️ Arquivos de Configuração

- **`.gitignore`**  
  Padrões de arquivos/pastas que não devem ser versionados.

- **`bun.lockb`**  
  Lockfile do Bun.

- **`components.json`**  
  Configuração de componentes (**Shadcn/ui**).

- **`eslint.config.js`**  
  Regras de linting e plugins para manter estilo de código consistente.

- **`index.html`**  
  Template HTML principal do Vite (injeta `<div id="root">` e scripts).

- **`package.json` & `package-lock.json`**  
  Dependências, scripts e metadados do projeto.

- **`postcss.config.js`**  
  Plugins do PostCSS (Tailwind, autoprefixer).

- **`tailwind.config.ts`**  
  Customização do design system Tailwind (cores, breakpoints, plugins Shadcn/ui).

- **`tsconfig.app.json`, `tsconfig.node.json`, `tsconfig.json`**  
  Configurações do compilador TypeScript para app e build de node.

- **`vite.config.ts`**  
  Ajustes de build e plugins do Vite (alias de pastas, import de SVGs, integração com Shadcn/ui).

---

> 💡 **Dica**: Sempre que adicionar um novo diretório ou alterar a convenção de nomes, atualize este documento para manter a equipe alinhada!

---

## ✅ Convenções do Projeto

* O projeto segue o padrão de **componentes funcionais com hooks**.
* Toda nova funcionalidade deve ser escrita em **TypeScript**.
* A separação de responsabilidades deve seguir o princípio de **Single Responsibility** (cada módulo com seu papel bem definido).
* Para estilização, utilizamos o **TailwindCSS** em conjunto com a biblioteca **Shadcn/ui** para componentes acessíveis e consistentes.
