# Checklist de Segurança - OWASP ASVS (Versão Mínima)

Este documento descreve os controles de segurança implementados no projeto LabTech Flow, baseados no padrão **OWASP Application Security Verification Standard (ASVS)**, nível 1, focado em aplicações web.

## Identificação da Equipe
* **Arylson Simão Lopes** — Tech Lead / Segurança
* **Davy Lopes da Cruz** — Analista de Requisitos / Validação

---

## 1. V2: Autenticação (Authentication)
| ID | Requisito | Status | Implementação no LabTech Flow |
|:---|:---|:---|:---|
| 2.1.1 | Senhas possuem comprimento mínimo (8+ caracteres). | Implementado | Nativo do Supabase Auth. |
| 2.1.7 | Não há limites arbitrários de caracteres especiais ou complexidade. | Implementado | Configuração de política de autenticação. |
| 2.1.9 | Bloqueio de conta após sucessivas tentativas falhas (Brute-force). | Implementado | Gestão de Rate Limit do Supabase. |

## 2. V3: Gestão de Sessão (Session Management)
| ID | Requisito | Status | Implementação no LabTech Flow |
|:---|:---|:---|:---|
| 3.1.1 | Uso de tokens de sessão seguros (JWT). | Implementado | Tokens gerados via Supabase/GoTrue. |
| 3.2.1 | Tokens de sessão expiram após período de inatividade. | Implementado | Timeout configurado no middleware do Next.js. |
| 3.4.1 | Sessão é invalidada no servidor após o logout. | Implementado | Chamada `supabase.auth.signOut()`. |

## 3. V4: Controle de Acesso (Access Control)
| ID | Requisito | Status | Implementação no LabTech Flow |
|:---|:---|:---|:---|
| 4.1.1 | O princípio do privilégio mínimo é aplicado. | Implementado | Perfis: Solicitante, Técnico e Coordenador. |
| 4.1.3 | Proteção de rotas administrativas. | Implementado | Middleware de autenticação por perfil no Next.js. |
| 4.1.5 | Controle de acesso em nível de linha (RLS) no DB. | Implementado | Políticas de Row Level Security no PostgreSQL. |

## 4. V5: Validação e Sanitização (Input Validation)
| ID | Requisito | Status | Implementação no LabTech Flow |
|:---|:---|:---|:---|
| 5.1.3 | Validação de tipos de dados (e.g. ID deve ser UUID). | Implementado | Tipagem forte com TypeScript e Zod. |
| 5.1.4 | Proteção contra SQL Injection. | Implementado | Uso de ORM/Query Builder (Supabase-js). |
| 5.3.3 | Proteção contra XSS (Cross-Site Scripting). | Implementado | Renderização segura nativa do React/Next.js. |

---

##  Observações de LGPD
O sistema armazena o nome e e-mail institucional dos alunos/professores apenas para fins de identificação do chamado. Não são coletados dados sensíveis (saúde, religião, etc.) conforme a Lei Geral de Proteção de Dados Pessoais.

---
**Data da última revisão:** 28/04/2026.
**Responsáveis:** Arylson Simão Lopes, Davy Lopes da Cruz.
