## 🎨 Design System  

###[Figma](https://www.figma.com/design/JqZGA2y1CwgoPORThZdNIN/Fatec-Intranet---Design-System?node-id=2-287&t=mcZSa5iEDD4uSkDF-1)

## 1. Introdução
O presente Design System define o conjunto de estilos, cores, tipografia e princípios visuais utilizados para garantir a consistência e a identidade visual da marca. Ele foi desenvolvido sobre a base do **shadcn/ui**, um sistema de componentes moderno para React, com suporte completo a Tailwind CSS e alta capacidade de customização.

Os tokens foram extraídos diretamente do Figma por meio do plugin **Design Tokens**, refletindo os estilos padronizados do projeto.

Os objetivos principais deste Design System são:
- Promover consistência visual entre produtos digitais.
- Facilitar a comunicação entre design e desenvolvimento.
- Garantir acessibilidade e harmonia estética em todos os pontos de contato.

---

## 2. O que é o Shadcn UI
O **shadcn/ui** é uma coleção de componentes de interface de código aberto para React, construída com **Tailwind CSS** e **Radix UI**, focada em acessibilidade e design consistente. Diferente de bibliotecas tradicionais como MUI ou Chakra, o shadcn/ui não é um pacote npm, mas sim um conjunto de **componentes copiáveis** — o que permite total controle e personalização do código.

### ⚙️ Principais vantagens:
- Baseado em **Tailwind CSS** e **Radix UI**.
- Componentes **acessíveis e prontos para produção**.
- **Código local** — você controla e versiona os componentes.
- Altamente **customizável e extensível**.
- Mantido pela comunidade e compatível com **Next.js** e **Vite**.

