# Matriz de Decisão Tecnológica

Este documento justifica as escolhas técnicas realizadas pela equipe para o desenvolvimento do MVP do LabTech Flow, utilizando critérios objetivos e pesos baseados nas restrições do projeto (Prazo de 4 semanas e Orçamento R$ 0).

## Decisão 1: Web Stack (Linguagem e Framework)

| Critério (peso) | Opção A (Next.js + Supabase) | Opção B (Laravel + MySQL) | Opção C (WordPress) | Evidência/observação |
|:---|:---|:---|:---|:---|
| Prazo (3) | 5 | 3 | 4 | Next.js permite deploy instantâneo via Vercel e integração rápida. |
| Domínio do time (3) | 4 | 3 | 2 | Arylson e Davy possuem maior familiaridade com Ecossistema JS/React. |
| Custo/licença (3) | 5 | 5 | 4 | Next.js e Supabase possuem Free Tiers robustos e custo zero inicial. |
| Segurança (2) | 5 | 3 | 2 | Supabase oferece autenticação (Auth) e políticas de banco prontas. |
| Manutenibilidade (1) | 4 | 4 | 2 | Código modular facilita futuras evoluções no sistema. |
| **Total ponderado** | **42** | **31** | **28** | **Vencedora: Opção A** |

## Decisão 2: Banco de Dados

| Critério (peso) | Opção A (PostgreSQL via Supabase) | Opção B (Firebase Firestore) | Evidência/observação |
|:---|:---|:---|:---|
| Prazo (3) | 5 | 4 | Supabase configura o DB relacional automaticamente com a Auth. |
| Relacionamento (2) | 5 | 2 | PostgreSQL lida melhor com relações (Laboratório x Chamado x Técnico). |
| Custo (3) | 5 | 5 | Ambos possuem camadas gratuitas. |
| **Total ponderado** | **25** | **20** | **Vencedora: Opção A** |

## Decisão 3: Infraestrutura / Deploy

| Critério (peso) | Opção A (Vercel) | Opção B (VPS Local do Campus) | Evidência/observação |
|:---|:---|:---|:---|
| Prazo (3) | 5 | 2 | CI/CD automático na Vercel economiza dias de configuração. |
| Custo (3) | 5 | 5 | Vercel é gratuita para projetos acadêmicos/pessoais. |
| **Total ponderado** | **30** | **21** | **Vencedora: Opção A** |

---
**Participantes da decisão:** Arylson Simão Lopes, Davy Lopes da Cruz.
