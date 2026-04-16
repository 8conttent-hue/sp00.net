# CLAUDE.md — SP00

Site gerado pelo **SF (Site Factory)** em 15/04/2026.

## Contexto do Site

**Nome:** SP00
**Nicho:** general
**Keywords:** Ana Saboia Principais trabalhos e premiacoes Setembro de 2015 Vencedora do Meta
**Paleta de cores:** gold | **Fonte:** poppins

Ana Sabóia Principais trabalhos e premiações Setembro de 2015 Vencedora do Meta Photo Contest, Edição #56 Melhor foto de capa para revista asiática, Edição #56 Julho de 2015 Premiação de melhor foto noturna para a revista “The luxury travel magazine”  Anna Kordiva Principais trabalhos e premiações Fevereiro de 2017 3 Lugar para melhor foto de por do sol “The time of photography” Setembro de 2017 Vencedora do prêmio melhor foto de natureza pela revista “Photoography”



## Componentes visuais usados

| Seção | Variante |
|-------|----------|
| Header | Header-D |
| Hero | Hero-A |
| Features | Features-C |
| About Section | About-H |
| Posts | Posts-J |
| Footer | Footer-I |
| Página Sobre | Sobre-J |
| Página Contato | Contato-F |

## Estrutura do projeto

```
src/
  sections/        # Layout escolhido pelo SF — Header, Hero, Features, About, Posts, Footer, Sobre, Contato
  data/            # JSONs com todo o conteúdo editável
  content/blog/    # Posts em Markdown
  pages/           # Rotas Astro (index, sobre, contato, blog, privacidade, termos)
  layouts/         # BaseLayout com fonte e cores dinâmicas
  styles/          # global.css com variáveis CSS de cor
public/
  images/          # hero.jpg, about.jpg, blog/*.jpg — inseridos automaticamente via Pexels
```

## O que editar

### Textos e conteúdo
- **`src/data/home.json`** — hero (título, subtítulo, botão), features (título, items), about section (título, desc, stats), posts
- **`src/data/sobre.json`** — conteúdo completo da página Sobre (hero, texto, missão)
- **`src/data/contato.json`** — título, subtítulo, email, tempo de resposta
- **`src/data/siteConfig.json`** — nome, slug, email, redes sociais, menu

### Imagens
Imagens já estão em `public/images/` (via Pexels). Para substituir, mantenha os mesmos nomes de arquivo:
- `hero.jpg` — imagem de fundo do Hero
- `about.jpg` — imagem da seção About (home)
- `sobre.jpg` — imagem de fundo da página Sobre
- `blog/{slug}.jpg` — imagens dos posts

### Posts do blog
Arquivos em `src/content/blog/`. Ajuste o tom de voz, adicione dados específicos do nicho e personalize conforme a identidade do site.

### Cores
Variáveis em `src/styles/global.css`: `--color-primary`, `--color-accent`, `--color-dark`.

## Deploy

```bash
bun install
bun run build
# Faça upload da pasta dist/ para Netlify, Vercel ou hosting estático
```
