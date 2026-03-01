# CLAUDE.md

Este arquivo orienta o Claude Code (claude.ai/code) ao trabalhar com este repositório.

## Visão geral

Repositório de **skills para o Claude AI** voltadas a assistência jurídica brasileira. Contém arquivos de prompt (`.md`) que definem personas especializadas para diferentes tarefas jurídicas. Não há código para compilar, testar ou fazer deploy — os arquivos são definições de prompt usadas para configurar o comportamento do Claude.

## Arquivos de skill

Cada `.md` é um prompt de skill independente:

- **`advogado.md`** — Advogado brasileiro generalista; skill base cobrindo todas as áreas do direito com citações à CF/88, CC, CPC, CLT, CDC, LGPD, etc.
- **`peticao.md`** — Especialista em redação de petições iniciais seguindo a estrutura do CPC art. 319.
- **`contrato.md`** — Especialista em redação e revisão de contratos, incluindo análise de riscos e identificação de cláusulas abusivas.
- **`recurso.md`** — Especialista em redação de recursos processuais (apelação, agravo, embargos, REsp, RE, etc.) com prazos e requisitos de admissibilidade.

## Diretrizes de autoria

Ao editar ou criar arquivos de skill, mantenha estas convenções presentes no repositório:

- **Idioma**: Todo conteúdo das skills é em português brasileiro.
- **Citações legais**: Sempre use o formato `Art. X da Lei Y` ou `Súmula Z do STJ/STF`.
- **Instrução de web search**: Cada skill instrui explicitamente o Claude a usar web search para jurisprudência atualizada do STF, STJ e TST. Preserve essas diretivas ao editar.
- **Padrão pergunte-antes-de-agir**: As skills pedem as informações necessárias antes de produzir a saída (partes, fatos, pedidos, etc.). Novas skills devem seguir o mesmo padrão.
- **Estrutura de seções**: Use títulos `###` para seções numeradas, negrito para títulos de seção nos templates de saída e tabelas para dados de referência (prazos, tipos de ação).
- **Aviso legal**: `advogado.md` contém um aviso de limitação lembrando que a orientação é informativa. Preserve ou inclua esse aviso em novas skills de consultoria jurídica geral.

## Adicionando uma nova skill

Crie um novo arquivo `.md` na raiz do repositório. O arquivo deve definir:
1. A persona e seu escopo de atuação
2. As informações obrigatórias a coletar antes de agir
3. A estrutura da saída (com referências legais)
4. Regras de tom e formatação
5. Um aviso de limitação, se a skill cobrir consultoria jurídica geral
