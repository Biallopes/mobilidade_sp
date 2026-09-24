# Data Engineering Lab — dbt + Databricks

Projeto colaborativo para praticar **Data Engineering, dbt, Databricks, Delta Lake, Git e modelagem de dados**, utilizando dados públicos.

O objetivo é construir um pipeline de dados completo, desde a ingestão dos dados brutos até modelos analíticos e testes de qualidade.

Projeto: “São Paulo Mobilidade Analytics” - Usar dados públicos de viagens de bicicleta compartilhada, transporte público ou trânsito e construir um pipeline completo
---

## Objetivo

Criar um pequeno **Lakehouse analítico** utilizando dados públicos.

O projeto será desenvolvido de forma colaborativa, utilizando Git para versionamento, branches, Pull Requests e code review.

### Tecnologias

- Databricks
- Apache Spark
- Delta Lake
- dbt
- SQL
- Python
- Git / GitHub

---

## Arquitetura

```text
                 PUBLIC DATA
                     │
                     ▼
              ┌──────────────┐
              │    BRONZE    │
              │ Raw Data     │
              │ Delta Tables │
              └──────┬───────┘
                     │
                     ▼
              ┌──────────────┐
              │    SILVER    │
              │ Cleaned Data │
              │ dbt models   │
              └──────┬───────┘
                     │
                     ▼
              ┌──────────────┐
              │     GOLD     │
              │   Analytics  │
              │ dbt models   │
              └──────┬───────┘
                     │
                     ▼
              ┌──────────────┐
              │   Analytics  │
              │ SQL / BI Tool│
              └──────────────┘
