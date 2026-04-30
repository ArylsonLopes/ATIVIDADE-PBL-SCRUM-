# ADR-001 — Escolha da Stack de Desenvolvimento
* **Status:** Aceito
* **Data:** 22/04/2026
* **Decisores:** Arylson Simão Lopes, Davy Lopes da Cruz

## Contexto
O projeto exige um MVP funcional em apenas 4 semanas, com orçamento zero e foco em ambiente web responsivo. Precisamos de uma tecnologia que permita desenvolvimento rápido (Fullstack) e que tenha integração nativa com serviços de nuvem gratuitos.

## Decisão
A equipe decidiu utilizar o framework **Next.js (React)** para o frontend e backend (API Routes).

## Alternativas consideradas
* **Opção A:** Next.js (JavaScript/TypeScript)
* **Opção B:** Laravel (PHP)
* **Opção C:** Django (Python)

## Justificativa
O Next.js foi escolhido pela familiaridade da equipe com JavaScript e pela facilidade de deploy em ambientes como a Vercel, o que reduz drasticamente o tempo de configuração de infraestrutura.

## Consequências
* **Positivas:** Agilidade no desenvolvimento, vasta comunidade e ferramentas de UI prontas.
* **Negativas:** Curva de aprendizado em Server Components se o projeto escalar muito.
