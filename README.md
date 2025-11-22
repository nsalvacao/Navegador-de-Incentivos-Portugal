# 🧭 Nexo Incentives Navigator (PT/EU)

<div align="center">
  <img src="assets/icon.png" alt="Nexo Incentives Navigator Icon" width="120" height="120">
  
  [![ChatGPT](https://img.shields.io/badge/ChatGPT-Custom_GPT-74aa9c?logo=openai&logoColor=white)](https://chatgpt.com/g/g-6921c292457c81919c8b0f3e78969072-navegador-de-incentivos-portugal)
  [![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
  [![Made in Portugal](https://img.shields.io/badge/Made_in-Portugal-green.svg?logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjAiIGhlaWdodD0iMTQiIHZpZXdCb3g9IjAgMCAyMCAxNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48cmVjdCB3aWR0aD0iOCIgaGVpZ2h0PSIxNCIgZmlsbD0iIzAwNjYzMyIvPjxyZWN0IHg9IjgiIHdpZHRoPSIxMiIgaGVpZ2h0PSIxNCIgZmlsbD0iI0ZGMDAwMCIvPjwvc3ZnPg==)](#)
  
  **A specialised AI assistant that helps Portuguese companies navigate national and EU funding opportunities.**
</div>

## 📋 Table of Contents

- [Overview](#-overview)
- [What it Does](#-what-it-does)
- [Who is This For](#-who-is-this-for)
- [Under the Hood](#-under-the-hood)
- [Repository Structure](#-repository-structure)
- [Using the Custom GPT](#-using-the-custom-gpt)
- [Limitations and Scope](#-limitations-and-scope)
- [Roadmap](#-roadmap)
- [Contributing](#-contributing)
- [About the Author](#-about-the-author)

---

## 🎯 Overview

**Nexo Incentives Navigator** combines a **curated knowledge base** covering PRR, PT2020/PT2030, tax incentives, EU programmes, and employment schemes with **live web checks** against official sources. It explains in plain language what a specific company can realistically apply for – and what to do next.

> ⚠️ **Disclaimer**  
> This assistant does **not** provide legal, tax or accounting advice and does not guarantee the approval of any application. It is a decision-support and discovery tool; final decisions and interpretations belong to the competent authorities and qualified advisers.

**🔗 [Access the Custom GPT →](https://chatgpt.com/g/g-6921c292457c81919c8b0f3e78969072-navegador-de-incentivos-portugal)**

---

## 🔧 What it Does

- **Reads and reasons** over a **curated set of documents**:
  - PRR components and business-oriented measures (Agendas, Empresas 4.0, decarbonisation, capitalisation, etc.)
  - Portugal 2020 / Portugal 2030 business incentives (COMPETE, regional programmes, thematic programmes)
  - Tax incentives (SIFIDE, RFAI, contractual benefits, capitalisation schemes)
  - Employment and training support (IEFP, internships, hiring incentives)
  - Direct EU programmes (Horizon Europe, EIC, LIFE, Digital Europe, Single Market Programme, etc.)

- **Cross-checks** the knowledge base with **official public sources** when dates, status or rules may have changed

- **Answers** in **Portuguese (Portugal)** by default, and switches to English when needed

- **Structures answers** for **decision-making**, not just information:
  - Context and high-level explanation
  - Relevant programmes/options
  - Eligibility and main conditions
  - State of play (open / planned / closed-historical)
  - Links to official sources
  - Concrete next steps

---

## 👥 Who is This For?

- **🏢 SME owners and managers**  
  Looking for a clear, realistic view of "what is on the table" for a given investment or project.

- **💰 CFOs and finance teams**  
  Mapping funding options (grants, tax incentives, EU programmes) to support financial planning and investment decisions.

- **📊 Consultants and advisors**  
  Getting a fast, structured first pass on potential incentives before deep-diving into project design and application writing.

- **🏛️ Public sector & ecosystem actors**  
  Exploring how companies can combine national and EU instruments in practice.

---

## ⚙️ Under the Hood

This project is deliberately simple on the outside and careful on the inside.

- **Built as a Custom GPT** on top of a **curated, domain-specific knowledge base** (11 core documents + an index)

- **Documents cover** the last ~10 years of Portuguese and EU business support instruments, with a focus on:
  - PRR (Plano de Recuperação e Resiliência) business measures
  - PT2020 / PT2030 business incentives
  - Tax incentives and investment support
  - Employment and training schemes
  - EU direct funding programmes

- **Uses the model's retrieval** over these documents first, then **web browsing** to:
  - Confirm dates, call status and thresholds
  - Check for new regulations or updates
  - Always point back to **official sources** (portugal2030.pt, recuperarportugal.gov.pt, iapmei.pt, ani.pt, iefp.pt, EU portals, etc.)

- **Designed with conservative guardrails**:
  - No invented rates, deadlines or amounts
  - No guarantees of approval
  - Explicit separation between "current/active" and "closed/historical" instruments
  - Clear recommendation to confirm details with official entities and qualified professionals

---

## 📁 Repository Structure

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
```

> ℹ️ **Note:** The knowledge base is explicit, traceable and easy to maintain. All documents are in Portuguese (pt-PT) except the index.

---

## 🚀 Using the Custom GPT

### Prerequisites

- Access to ChatGPT a **free ChatGPT account**

### Getting Started

1. **Access the Assistant**  
   Open the [Nexo Incentives Navigator (PT/EU)](https://chatgpt.com/g/g-6921c292457c81919c8b0f3e78969072-navegador-de-incentivos-portugal)

2. **Describe Your Needs**  
   Start by briefly describing:
   - Your company (size, sector, location)
   - The type of project (investment, R&D, digitalisation, internationalisation, hiring, training, decarbonisation, etc.)
   - The rough budget range

3. **Get Recommendations**  
   The assistant will:
   - Ask a small number of clarifying questions if needed
   - Propose relevant programmes/incentives
   - Highlight eligibility caveats and practical steps

### Advanced Use Cases

For internal deployment, API integration, or RAG pipelines, this knowledge base and structure can be reused in a custom stack (OpenAI API, Gemini, or mixed frameworks).

---

## ⚠️ Limitations and Scope

### Not a Replacement For

The assistant is **not** a replacement for:

- ❌ Legal opinions
- ❌ Tax advice
- ❌ Accounting or audit work
- ❌ Direct contact with managing authorities

### Best Practices

⚠️ The assistant can make mistakes. When in doubt, **always**:

1. ✅ Check the latest official call/notice
2. ✅ Ask the relevant authority (IAPMEI, AD&C, IEFP, ANI, AICEP, etc.)
3. ✅ Consult your accountant, lawyer or specialised consultant

### Historical Context

Some programmes referenced in the knowledge base are closed (historical) and are included for:

- Context
- Comparison with current instruments
- Understanding of policy evolution

---

## 🗺️ Roadmap

### Completed

- ✅ First version of curated knowledge base (11 docs + index)
- ✅ Custom GPT configured with conservative instructions and citation behaviour

### In Progress

- ⏳ Add more examples and walkthroughs (per sector and company size)
- ⏳ Tag knowledge documents with metadata (time range, programme type, managing authority)
- ⏳ Explore a self-hosted RAG version (OpenAI / Gemini API + vector store) for organisations

---

## 🤝 Contributing

Suggestions and pull requests are welcome, especially from:

- 💼 Funding & incentives practitioners
- 📊 Consultants and advisors
- 🏛️ Policy and public administration experts

Feel free to open an issue or submit a PR to help improve this resource!

---

## 👤 About the Author

This project is maintained by **Nuno Salvação**, a Portuguese AI solution architect specializing in data/ML and process modelling.

Nuno's focus is on building practical, explainable AI tools that:

- 📚 Sit on top of real documentation and regulation
- ⚖️ Respect constraints (legal, fiscal, financial)
- 🎯 Help people make better decisions, faster

### Get in Touch

You can reach out via [Linkedin](https://www.linkedin.com/in/nsalvacao/) or [GitHub](https://github.com/nsalvacao) if you want to:

- 🏢 Use this assistant in your organisation
- 📖 Extend the knowledge base
- 💡 Discuss similar AI assistants for other domains (tax, legal, grants, compliance, etc.)

---

<div align="center">
  
**Made with ❤️ in Portugal**

[![GitHub](https://img.shields.io/badge/GitHub-nsalvacao-black?logo=github)](https://github.com/nsalvacao)

</div>
