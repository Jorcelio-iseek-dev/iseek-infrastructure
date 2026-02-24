# ISEEK — INFRA BASELINE (AGORA) v1.1
Projeto: iseek-infrastructure
Escopo: Subida de ambiente dedicado para teste real
Princípios iSeek: Disciplina + Isolamento + Determinismo + Data Safety

────────────────────────────────────────

1) DEFINIÇÃO

Este documento estabelece o baseline mínimo de infraestrutura
para operar a iSeek em ambiente dedicado de teste real,
preservando as invariantes Stable v1 (03.x → 07.0).

────────────────────────────────────────

2) ESCOPO (AGORA)

- Ambiente dedicado (sem misturar com servidores de clientes/aaPanel)
- Deploy previsível (Laravel 12)
- Hardening mínimo obrigatório
- Backup e restore testado
- Logs com retenção controlada
- Separação conceitual: Public Web vs Core SaaS

────────────────────────────────────────

3) INVARIANTES DE INFRA (NÃO NEGOCIÁVEIS)

- Tenant isolation preservado (nenhum leak cross-tenant)
- Data Safety (segredos fora do repo; sem segredos em logs/UI)
- MySQL como fonte de verdade onde definido
- Redis nunca é “fonte de verdade”
- Determinismo operacional (mudanças documentadas)

────────────────────────────────────────

4) REFERÊNCIA INSTITUCIONAL

Este baseline é alinhado ao marco Stable v1 (03.x → 07.0).
Infra não altera engine, invariantes ou fluxo de execução.
Infra apenas sustenta a operação com disciplina.

────────────────────────────────────────

FIM DO DOCUMENTO
ISEEK — Infra Baseline (Agora) v1.1
