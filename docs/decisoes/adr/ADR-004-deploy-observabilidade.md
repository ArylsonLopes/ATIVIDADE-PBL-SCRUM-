# ADR-004 — Estratégia de Deploy e Observabilidade
* **Status:** Aceito
* **Data:** 24/04/2026
* **Decisores:** Arylson Simão Lopes, Davy Lopes da Cruz

## Contexto
O MVP precisa estar disponível na web para testes do cliente final (coordenação). Além disso, precisamos monitorar se o sistema está online e se ocorrem erros em produção.

## Decisão
Realizar o deploy na plataforma **Vercel** e utilizar o **LogSnag ou Sentry** (camada free) para monitoramento.

## Alternativas consideradas
* **Opção A:** Vercel (PaaS)
* **Opção B:** Netlify
* **Opção C:** Servidor VPS Local (Docker)

## Justificativa
A Vercel oferece integração contínua (CI/CD) direta com o repositório GitHub. Qualquer alteração no código é publicada automaticamente, facilitando o feedback rápido das Sprints do Scrum.

## Consequências
* **Positivas:** Processo de publicação automatizado e HTTPS nativo gratuito.
* **Negativas:** Dependência da estabilidade da plataforma Vercel.
