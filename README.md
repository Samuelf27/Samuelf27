<picture>
  <source media="(prefers-color-scheme: dark)"  srcset="https://raw.githubusercontent.com/Samuelf27/Samuelf27/main/assets/pipeline-dark.svg?v=1">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Samuelf27/Samuelf27/main/assets/pipeline-light.svg?v=1">
  <img width="100%" src="https://raw.githubusercontent.com/Samuelf27/Samuelf27/main/assets/pipeline-dark.svg?v=1" alt="Samuel Ferreira, Desenvolvedor Full-Stack, São Paulo. Construo produtos digitais do primeiro commit ao servidor no ar. Esteira de promoção: dev, lint, typecheck, teste, build, pull request, main, release.">
</picture>

Trabalho o ciclo inteiro: modelo os dados, escrevo a API, construo a interface e coloco no ar.

Fundei a **[SFN Creative](https://sfncreative.tech/)**: sites, aplicativos e sistemas de gestão sob medida, para clientes reais.

O que separa os repositórios abaixo de código solto é a esteira do topo desta página: todos seguem o mesmo padrão de branches, portões e releases. Está tudo público, e dá para conferir commit por commit.

---

## Selected work

### node-api-starter · a base de API que eu não quero reescrever

Autenticação e autorização são a parte que todo projeto precisa e ninguém quer refazer. Esta é a minha resposta: JWT com **access + refresh**, rotação e revogação no logout, **RBAC** por papel, validação com Zod e Swagger em `/docs`. A camada de repositório é plugável: troca memória por PostgreSQL sem tocar nos serviços.

`TypeScript` · `Express` · `JWT` · `Zod` · `Swagger` · `Vitest + Supertest` · `Docker` · `PostgreSQL`
20 testes de integração · CI no GitHub Actions · `v1.0.0`

→ **[Código](https://github.com/Samuelf27/node-api-starter)**

### BR Toolkit · um domínio, quatro superfícies

CPF, CNPJ, PIS, CEP e telefone. Os mesmos algoritmos de dígito verificador, entregues de quatro formas, porque cada contexto consome de um jeito diferente.

- **[br-utils](https://github.com/Samuelf27/br-utils)**: biblioteca TypeScript, zero dependências, ESM + CJS, *tree-shakeable*. 34 testes · `v1.1.0` · [demo interativa](https://samuelf27.github.io/br-utils/)
- **[br-validator-api](https://github.com/Samuelf27/br-validator-api)**: a mesma validação exposta como REST, com Express, helmet, rate limiting e Docker. 13 testes · `v1.0.0`
- **[br-gen](https://github.com/Samuelf27/br-gen)**: CLI para gerar dados válidos em *seeds* e testes automatizados. `v1.0.0`
- **[br-toolkit-extension](https://github.com/Samuelf27/br-toolkit-extension)**: extensão Chrome, Manifest V3

### react-ui-kit · o design system que documenta a si mesmo

Componentes acessíveis (ARIA, foco, labels), tematizados por **design tokens** em CSS variables, com dark mode e *tree-shaking*. A documentação ao vivo é construída com os próprios componentes: se um quebra, a página mostra.

`React` · `TypeScript` · `Design tokens` · `a11y` · `Vitest`
8 componentes · 17 testes · `v1.0.0`

→ **[Documentação ao vivo](https://samuelf27.github.io/react-ui-kit/)** · [Código](https://github.com/Samuelf27/react-ui-kit)

### admin-dashboard · o painel que toda empresa acaba precisando

CRUD completo com modal e validação, tabela com busca, ordenação e paginação, KPIs e gráficos, dark mode persistente. A camada de API é desacoplada, pronta para plugar um back-end real. O login da demo é fictício e está documentado como tal. Não é segurança de produção.

`React` · `TypeScript` · `Vite` · `Tailwind CSS` · `Recharts`
Build e deploy automáticos via GitHub Actions

→ **[Demo ao vivo](https://samuelf27.github.io/admin-dashboard/)** · [Código](https://github.com/Samuelf27/admin-dashboard)

### devtoolbox · nove ferramentas, nenhum dado saindo da máquina

JSON, Base64, JWT, hash, UUID, timestamp, URL, cor e lorem. Tudo roda no cliente, via Web Crypto e Clipboard API, com *deep-link* por hash para compartilhar a aba aberta. Sem framework, sem build, sem servidor. E nada do que você cola sai do navegador.

`JavaScript` · `Web Crypto API` · `GitHub Pages`

→ **[Abrir](https://samuelf27.github.io/devtoolbox/)** · [Código](https://github.com/Samuelf27/devtoolbox)

Mais de vinte repositórios públicos além destes, entre estruturas de dados em TypeScript, automações e análise de dados em Python e utilitários de front-end, estão reunidos no **[hub](https://samuelf27.github.io/hub/)**.

---

## Stack

| | |
|---|---|
| **Interface** | React · Next.js · TypeScript · Vite · Tailwind CSS · design tokens · acessibilidade |
| **Aplicação** | Node.js · Express · REST · JWT (access + refresh) · RBAC · Zod · OpenAPI |
| **Dados** | PostgreSQL · Supabase · SQL |
| **Entrega** | Docker · GitHub Actions · Vitest · Supertest · versionamento semântico · Dependabot |

Antes disso, e ainda no perfil: Python (Pandas, Flask, Streamlit, automação com PyAutoGUI) e Java.

---

## Padrão de engenharia

<picture>
  <source media="(prefers-color-scheme: dark)"  srcset="https://raw.githubusercontent.com/Samuelf27/Samuelf27/main/assets/baseline-dark.svg?v=1">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Samuelf27/Samuelf27/main/assets/baseline-light.svg?v=1">
  <img width="100%" src="https://raw.githubusercontent.com/Samuelf27/Samuelf27/main/assets/baseline-dark.svg?v=1" alt="Padrão de engenharia aplicado em todos os repositórios: branches (duas permanentes, dev para main), promoção (só por pull request, origem conferida), integração (typecheck, teste e build antes do merge), entrega (docker, semver e release marcada), manutenção (dependabot ativo em todo repositório).">
</picture>

O mesmo contrato vale para todo repositório meu. Não é aspiração, é o que está configurado:

- **Branches**: `dev` e `main`, só essas duas. Nada experimental chega direto à produção.
- **Promoção**: toda mudança sobe por pull request, e um workflow confere de onde a branch veio.
- **Integração**: typecheck, testes e build no GitHub Actions antes do merge.
- **Entrega**: Docker onde faz sentido, versionamento semântico e release marcada.
- **Manutenção**: Dependabot ativo. Dependência desatualizada é dívida, não detalhe.

---

## Atividade

<picture>
  <source media="(prefers-color-scheme: dark)"  srcset="https://raw.githubusercontent.com/Samuelf27/Samuelf27/output/snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Samuelf27/Samuelf27/output/snake-light.svg">
  <img width="100%" src="https://raw.githubusercontent.com/Samuelf27/Samuelf27/output/snake-dark.svg" alt="Gráfico de contribuições do último ano, percorrido por uma linha animada.">
</picture>

<sub>Gerado a cada 12 horas por uma GitHub Action neste próprio repositório. Nada nesta página depende de um serviço de terceiros em tempo de carregamento.</sub>

---

**Aberto a projetos e oportunidades.**

[sfncreative.tech](https://sfncreative.tech/) · [LinkedIn](https://www.linkedin.com/in/samuel-ferreira27/) · [GitHub](https://github.com/Samuelf27) · [Instagram](https://www.instagram.com/samuuka_zs/)
