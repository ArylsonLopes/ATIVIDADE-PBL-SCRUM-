# ADR-002 — Escolha do Banco de Dados
* **Status:** Aceito
* **Data:** 22/04/2026
* **Decisores:** Arylson Simão Lopes, Davy Lopes da Cruz

## Contexto
O sistema de chamados requer o armazenamento de relações entre Usuários, Laboratórios, Categorias e Histórico de Comentários. É necessário um banco que suporte integridade referencial e que possua uma camada gratuita (Free Tier).

## Decisão
A equipe decidiu utilizar o **PostgreSQL**, gerenciado através da plataforma **Supabase**.

## Alternativas consideradas
* **Opção A:** PostgreSQL (via Supabase)
* **Opção B:** MySQL (via host compartilhado)
* **Opção C:** Firebase Firestore (NoSQL)

## Justificativa
O PostgreSQL é um banco relacional robusto. O Supabase foi escolhido por oferecer o banco como serviço (BaaS) gratuitamente, com ferramentas de visualização de dados e fácil integração com o Next.js.

## Consequências
* **Positivas:** Garantia de integridade de dados e facilidade de consultas complexas para relatórios.
* **Negativas:** Limite de conexões simultâneas na camada gratuita (suficiente para o MVP).
