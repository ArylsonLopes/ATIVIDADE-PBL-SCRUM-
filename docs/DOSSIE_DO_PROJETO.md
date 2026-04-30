# DOSSIÊ DO PROJETO: LabTech Flow

## 1. Resumo Executivo
Este projeto apresenta a documentação do MVP de um sistema web para gestão de chamados de suporte técnico nos laboratórios de TI da UNIFACIMP. O objetivo central é eliminar a informalidade (WhatsApp/presencial) e centralizar as solicitações em uma plataforma única. A solução foca em baixo custo (open source), facilidade de uso e geração de métricas essenciais para a coordenação.

## 2. Problema e Objetivos
- **Problema:** Gestão ineficiente de manutenção nos laboratórios de TI devido à falta de canais oficiais, resultando em perda de histórico e interrupção de atividades acadêmicas.
- **Objetivo Geral:** Documentar e estruturar um sistema de chamados responsivo e seguro.
- **Métrica de Sucesso:** Redução do tempo médio de atendimento (SLA) para menos de 12h após a implementação do sistema.

## 3. Identificação da Equipe
- **Nome do projeto:** LabTech Flow
- **Arylson Simão Lopes:** Tech Lead / Arquitetura
- **Davy Lopes da Cruz:** Analista de Requisitos / Facilitador

## 4. Stakeholders e Perfis de Usuário
- **Solicitante (Professor/Aluno):** Abre chamados e acompanha o status de resolução.
- **Técnico:** Gerencia a fila de chamados e registra as manutenções realizadas.

## 5. Jornada AS-IS e TO-BE
| Etapa | AS-IS (Cenário Atual) | TO-BE (Cenário Proposto) |
| :--- | :--- | :--- |
| Reportar Erro | Mensagem via WhatsApp ou informal. | Formulário web com campos obrigatórios e anexo de foto. |
| Triagem | Atendimento por ordem de insistência. | Fila organizada por prioridade e tempo de espera. |
| Acompanhamento | Incerteza sobre a data de conserto. | Status em tempo real (Novo -> Em andamento -> Concluído). |

## 6. Requisitos Funcionais (12 User Stories)
1. **US01:** Como usuário, quero realizar login para acessar as funções do meu perfil.
2. **US02:** Como professor, quero abrir um chamado indicando o laboratório para solicitar manutenção.
3. **US03:** Como solicitante, quero anexar uma foto do problema para detalhamento visual.
4. **US04:** Como técnico, quero visualizar a fila de chamados pendentes para planejar o trabalho.
5. **US05:** Como técnico, quero assumir um chamado para sinalizar o início do atendimento.
6. **US06:** Como técnico, quero encerrar um chamado com log da solução aplicada.
7. **US07:** Como coordenador, quero visualizar relatórios por laboratório para identificar falhas recorrentes.
8. **US08:** Como solicitante, quero ver o histórico dos meus chamados.
9. **US09:** Como coordenador, quero gerenciar perfis de técnicos autorizados.
10. **US10:** Como usuário, quero recuperar minha senha via e-mail institucional.
11. **US11:** Como técnico, quero filtrar chamados por categoria (Hardware/Software).
12. **US12:** Como coordenador, quero exportar métricas de atendimento em formato CSV.

## 7. Requisitos Não-Funcionais
- **Segurança:** Autenticação via JWT e criptografia de dados sensíveis.
- **Desempenho:** Carregamento de páginas em menos de 2 segundos.
- **Disponibilidade:** Acesso 24/7 via web responsiva.

## 8. Priorização do Backlog (RICE)
| Funcionalidade | Alcance | Impacto | Confiança | Esforço | Score |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Abertura de Chamado | 10 | 3 | 100% | 2 | 15.0 |
| Login e Perfis | 10 | 3 | 100% | 1 | 30.0 |
| Relatórios | 2 | 3 | 90% | 4 | 1.35 |

## 9. Matriz de Decisão Tecnológica
- **Vencedora:** Next.js + Supabase.
- **Justificativa:** Menor tempo de desenvolvimento e custo zero de infraestrutura (Free Tier).

## 10. ADRs Registradas
- **ADR-001:** Escolha da Stack (Next.js/Supabase).
- **ADR-002:** Banco de Dados (PostgreSQL via Supabase).
- **ADR-003:** Autenticação (Supabase Auth).
- **ADR-004:** Deploy (Vercel).

## 11. Arquitetura C4
- **Contexto:** Sistema web interagindo com usuários e serviço de banco de dados/auth.
- **Containers:** Web App (React) e Data Provider (Supabase).

## 12. Checklist de Segurança (OWASP ASVS)
- Controle de autenticação e gestão de sessões.
- Proteção contra Cross-Site Scripting (XSS).
- Logs de eventos críticos e auditoria.
