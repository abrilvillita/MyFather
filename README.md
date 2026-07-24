<div align="center">

# MyFather
### Interactive faith-learning platform

[![Prototype](https://img.shields.io/badge/Prototype-myfather.app-635bff?style=for-the-badge&logo=googlechrome&logoColor=white)](https://myfather.app)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-f7df1e?style=for-the-badge&logo=javascript&logoColor=111)
![Supabase](https://img.shields.io/badge/Supabase-Auth_&_Data-3ecf8e?style=for-the-badge&logo=supabase&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-Workers-f38020?style=for-the-badge&logo=cloudflare&logoColor=white)

</div>

---

## About
MyFather explores how interactive product design can support structured faith education. It combines guided lessons, quizzes, progression, virtual rewards and AI-assisted conversation.

> Evolving educational prototype — not theological authority, pastoral guidance or a finished commercial service.

## Experiences
- Adult, child, family and church account concepts
- Guided lesson paths and quizzes
- Streaks, experience points and virtual currency
- AI-assisted questions and lesson exploration
- Free and subscription product tiers
- Digital store and reward concepts
- Mercado Pago checkout and church registration
- Spanish and English interface
- Responsive animation-focused UX

## Architecture
```text
Browser ├→ Supabase Auth
        └→ Cloudflare Worker ├→ AI provider
                              ├→ Mercado Pago
                              ├→ Resend
                              └→ Supabase / PostgreSQL
```

## Technology
HTML5 · CSS3 · JavaScript · Supabase Auth · PostgreSQL · Cloudflare Workers · DeepSeek API · Mercado Pago · Resend

## Product decisions
Reusable lesson structures reduce unnecessary AI consumption; static and generated content are combined to control operating cost; motion and feedback make learning more engaging.

## Run locally
```bash
git clone https://github.com/abrilvillita/MyFather.git
cd MyFather
```
Open `index.html`. Connected features require backend configuration.

## Status
**Prototype in active development.** Some content and commercial flows remain incomplete.

## Media
Prepared for future lesson walkthroughs, animation previews and a public demo video.

---
<div align="center">Designed and developed by [Abril Miranda Villa Márquez](https://github.com/abrilvillita)</div>
