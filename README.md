
# 2. Rode em modo desenvolvimento
npm start

# 3. Acesse no navegador
# http://localhost:3000
```

Para gerar a versão de produção:
```bash
npm run build
```

---

## Estrutura de arquivos

```
src/
├── assets/
│   └── profile.jpg          ← Sua foto de perfil
├── components/
│   ├── Navbar.jsx / .css     ← Barra de navegação
│   ├── Hero.jsx / .css       ← Seção inicial com foto + animação de digitação
│   ├── About.jsx / .css      ← Sobre mim + estatísticas
│   ├── Technologies.jsx/.css ← Cards de tecnologias
│   ├── Studying.jsx / .css   ← O que está estudando (com barra de progresso)
│   ├── Certifications.jsx/.css ← Certificados
│   ├── Projects.jsx / .css   ← Projetos do GitHub
│   └── Contact.jsx / .css    ← Links de contato
├── App.jsx / .css            ← Componente raiz
├── index.js                  ← Ponto de entrada React
└── index.css                 ← Estilos globais + variáveis CSS
```

---

## Como personalizar

### Trocar a foto de perfil
Substitua o arquivo `src/assets/profile.jpg` pela sua nova foto.

### Adicionar tecnologias
Abra `src/components/Technologies.jsx` e adicione um objeto no array `TECHNOLOGIES`:
```js
{
  name: 'Spring Boot',
  icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/spring/spring-original.svg',
  level: 'Estudando',
  levelClass: 'level-basic',
},
```

### Adicionar certificações
Abra `src/components/Certifications.jsx` e adicione no array `CERTIFICATIONS`:
```js
{
  title: 'Nome do Certificado',
  org: 'Organização',
  year: '2025',
  color: 'cert-purple',  // cert-red | cert-orange | cert-blue | cert-green | cert-purple
  initial: 'N',
  link: 'https://link-do-certificado.com',
},
```

### Adicionar projetos
Abra `src/components/Projects.jsx` e adicione no array `PROJECTS`:
```js
{
  name: 'Nome do Projeto',
  description: 'Descrição do que o projeto faz.',
  tags: ['Java', 'MySQL'],
  github: 'https://github.com/seu-usuario/repositorio',
  live: null, // ou URL do deploy
},
```

### Atualizar links de contato
Abra `src/components/Contact.jsx` e atualize o array `CONTACTS` com seu LinkedIn e GitHub reais.

### Mudar as cores
Todas as cores estão em `src/index.css` nas variáveis CSS `:root`. As principais são:
- `--green`: cor verde principal (`#1db954`)
- `--black`: fundo principal (`#080c08`)
- `--text-primary`: texto principal (`#e8f5e8`)

---

## Deploy gratuito

**Vercel** (recomendado):
1. Suba o projeto para um repositório no GitHub
2. Acesse [vercel.com](https://vercel.com)
3. Importe o repositório → deploy automático

**GitHub Pages**:
```bash
npm install -g gh-pages
# No package.json adicione "homepage": "https://seu-usuario.github.io/portfolio"
npm run build
gh-pages -d build
```
