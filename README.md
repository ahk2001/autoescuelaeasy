# Autoescuela EASY — Jerez de la Frontera (Cádiz)

Landing page institucional e de alta conversão da **Autoescuela EASY** (*EASY Centro de Formación* · `RALOB EASY FORMACION S.L.`, CIF `B06914808`, Código DGT `CA0508-01`), referência em Jerez de la Frontera desde 2015 com **82% de aprovados no exame prático B (DGT)** e **4,9 ★ no Google**.

- **Sede Principal:** Avenida de Nazaret, 48 · Barrio de Los Albarizones · 11406 Jerez de la Frontera (Cádiz)
- **Telefone & WhatsApp:** `+34 601 36 92 38` (`601 36 92 38`)
- **E-mail:** `info@autoescuelaeasy.es`
- **Instagram:** [@autoescuelaeasy](https://www.instagram.com/autoescuelaeasy/)
- **Repositório:** [github.com/ahk2001/autoescuelaeasy](https://github.com/ahk2001/autoescuelaeasy)
- **GitHub Pages:** [ahk2001.github.io/autoescuelaeasy](https://ahk2001.github.io/autoescuelaeasy/)

---

## Principais Recursos

- **Design Editorial & Identidade Oficial:** Interface em modo escuro com alto contraste em azul institucional (`#0019FB`), dourado viário (`#FFD600`) e tipografia refinada (`Inter Tight`, `Plus Jakarta Sans`, `JetBrains Mono`), além de vídeo introdutório responsivo (desktop 16:9 e mobile 9:16).
- **Estrutura Otimizada & Limpa:** HTML5 semântico, CSS3 moderno e Vanilla JavaScript puro, sem dependências pesadas e com ativos estáticos organizados em `assets/`.
- **SEO & Metadados:** Meta tags Open Graph, `robots.txt` (com bloqueio preventivo de `/docs/`) e `sitemap.xml` configurados.
- **Segurança & Cabeçalhos HTTP (`vercel.json`):**
  - `X-Content-Type-Options: nosniff`
  - `X-Frame-Options: SAMEORIGIN`
  - `X-XSS-Protection: 1; mode=block`
  - `Referrer-Policy: strict-origin-when-cross-origin`
  - `Permissions-Policy: camera=(), microphone=(), geolocation=()`
  - `Strict-Transport-Security: max-age=31536000; includeSubDomains; preload`
  - Cache imutável de 1 ano para ativos estáticos em `/assets/`.
- **CI/CD Seguro (`.github/workflows/deploy.yml`):** Pipeline automatizado para GitHub Pages com princípio de menor privilégio (`contents: read`, `pages: write`, `id-token: write`), controle de concorrência e publicação isolada em `_site/` (excluindo `/docs/` e configurações internas do artefato público).

---

## Estrutura de Diretórios

```text
autoescuelaeasy/
├── .github/
│   └── workflows/
│       └── deploy.yml                   # Pipeline CI/CD seguro para GitHub Pages
├── assets/                              # Mídias, vídeos e identidade visual
│   ├── favicon.png
│   ├── logo.png
│   ├── videohomedesktop.mp4
│   └── videohomemobile.mp4
├── docs/                                # Documentação interna e dossiê estratégico
│   ├── dados.txt
│   └── dossie_autoescola.md
├── .gitignore                           # Exclusões de segurança e arquivos temporários
├── index.html                           # Página principal institucional
├── README.md                            # Documentação técnica do projeto
├── robots.txt                           # Regras de rastreamento para buscadores
├── sitemap.xml                          # Mapa do site
└── vercel.json                          # Headers de segurança e cache para Vercel
```

---

## Deploy

### GitHub Pages
1. No repositório `ahk2001/autoescuelaeasy`, acesse **Settings > Pages**.
2. Em **Build and deployment > Source**, selecione **GitHub Actions**.
3. Todo push na branch `main` publica automaticamente apenas os arquivos públicos (`index.html`, `assets/`, `robots.txt`, `sitemap.xml`) em `https://ahk2001.github.io/autoescuelaeasy/`.

### Vercel
Com `vercel.json` incluído na raiz, basta importar o repositório no painel da Vercel ou executar `vercel --prod` para publicar com todos os headers de segurança e políticas de cache ativos.
