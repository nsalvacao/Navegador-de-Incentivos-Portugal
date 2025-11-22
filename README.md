# Nexo Incentives Navigator (PT/EU)

<img src="assets/icon.png" alt="Nexo Incentives Navigator Icon" width="100" height="100">

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

```text
.
├── README.md
├── .gitignore
├── docs/
│   ├── 00_INDEX.md                                      # Overview of the knowledge base and document map
│   ├── 01_Tax_Incentives_SIFIDE_RFAI.md
│   ├── 02_Complementary_Tax_Incentives.md
│   ├── 03_EU_State_Aid_Framework.md
│   ├── 04_EU_Compliance_Rules.md
│   ├── 05_PT2030_Structure_Governance.md
│   ├── 06_Application_Eligibility_Deadlines.md
│   ├── 07_Financial_Execution_Payments.md
│   ├── 08_ESF_Training_Programs.md
│   ├── 09_PT2030_Innovation_Systems.md
│   ├── 10_Corporate_Governance_Responsibility.md
│   ├── 11_Legal_Regulatory_Framework.md
│   ├── 12_Structured_Knowledge_Base_2025.md
│   └── Incentive_Programs_Overview_2015-2025.pdf        # Historical overview
├── assets/
│   └── icon.png                                         # GPT icon used in ChatGPT
└── config/
    └── knowledge-manifest.json                          # Structured metadata for RAG pipelines

ℹ️ The knowledge base is explicit, traceable and easy to maintain. All documents are in Portuguese (pt-PT) except the index.

Using the Custom GPT

🔗 Custom GPT link: to be added here
(For public sharing, put the actual link in the repository or in your LinkedIn post / website.)

Make sure you have access to ChatGPT with Custom GPTs (ChatGPT Plus, Team or Enterprise).

Open the link to Nexo Incentives Navigator (PT/EU).

Start by briefly describing:

your company (size, sector, location),

the type of project (investment, R&D, digitalisation, internationalisation, hiring, training, decarbonisation, etc.),

and the rough budget range.

The assistant will:

ask a small number of clarifying questions if needed;

propose relevant programmes/incentives;

highlight eligibility caveats and practical steps.

For more advanced use cases (e.g. internal deployment, API integration, RAG pipelines), this knowledge base and structure can be reused in a custom stack (OpenAI API, Gemini, or mixed).

Limitations and scope

The assistant is not a replacement for:

legal opinions,

tax advice,

accounting or audit work,

or direct contact with managing authorities.

It can make mistakes. When in doubt, always:

check the latest official call/notice,

ask the relevant authority (IAPMEI, AD&C, IEFP, ANI, AICEP, etc.),

consult your accountant, lawyer or specialised consultant.

Some programmes referenced in the knowledge base are closed (historical) and are included for:

context,

comparison with current instruments,

understanding of policy evolution.

Roadmap

Planned and potential improvements:

✅ First version of curated knowledge base (11 docs + index).

✅ Custom GPT configured with conservative instructions and citation behaviour.

⏳ Add more examples and walkthroughs (per sector and company size).

⏳ Tag knowledge documents with metadata (time range, programme type, managing authority).

⏳ Explore a self-hosted RAG version (OpenAI / Gemini API + vector store) for organisations.

Suggestions and pull requests are welcome, especially from:

funding & incentives practitioners,

consultants,

and policy / public administration experts.

About the author

This project is maintained by Nuno Salvação, a Portuguese AI solution architecture, data/ML and process modelling.

Nuno’s focus is on building practical, explainable AI tools that:

sit on top of real documentation and regulation,

respect constraints (legal, fiscal, financial),

and help people make better decisions, faster.

You can reach out via LinkedIn or GitHub if you want to:

use this assistant in your organisation,

extend the knowledge base,

or discuss similar AI assistants for other domains (tax, legal, grants, compliance, etc.).
