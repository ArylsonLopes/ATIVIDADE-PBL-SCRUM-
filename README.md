# ATIVIDADE-PBL-SCRUM-
# LabTech Flow — Gestão de Chamados UNIFACIMP

Este repositório contém a documentação e o planeamento do MVP (Minimum Viable Product) para o sistema de gestão de manutenção dos laboratórios de TI do campus UNIFACIMP, desenvolvido para a disciplina de Métodos Ágeis com Scrum (ARA0152).

## Equipe (Turma 2026.1)
* Arylson Simão Lopes — Tech Lead / Arquitetura
* Davy Lopes da Cruz — Analista de Requisitos / Facilitador

---

## O Projeto
O LabTech Flow surge para resolver a falta de rastreabilidade nos pedidos de suporte técnico do campus. Atualmente, os pedidos são feitos de forma informal (WhatsApp e presencial), o que impede a priorização correta e a recolha de métricas de desempenho.

### Objetivos do MVP:
- Centralizar a abertura de chamados.
- Permitir o anexo de evidências fotográficas.
- Fornecer uma fila de trabalho organizada para os técnicos.
- Gerar relatórios básicos de recorrência por laboratório.

---

## Tecnologias Decididas (Stack)
Baseado na Matriz de Decisão Tecnológica e nos ADRs, a equipa optou por:
- Framework: Next.js (React)
- Backend/Database: Supabase (PostgreSQL)
- Autenticação: Supabase Auth
- Deploy: Vercel (Free Tier)

---

## Estrutura do Repositório
A organização das pastas segue o padrão obrigatório estabelecido:

- /docs/: Documentação principal.
  - DOSSIE_DO_PROJETO.md: Documento completo com requisitos e arquitetura.
  - /discovery/: Logs de pesquisa e evidências do problema.
  - /decisoes/: Matrizes de decisão e registros ADR.
  - /arquitetura/: Diagramas C4 (Contexto e Containers).
  - /seguranca/: Checklist OWASP ASVS.
  - /sprints/: Evidências das cerimónias Scrum (Sprint 01 a 04).
- /src/: Espaço reservado para o código fonte do MVP.

---

## Board de Gestão (Backlog)
O acompanhamento das tarefas e o progresso das Sprints podem ser visualizados no link abaixo:
> [LINK DO SEU BOARD AQUI - Ex: Trello/Jira/GitHub Projects]

---

## Como "Rodar" o Projeto (Documentação)
Como este projeto foca na Documentação do MVP (Entrega A):
1. Navegue até a pasta /docs.
2. O arquivo principal de leitura é o DOSSIE_DO_PROJETO.md.
3. Para entender as decisões técnicas, consulte os arquivos em /docs/adr/.

---

## Segurança e LGPD
O projeto segue as recomendações da OWASP ASVS, garantindo:
- Autenticação por perfis (Solicitante, Técnico, Coordenador).
- Validação de inputs para evitar SQL Injection e XSS.
- Tratamento de dados sensíveis conforme a LGPD brasileira.

---
*Este projeto é parte integrante da avaliação acadêmica da UNIFACIMP.*