📘 Documentação oficial: [https://ui.shadcn.com](https://ui.shadcn.com)

---

## 3. Como Instalar o Shadcn UI em um Projeto React

### Pré-requisitos
Antes de começar, garanta que o projeto React tenha:
- **Node.js** v18+  
- **Tailwind CSS** configurado

### Passos de instalação (Next.js ou Vite + React):

```bash
# 1. Instale o shadcn/ui CLI
tpnpm dlx shadcn-ui@latest init

# ou
nnpx shadcn-ui@latest init

# 2. Adicione componentes
npx shadcn-ui@latest add button card input dialog

# 3. Execute o servidor de desenvolvimento
npm run dev
```

Isso criará uma pasta `/components` com todos os componentes adicionados.

### Estrutura gerada:
```
src/
  components/
    ui/
      button.tsx
      card.tsx
      input.tsx
      dialog.tsx
```

Cada componente é um arquivo independente, estilizado com **Tailwind CSS** e pronto para customização.

---

## 4. Customizando o Shadcn UI

O Shadcn UI é projetado para **ser personalizado desde o início**. Todos os tokens, cores e fontes podem ser adaptados para refletir a identidade visual da **Fatec Intranet**.

### 🔧 Alterando o tema (tokens de cor e fonte)
Acesse o arquivo `tailwind.config.js` e adicione as variáveis do Design System:

```js
// tailwind.config.js
module.exports = {
  theme: {
    extend: {
      colors: {
        primary: {
          DEFAULT: '#b20000',
          hover: '#d60505',
        },
        secondary: '#005c6d',
        success: '#3acf1f',
        warning: '#b78718',
        error: '#d32719',
      },
      fontFamily: {
        sans: ['Roboto', 'sans-serif'],
      },
    },
  },
}
```

### 🧱 Exemplo: Customizando o botão padrão
```tsx
import { Button } from "@/components/ui/button"

export function Example() {
  return (
    <Button className="bg-primary hover:bg-primary-hover text-white">
      Enviar
    </Button>
  )
}
```

O estilo aplicado usará as variáveis de cor do Design System da Fatec Intranet.

---

## 5. Como Começar a Utilizar

1. Instale o shadcn/ui seguindo os passos acima.
2. Configure o Tailwind para usar os tokens definidos neste documento.
3. Importe os componentes da pasta `/components/ui`.
4. Ajuste estilos e cores conforme os tokens definidos no Design System.

💡 **Dica:** mantenha os tokens sincronizados com o Figma através do plugin **Design Tokens**. Assim, as alterações visuais serão refletidas no código de forma consistente.

---

## 6. Paleta de Cores

### 🎯 **Cores Principais**
| Nome | Hex | Descrição | Uso |
|------|-----|------------|-----|
| Vermelho Base | `#B20000` | Cor institucional principal da marca. | Botões primários, elementos de destaque. |
| Vermelho Escuro 10 | `#7E0000` | Variação mais escura do vermelho base. Estado de hover para elementos primários. | Borda, ícones, fundos de alerta. Hover em botões ou links principais. |

### 💧 **Cores Secundárias**
| Nome | Hex | Descrição | Uso |
|------|-----|------------|-----|
| Azul Base | `#005C6D` | Cor secundária da marca. | Links, destaques secundários. |
| Azul Destaque Base | `#00C1CF` | Cor complementar vibrante. | Ícones, estados ativos, badges. |
| Secundário Hover | `#00D8E8` | Estado de interação da cor secundária. | Hover em botões secundários. |

### 🌈 **Cores Auxiliares**
| Nome | Hex | Descrição | Uso |
|------|-----|------------|-----|
| Verde Base | `#A0C340` | Ênfase positiva. | Sucesso, confirmações. |
| Blueberry Base | `#4C7EFF` | Destaque informativo. | Links e informações. |
| Crayola Base | `#FFC24C` | Ênfase de aviso. | Alertas e notificações. |
| Violeta Base | `#8A29E6` | Ênfase visual. | Destaques visuais e gráficos. |
| Coral Base | `#FF4C4D` | Ênfase de erro. | Mensagens de erro e avisos. |
| Pink Base | `#FF4CA2` | Elementos decorativos. | Badges, marcação de status. |

### ⚡ **Cores de Feedback**
| Estado | Hex | Descrição | Uso |
|---------|-----|------------|-----|
| Cancelado | `#D32719` | Indica erro ou ação cancelada. | Alertas de erro. |
| Andamento | `#B78718` | Indica processo em execução. | Status intermediário. |
| Concluído | `#3ACF1F` | Indica sucesso. | Status finalizado. |
| Cancelado Outline | `#F95B4D` | Versão contorno. | Bordas de aviso. |
| Andamento Outline | `#DFB77B` | Versão contorno. | Ícones e gráficos. |
| Concluído Outline | `#80E96D` | Versão contorno. | Feedback positivo. |
| Cancelado Light | `#FDD5D1` | Fundo leve para erro. | Fundo de alerta. |
| Andamento Light | `#FFF5EA` | Fundo leve para aviso. | Fundo de status intermediário. |
| Concluído Light | `#E8FBE4` | Fundo leve para sucesso. | Fundo de status positivo. |

### ⚫ **Cores Neutras**
| Nome | Hex | Descrição | Uso |
|------|-----|------------|-----|
| White | `#FFFFFF` | Cor neutra de fundo. | Backgrounds, texto escuro sobre claro. |
| Prata Base | `#F8F8F8` | Fundo de seções neutras. | Áreas secundárias. |
| Prata Hover | `#F3F3F3` | Estado hover para fundos. | Interações sutis. |
| Cinza Claro | `#DADADA` | Tons neutros de interface. | Bordas, divisórias. |
| Cinza Hover | `#E6E6E6` | Feedback visual leve. | Estados interativos neutros. |
| Cinza Texto Base | `#666666` | Texto padrão neutro. | Corpo de texto, labels. |
| Black | `#000000` | Texto e elementos escuros. | Contraste e títulos. |

---

## 7. Tipografia

A tipografia é um dos principais pilares da identidade visual do Design System. O conjunto de estilos é baseado na fonte **Roboto**, escolhida por sua legibilidade, versatilidade e compatibilidade multiplataforma.

### 🧱 **Hierarquia Tipográfica**

| Estilo | Tamanho | Peso | Altura da Linha | Espaçamento | Família | Uso |
|---------|----------|-------|----------------|--------------|----------|-----|
| **H1** | 48px | 800 (Extra Bold) | 48px | -0.576px | Roboto | Títulos principais e cabeçalhos de páginas. |
| **H2** | 30px | 600 (Semibold) | 36px | -0.225px | Roboto | Subtítulos de seções. |
| **H3** | 24px | 600 (Semibold) | 32px | -0.144px | Roboto | Cabeçalhos de blocos ou módulos. |
| **H4** | 20px | 600 (Semibold) | 28px | -0.1px | Roboto | Subcabeçalhos, títulos secundários. |
| **Lead** | 20px | 400 (Regular) | 28px | 0 | Roboto | Textos introdutórios e destaques. |
| **Large** | 18px | 600 (Semibold) | 28px | 0 | Roboto | Textos de destaque intermediário. |
| **P (Parágrafo)** | 16px | 400 (Regular) | 28px | 0 | Roboto | Texto de corpo padrão. |
| **P UI** | 16px | 400 (Regular) | 24px | 0 | Roboto | Textos em componentes de interface. |
| **P UI Medium** | 16px | 500 (Medium) | 24px | 0 | Roboto | Textos com ênfase leve na interface. |
| **Body** | 14px | 400 (Regular) | 24px | 0 | Roboto | Textos secundários e legendas. |
| **Body Medium** | 14px | 500 (Medium) | 24px | 0 | Roboto | Labels e descrições curtas. |
| **Subtle** | 14px | 400 (Regular) | 20px | 0 | Roboto | Texto leve, instruções, placeholders. |
| **Subtle Medium** | 14px | 500 (Medium) | 20px | 0 | Roboto | Texto discreto com leve destaque. |
| **Small** | 14px | 500 (Medium) | 14px | 0 | Roboto | Rodapés, notas, legendas pequenas. |
| **Detail** | 12px | 500 (Medium) | 20px | 0 | Roboto | Detalhes técnicos e observações. |
| **Blockquote** | 16px | 400 (Regular, Itálico) | 24px | 0 | Roboto | Citações e mensagens destacadas. |
| **Inline Code** | 14px | 400 (Regular) | 20px | 0 | Menlo | Códigos curtos dentro de texto. |
| **Table Head** | 16px | 700 (Bold) | 24px | 0 | Roboto | Cabeçalho de tabela. |
| **Table Item** | 16px | 400 (Regular) | 24px | 0 | Roboto | Células de tabela. |

### 🧭 **Princípios de Uso Tipográfico**
- Utilize **H1 a H4** de forma hierárquica, sem pular níveis.  
- Use **Lead** e **Large** para introduções ou textos curtos de destaque.  
- **Body** é a base textual para conteúdo longo.  
- Prefira **Subtle** e **Detail** para informações auxiliares e legendas.  
- Utilize **Inline Code** apenas para pequenos trechos de código dentro de texto corrido.

### 💻 **Exemplo CSS**
```css
:root {
  --font-primary: 'Roboto', sans-serif;
  --font-code: 'Menlo', monospace;

  --text-h1: 800 48px/48px var(--font-primary);
  --text-h2: 600 30px/36px var(--font-primary);
  --text-body: 400 14px/24px var(--font-primary);
}

h1 {
  font: var(--text-h1);
  letter-spacing: -0.576px;
}

p {
  font: var(--text-body);
}
```

---

## 8. Tokens Tailwind (Escalas de Cores)
As escalas seguem o padrão **Tailwind CSS**, permitindo integração direta com sistemas utilitários. Cada tom é numerado de **50 (mais claro)** a **900 (mais escuro)**, abrangendo famílias como `slate`, `gray`, `teal`, `violet`, `pink`, `emerald`, `indigo`, entre outras.

Exemplo:
```css
--color-slate-50: #f8fafc;
--color-slate-900: #0f172a;
--color-gray-50: #f9fafb;
--color-gray-900: #111827;
```
Essas escalas são ideais para **backgrounds, bordas, sombras e hierarquia visual**.

---

## 9. Estados e Interações
Os estados de interação seguem princípios de **feedback visual imediato**:

| Estado | Ação visual |
|---------|-------------|
| **Hover** | A cor torna-se mais escura (para botões claros) ou mais clara (para botões escuros). |
| **Ativo** | Redução leve de luminosidade e aumento de contraste. |
| **Foco** | Adição de borda ou sombra suave para acessibilidade. |
| **Desativado** | Redução de opacidade e remoção de sombras. |

Exemplo CSS:
```css
.button-primary {
  background-color: var(--color-vermelho-base);
  color: #fff;
}

.button-primary:hover {
  background-color: var(--color-vermelho-base-hover);
}
```

---

## 10. Acessibilidade
- Utilize sempre **contrastes mínimos de 4.5:1** entre texto e fundo.  
- Prefira **cores claras para fundos** e **tons escuros para texto**.  
- Os tons claros (50–300) devem ser evitados para textos primários.  
- Priorize a coerência semântica:  
  - Verde → Sucesso  
  - Vermelho → Erro  
  - Amarelo / Laranja → Aviso  
  - Azul → Informação

---

## 11. Implementação Técnica

### 💻 **CSS Custom Properties**
```css
:root {
  --color-primary: #b20000;
  --color-primary-hover: #d60505;
  --color-secondary: #005c6d;
  --color-success: #3acf1f;
  --color-warning: #b78718;
  --color-error: #d32719;
  --color-neutral-100: #f8f8f8;
  --color-neutral-900: #000000;
}
```

### 🧩 **Tailwind Config (exemplo)**
```js
// tailwind.config.js
module.exports = {
  theme: {
    extend: {
      colors: {
        primary: {
          DEFAULT: '#b20000',
          hover: '#d60505',
        },
        secondary: '#005c6d',
        success: '#3acf1f',
        warning: '#b78718',
        error: '#d32719',
      },
    },
  },
}
```

---

## 12. Diretrizes de Uso
- **Evite** o uso de cores fora do conjunto institucional.  
- **Respeite** os contrastes definidos para acessibilidade.  
- **Priorize** consistência entre componentes e contextos.  
- **Atualize** os tokens via integração com o Figma sempre que houver alterações.

---

## 📚 Conclusão
O **Design System da Fatec Intranet** foi desenvolvido com base no **shadcn/ui**, garantindo uma estrutura moderna, escalável e acessível.  
Ele oferece integração direta com React e Tailwind, além de permitir customização total dos componentes, mantendo consistência visual e técnica em todos os projetos institucionais.

