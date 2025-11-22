# Nexo Incentives Navigator (PT/EU)

**Nexo Incentives Navigator** is a specialised AI assistant (Custom GPT) that helps Portuguese companies understand and navigate **national and EU funding, incentives and support schemes**.

It combines a **curated knowledge base** (PRR, PT2020/PT2030, tax incentives, EU programmes, employment schemes, etc.) with **live web checks** against official sources, and explains in plain language what a specific company can realistically apply for – and what to do next.

> ⚠️ Disclaimer  
> This assistant does **not** provide legal, tax or accounting advice and does not guarantee the approval of any application. It is a decision-support and discovery tool; final decisions and interpretations belong to the competent authorities and qualified advisers.

---

## What it does

- Reads and reasons over a **curated set of documents**:
  - PRR components and business-oriented measures (Agendas, Empresas 4.0, decarbonisation, capitalisation, etc.)
  - Portugal 2020 / Portugal 2030 business incentives (COMPETE, regional programmes, thematic programmes)
  - Tax incentives (SIFIDE, RFAI, contractual benefits, capitalisation schemes)
  - Employment and training support (IEFP, internships, hiring incentives)
  - Direct EU programmes (Horizon Europe, EIC, LIFE, Digital Europe, Single Market Programme, etc.)
- Cross-checks the knowledge base with **official public sources** when dates, status or rules may have changed.
- Answers in **Portuguese (Portugal)** by default, and switches to English when needed.
- Structures answers for **decision-making**, not just information:
  - context and high-level explanation
  - relevant programmes/options
  - eligibility and main conditions
  - state of play (open / planned / closed-historical)
  - links to official sources
  - concrete next steps

---

## Who is this for?

- **SME owners and managers**  
  Looking for a clear, realistic view of “what is on the table” for a given investment or project.

- **CFOs and finance teams**  
  Mapping funding options (grants, tax incentives, EU programmes) to support financial planning and investment decisions.

- **Consultants and advisors**  
  Getting a fast, structured first pass on potential incentives before deep-diving into project design and application writing.

- **Public sector & ecosystem actors**  
  Exploring how companies can combine national and EU instruments in practice.

---

## Under the hood

This project is deliberately simple on the outside and careful on the inside.

- Built as a **Custom GPT** on top of a **curated, domain-specific knowledge base** (11 core documents + an index).
- Documents cover the last ~10 years of Portuguese and EU business support instruments, with a focus on:
  - PRR (Plano de Recuperação e Resiliência) business measures
  - PT2020 / PT2030 business incentives
  - Tax incentives and investment support
  - Employment and training schemes
  - EU direct funding programmes
- Uses the model’s **retrieval over these documents first**, then **web browsing** to:
  - confirm dates, call status and thresholds
  - check for new regulations or updates
  - always point back to **official sources** (portugal2030.pt, recuperarportugal.gov.pt, iapmei.pt, ani.pt, iefp.pt, EU portals, etc.)
- Designed with **conservative guardrails**:
  - no invented rates, deadlines or amounts
  - no guarantees of approval
  - explicit separation between “current/active” and “closed/historical” instruments
  - clear recommendation to confirm details with official entities and qualified professionals

---

## Repository structure

A suggested structure for this repository:

```text
.
├── README.md
├── docs/
│   ├── 00_INDEX.md                     # Overview of the knowledge base and document map
│   ├── 01_PRR_Business_Measures.md
│   ├── 02_PT2020_Business_Incentives.md
│   ├── 03_PT2030_Business_Incentives.md
│   ├── 04_Tax_Incentives_SIFIDE_RFAI.md
│   ├── 05_Employment_IEFP_Programmes.md
│   ├── 06_EU_Direct_Programmes.md
│   ├── 07_Legal_Framework_References.md
│   ├── 08_Case_Notes_and_Patterns.md
│   ├── 09_Frequently_Asked_Questions.md
│   └── 10_Glossary_and_Definitions.md
├── assets/
│   └── icon.png                        # GPT icon used in ChatGPT
└── config/
    └── knowledge-manifest.json         # Optional: structured metadata about the docs
