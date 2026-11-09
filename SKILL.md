---
name: es-legal-mcp-skill
description: Official Spain (ES) legislation, multi-tier court precedent research, and citation verification skill.
version: 2.0.0
author: JurisAtlas
license: MIT
---

# Spain Legal Research & Multi-Tier Case Law Skill (`es-legal-mcp`)

Use this skill whenever the user asks a legal question, drafts a pleading or contract, or researches case law across any judicial instance in **Spain (ES)**.

## Verification & Research Rules

1. **Citation Verification:** Never fabricate a statutory provision or case citation. Query `search_legislation`, `search_case_law`, `search_tiered_court_decisions`, or `verify_citation` before citing any authority (e.g., `ECLI:ES:TS:2024:150 or BOE-A-2024-1234`).
2. **Multi-Tier Judicial Coverage:**
   - **First Instance (Trial / Municipal / District):** Juzgados de Primera Instancia e Instrucción, Juzgados de lo Mercantil, de lo Penal, de lo Social & de lo Contencioso-Administrativo
   - **Second Instance (Cantonal / Regional / Appellate):** 50 Audiencias Provinciales, 17 Tribunales Superiores de Justicia (TSJ of Autonomous Communities) & Audiencia Nacional (AN)
   - **Supreme & Constitutional Instance:** Tribunal Supremo (TS) & Tribunal Constitucional de España (TC)
   - **Primary Tiered Database:** CENDOJ (Centro de Documentación Judicial — TS, AN, 17 TSJ, 50 Audiencias Provinciales & Juzgados) (`https://www.poderjudicial.es/search/indexAN.jsp`)
