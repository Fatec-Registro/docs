# 🫱🏻‍🫲🏻 Como Contribuir

🫶 Agradecemos o seu interesse em contribuir com o projeto! Para manter a organização e a clareza no desenvolvimento, seguimos padrões para a criação de branches e para a escrita de mensagens de commit. Seguir estas diretrizes nos ajuda a gerenciar o histórico de versões de forma eficiente e a automatizar tarefas como a geração de changelogs.

### 🧭 Padrão de Nomenclatura de Branches

Toda branch deve seguir o padrão de nomenclatura abaixo:

```bash
<tipo>/<descricao-curta>
```

-   **`<tipo>`**: Representa a categoria da alteração (ex: `feat`, `fix`, `docs`).
-   **`<descricao-curta>`**: Um resumo claro e direto da tarefa, **em português**, com palavras separadas por hífen (`-`).

#### 📂 Tipos de Branches e Commits

Utilize os seguintes tipos para categorizar suas branches e commits. A consistência entre eles é fundamental.

| Tipo | Descrição | Exemplo de Branch |
| :--- | :--- | :--- |
| `feat` | Novas funcionalidades (features). | `feat/sistema-de-autenticacao` |
| `fix` | Correção de bugs. | `fix/overflow-no-cabecalho` |
| `refactor` | Refatoração de código sem alterar o comportamento externo. | `refactor/logica-servico-usuario` |
| `docs` | Alterações e melhorias na documentação. | `docs/atualizar-readme` |
| `test` | Adição ou modificação de testes. | `test/testes-endpoint-login` |
| `chore` | Tarefas menores e rotineiras (build, dependências). | `chore/atualizar-dependencias` |
| `style` | Mudanças de formatação ou estilo (sem alterar lógica). | `style/corrigir-indentacao` |
| `ci` | Alterações em arquivos de Integração Contínua. | `ci/configurar-github-actions` |
| `infra` | Mudanças em infraestrutura (ex: Docker, setup inicial). | `infra/configurar-ambiente-docker` |

#### 🧱 Exemplos de Nomes de Branch

-   **Nova funcionalidade de autenticação com JWT:**
    ```bash
    git checkout -b feat/seguranca-autenticacao-jwt
    ```
-   **Documentação dos endpoints da API:**
    ```bash
    git checkout -b docs/documentacao-endpoints-api
    ```
-   **Correção de um bug de redirecionamento no login:**
    ```bash
    git checkout -b fix/redirecionamento-pagina-login
    ```

---

### 📜 Padrão de Commits

Para manter um histórico de commits claro e rastreável, seguimos o padrão **Conventional Commits**. Cada mensagem de commit deve ter a seguinte estrutura:

```
<tipo>(escopo opcional): <descrição>

[corpo opcional]

[rodapé opcional]
```

-   **Tipo**: Um dos tipos listados na tabela acima (`feat`, `fix`, `docs`, etc.).
-   **Escopo (Opcional)**: Uma palavra que especifica a parte do código afetada (ex: `api`, `login`, `database`).
-   **Descrição**: Um resumo conciso da alteração.
    -   Deve ser em português.
    -   Use o modo imperativo (ex: "**adiciona**" ao invés de "adicionado").
    -   Inicie com letra minúscula e não termine com ponto final.
-   **Corpo (Opcional)**: Uma explicação mais detalhada, justificando a mudança e o seu impacto.
-   **Rodapé (Opcional)**: Usado para referenciar issues (`Resolve: #123`) ou para indicar mudanças que quebram a compatibilidade (`BREAKING CHANGE:`).

#### 📝 Exemplos de Commits

**Commit simples (apenas título):**
```bash
feat: adiciona autenticação de usuário com email e senha
```

**Commit com escopo:**
```bash
fix(api): corrige cálculo de impostos no carrinho de compras
```

**Commit com corpo explicativo:**
```bash
refactor(database): atualiza método de conexão com o banco

O método anterior usava uma biblioteca depreciada que causava
vazamentos de memória. A nova implementação utiliza o driver
oficial e pool de conexões para mais performance e segurança.
```

**Commit com breaking change e referenciando issue:**
```bash
feat(api): altera o endpoint de busca de usuários

BREAKING CHANGE: O endpoint `GET /users` foi removido e
substituído por `GET /api/v1/users` para seguir o novo
padrão de versionamento da API.

Resolve: #45
```
---

### ✅ Regras Gerais

1.  **Idioma:** Mantenha nomes de branches e mensagens de commit em **português**.
2.  **Clareza:** Seja descritivo e evite termos genéricos. O nome da branch e a descrição do commit devem deixar claro o que foi feito.
3.  **Formato:** Use hífen (`-`) para separar palavras em nomes de branches.
4.  **Sincronia:** Mantenha sua branch sempre atualizada com a branch principal (`main` ou `develop`) para evitar conflitos.

Ao seguir este guia, você nos ajuda a manter o projeto organizado e a revisar suas contribuições de forma mais ágil. Boas contribuições!