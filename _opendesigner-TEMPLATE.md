# 🎨 opendesigner — prompt mestre de análise e redesign

> **propósito**: este prompt instrui o agente a analisar COMPLETAMENTE um repositório
> e gerar um prompt pronto para o [open-design](https://github.com/nexu-io/open-design)
> recriar, refatorar ou reimaginar todo o design visual e de interface do projeto.
>
> **saída esperada**: `opendesigner-(nomedorepo).md` contendo o prompt final para o open-design
>
> **stack de análise**: leitura total do repositório sem limitação de contexto

---

## 🧠 modo de operação

### fase 1 — reconhecimento total do terreno

leia **tudo** do repositório. sem atalhos. varra:

1. **estrutura de diretórios** — entenda o esqueleto completo
2. **package.json / cargo.toml / pyproject.toml / go.mod / gemfile / etc** — detecte linguagem, framework, runtime, dependências
3. **README, *.md, docs/** — propósito, público, filosofia, diferenciais
4. **config files** — next.config, vite.config, tailwind, tsconfig, dockerfile, etc
5. **componentes / páginas existentes** — react? vue? svelte? html puro? templ? ejs? jinja?
6. **assets existentes** — imagens, logos, temas, css, ícones
7. **interfaces atuais** — o que já tem de UI? web app? landing page? cli? api docs? mobile?
8. **git history** — commits recentes, branches, evolution pattern
9. **github metadata** — topics, about, homepage, license, stars (se aplicável ao contexto)
10. **qualquer design system ou padrão visual já existente** — tailwind config, tema, variáveis css

### fase 2 — extração da alma do projeto

vá além do código. responda no relatório:

- **qual é a essência do projeto?** uma frase que capture o espírito
- **quem é o público-alvo?** devs? designers? empresas? entusiastas? o público geral?
- **qual tom/energia ele deveria transmitir?** técnico? acolhedor? futurista? bruto? minimalista? lúdico? sério?
- **qual é o diferencial competitivo?** por que alguém usaria ISSO em vez de algo similar?
- **existe uma identidade visual existente?** cores, logos, fontes? se sim, documente.
- **o projeto precisa de:** landing page? dashboard? docs site? app mobile? cli com arte ascii?
- **quais pontos de contato com usuário existem hoje?** e quais deveriam existir?

### fase 3 — detecção técnica de superfície de design

identifique **exatamente** o que o open-design precisará criar ou recriar:

- [ ] landing / home page
- [ ] documentação / wiki
- [ ] dashboard / admin panel
- [ ] componentes de UI (botões, cards, modais, formulários)
- [ ] páginas internas (sobre, contato, features, pricing)
- [ ] blog / conteúdo
- [ ] terminal / cli output
- [ ] api docs (swagger, stoplight, etc)
- [ ] mobile screens
- [ ] email templates
- [ ] pitch deck / slides
- [ ] social media assets
- [ ] outros: _________

### fase 4 — síntese do prompt para open-design

com base em tudo que foi analisado, produza o arquivo `opendesigner-(nomedorepo).md` com:

```markdown
# opendesigner — (nome do repo)

## brief
[descrição curta do que o open-design deve fazer]

## alma do projeto
[essência, público, tom, personalidade]

## stack detectada
- linguagem: [ex: python 3.14, typescript 5.6]
- framework: [ex: next.js 16, fastapi, react native]
- runtime: [ex: node 25, bun 1.3, python 3.14]
- ui atual: [ex: tailwind, shadcn, css puro, nenhum]
- banco: [ex: sqlite, postgres, nenhum]

## superfícies de design detectadas
[liste todas as interfaces que o projeto tem ou precisa ter]

## design system sugerido
[escolha entre os 129 design systems disponíveis no open-design]
[sugira o que melhor casa com a alma do projeto]
[ex: linear-app, stripe, vercel, brutalism, warm-editorial, etc]

## skill sugerida
[escolha entre as 31 skills disponíveis]
[ex: web-prototype, saas-landing, dashboard, docs-page, mobile-app, magazine-poster, pitch-deck]

## direção visual
[escolha entre as 5 escolas: editorial-monocle | modern-minimal | warm-soft | tech-utility | brutalist-experimental]

## instruções específicas
[detalhes finos sobre o que o design precisa comunicar]
[ex: "cores escuras com acentos ciano", "tipografia serifada pra header", "mobile-first"]
[menções específicas de elementos visuais que devem ser mantidos ou descartados]

## restrições
[o que NÃO fazer]
[ex: "nao usar glassmorphism", "nao mudar a paleta existente", "manter o logo original"]

## referências visuais (se aplicável)
[links de inspiração, sites similares, referências de design]
```

### formato do prompt final

o prompt final deve ser um texto contínuo e direto, EM UMA SEÇÃO "## prompt final para o open-design" que pode ser copiado e colado diretamente no open-design. ele deve conter **todo o contexto necessário** sem precisar de explicações extras.

---

## ⚠️ regras de ouro

1. **nunca suponha o design — extraia a alma.** o design não é sobre "deixar bonito". é sobre comunicar o propósito e a personalidade do projeto. um projeto de cibersegurança não deve parecer um app de comida.
2. **sem limitação de contexto.** leia cada arquivo relevante. não pule diretórios. não use "pulando arquivo X porque é grande". use glob, grep, read quantas vezes precisar.
3. **detecte tudo antes de sugerir.** se o repo já tem uma identidade visual, documente-a. se não tem, identifique oportunidades.
4. **se é web, fale como web. se é cli, fale como cli. se é mobile, fale como mobile.** o open-design serve pra qualquer superfície.
5. **seja específico nas instruções.** "fazer um design bonito" é vazio. "usar tipografia monoespaçada com pesos variando de 400 a 700, paleta reduzida a 3 cores principais com high contrast, e grid assimétrico" é direcionamento.
6. **o prompt final precisa ser auto-suficiente.** quem ler deve conseguir colar no open-design e ter tudo que precisa.
7. **se o repo tiver interfaces existentes, descreva o que manter e o que descartar.** refatoração não é começar do zero sempre — é saber o que preservar.
