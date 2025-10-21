Esta documentação provê um resumo dos sistemas ativos e o *stack* tecnológico padrão utilizado em nosso ambiente de desenvolvimento e produção.

---

## 💻 Sistemas e Aplicações

Abaixo estão listados os principais sistemas e aplicações mantidos pela equipe, com uma breve descrição do seu foco (se disponível):

| Sistema | Descrição (Foco Principal) |
| :--- | :--- |
| **Lib Designer System** | Sistema de design e bibliotecas de componentes. |
| **Intranet Base** | Plataforma interna fundamental para operações diárias. |
| **Auth** | Serviço centralizado de autenticação e autorização de usuários. |
| **PACE** | *(Detalhes a serem adicionados)* |
| **QTE** | *(Detalhes a serem adicionados)* |
| **Emissão de certificados** | Sistema dedicado à geração e gestão de certificados. |
| **AI** | Aplicações e serviços relacionados à Avaliação Integradora. |
| **Biblioteca** | Sistema de gestão de recursos. |
| **Academy** | Plataforma de aprendizado. |

---

## 🛠️ Stack Tecnológico Padrão

O ambiente é construído sobre um conjunto de tecnologias modernas e robustas, garantindo escalabilidade e facilidade de manutenção.

### 💾 Backend (BE)

| Categoria | Tecnologia | Detalhes |
| :--- | :--- | :--- |
| **Linguagem Principal** | Python | |
| **Framework** | Flask | Utilizado para construir APIs e serviços. |

### 🎨 Frontend (FE)

| Categoria | Tecnologia | Detalhes |
| :--- | :--- | :--- |
| **Framework/Biblioteca** | React | |
| **Tooling** | Vite | Utilizado para *bundling* rápido e ambiente de desenvolvimento. |
| **Linguagem** | TypeScript (TS) | Para tipagem estática e maior robustez. |
| **Componentização** | shadcn/ui | Biblioteca de componentes baseada em Radix e Tailwind CSS para construção rápida de UIs. Link de Referência: `https://www.shadcn.io` |

### 🗄️ Banco de Dados (DB)

| Categoria | Tecnologia | Detalhes |
| :--- | :--- | :--- |
| **SGBD** | PostgreSQL | Utilizado como o principal sistema de gerenciamento de banco de dados. |

### ☁️ Infraestrutura e Servidores

| Categoria | Ambiente | Detalhes |
| :--- | :--- | :--- |
| **Desenvolvimento** | Servidor Interno (DEV) | Ambiente de testes e desenvolvimento. |
| **Produção** | Servidor Interno (PROD) | Ambiente de produção e acesso ao público. |
