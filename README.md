# MyFather

Interactive faith-learning platform inspired by language-learning applications.
It combines guided lessons, quizzes, progression systems and an AI-assisted
conversation experience.

## Live prototype

[myfather.app](https://myfather.app)

> The product is currently an evolving prototype. Some sections and commercial
> flows are still under development.

## Highlights

- Adult, child, family and church account experiences
- Guided learning paths and quizzes
- Streaks, experience points and virtual currency
- AI-assisted questions and lesson exploration
- Subscription plans and digital store items
- Mercado Pago checkout
- Church-registration workflow
- Bilingual Spanish/English interface
- Responsive, animation-focused user experience

## Technology

- HTML5, CSS3 and JavaScript
- Supabase Auth and PostgreSQL
- Cloudflare Workers
- DeepSeek API
- Mercado Pago API
- Resend
- Custom domain and DNS

## Architecture

```text
Browser
   ├── Supabase Auth
   └── Cloudflare Worker
          ├── DeepSeek
          ├── Mercado Pago
          ├── Resend
          └── Supabase
```

Production credentials remain in Cloudflare environment variables and are not
included in the public client.

## Product and safety note

MyFather is an educational product concept. AI-generated responses are intended
to support exploration and should not be treated as professional religious,
medical, legal or crisis advice.

## Status

Prototype in active development.
