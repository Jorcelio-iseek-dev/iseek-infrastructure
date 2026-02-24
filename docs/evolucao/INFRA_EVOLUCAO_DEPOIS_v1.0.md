# ISEEK — INFRA EVOLUÇÃO (DEPOIS) v1.0
Projeto: iseek-infrastructure
Escopo: Melhorias incrementais após estabilidade

────────────────────────────────────────

1) OBJETIVO

Evoluir a infraestrutura com segurança e repetibilidade,
sem “feature creep” de infra e sem misturar camadas
(Public Web vs Core SaaS).

────────────────────────────────────────

2) EVOLUÇÕES (QUANDO HOUVER SINAL)

- Upgrade de compute (t3.small/t3.medium) conforme carga real
- MySQL em RDS (8.0.36+) quando confiabilidade/backup exigir
- Redis em ElastiCache quando filas/cache forem críticos
- S3 para arquivos quando houver persistência relevante
- CloudFront + WAF para superfície pública quando tráfego justificar
- Observabilidade incremental (alarmes) quando houver incidentes/necessidade
- IaC (Terraform) quando repetir ambientes virar necessidade
- HA/autoscaling apenas com pressão real (SLA/tráfego)

────────────────────────────────────────

3) COISAS QUE NÃO DEVEM ENTRAR CEDO

- Observability “pesada” sem necessidade
- Autoscaling sem baseline estável
- Jobs destrutivos de retenção sem política/auditoria
- Materialização de métricas/BI como “verdade paralela”

────────────────────────────────────────

4) ORDEM RECOMENDADA

1) Estabilizar baseline (AGORA) + validar isolamento e segurança
2) RDS (quando ambiente ficar sério)
3) ElastiCache (quando filas/cache forem críticas)
4) CloudFront+WAF (quando tráfego justificar)
5) IaC (quando precisar repetir ambiente)
6) HA/autoscaling (quando houver pressão real)

────────────────────────────────────────

FIM DO DOCUMENTO
ISEEK — Infra Evolução (Depois) v1.0
