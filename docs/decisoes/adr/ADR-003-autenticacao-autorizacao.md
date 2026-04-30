# ADR-003 — Sistema de Autenticação e Autorização
* **Status:** Aceito
* **Data:** 23/04/2026
* **Decisores:** Arylson Simão Lopes, Davy Lopes da Cruz

## Contexto
O sistema exige três perfis de acesso (Solicitante, Técnico e Coordenador) com permissões distintas. Por restrição de segurança e prazo, não é viável desenvolver um sistema de criptografia e gestão de sessões do zero.

## Decisão
Utilizar o **Supabase Auth** integrado com políticas de segurança de nível de linha (RLS - Row Level Security).

## Alternativas consideradas
* **Opção A:** Supabase Auth (E-mail/Senha)
* **Opção B:** NextAuth.js com banco próprio
* **Opção C:** Sistema de login manual com JWT

## Justificativa
O Supabase Auth já resolve a segurança de tokens, recuperação de senha e gestão de usuários de forma nativa, permitindo que a equipe foque nas funcionalidades de negócio do LabTech Flow.

## Consequências
* **Positivas:** Alta segurança (conformidade com padrões de mercado) e baixíssimo esforço de implementação.
* **Negativas:** Menor controle sobre o fluxo interno de geração de tokens.
