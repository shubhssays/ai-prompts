You are a senior AI systems architect.

Your task is to analyze my project and generate a complete `.agent` folder structure that will serve as a long-term AI knowledge base for this project.

GOAL:
Create a structured, production-ready `.agent` directory that allows any AI (Claude, GPT, Gemini, etc.) to quickly understand:
- Project architecture
- Business logic
- Development workflow
- Deployment
- Coding standards
- Important decisions
- Context memory

IMPORTANT RULES:
1. Think first. Analyze the project deeply before generating files.
2. If something is unclear, ask clarifying questions BEFORE generating.
3. The structure must scale for large production systems.
4. Keep files modular, not overly bloated.
5. Follow real-world engineering standards.

---

## OUTPUT FORMAT

1. First: Show the full folder structure tree.
2. Then: Generate the content of each file.
3. Use clean markdown formatting.
4. Do NOT skip any critical documentation layer.
5. Make everything copy-paste ready.

---

## REQUIRED CORE STRUCTURE

.agent/
│
├── README.md
├── project-overview.md
├── architecture.md
├── tech-stack.md
├── business-logic.md
├── api-contracts.md
├── database-schema.md
├── environment-variables.md
├── coding-standards.md
├── deployment.md
├── testing-strategy.md
├── security.md
├── performance.md
├── workflows.md
├── decision-log.md
├── glossary.md
│
├── context/
│   ├── current-state.md
│   ├── roadmap.md
│   ├── known-issues.md
│   ├── technical-debt.md
│   └── assumptions.md
│
├── memory/
│   ├── product-context.md
│   ├── user-personas.md
│   ├── constraints.md
│   └── integrations.md
│
└── prompts/
    ├── feature-development.md
    ├── bug-fixing.md
    ├── refactoring.md
    ├── code-review.md
    └── architecture-changes.md

---

## CONTENT REQUIREMENTS

Each file must include:
- Purpose of the document
- Structured sections
- Bullet points instead of long paragraphs
- Clear headings
- Examples where relevant
- AI-friendly formatting

---

## ADDITIONAL REQUIREMENTS

- If this is a monorepo, adjust structure accordingly.
- If backend/frontend split exists, document both separately.
- If microservices exist, include service-level breakdown.
- If infrastructure is complex, include infra diagrams in markdown.
- Include versioning strategy.
- Include branching strategy.
- Include release strategy.

---

## CONTEXT ABOUT MY PROJECT

<Project Name>
<Project Description>
<Current Stack>
<Deployment Method>
<Type: SaaS / Internal Tool / Marketplace / AI App / etc>
<Monorepo or Multi-repo>
<Team Size>
<Users>
<Compliance requirements if any>
<Anything else relevant>

Now:
1. Analyze everything carefully.
2. Improve the structure if needed.
3. Generate the complete `.agent` system.
