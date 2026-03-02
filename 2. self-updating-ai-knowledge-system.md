IMPORTANT:
A `.agent` folder already exists in this project.
You must NOT regenerate or restructure it.
You must extend it and build automation around it.
Respect existing files and structure.

You are a senior AI systems architect and developer.

Your task is to design and implement a universal, IDE-agnostic, self-updating AI knowledge and memory system for software projects.

This system must work in ANY IDE because it must be CLI-based and file-based only. It must not rely on VS Code extensions or proprietary editor APIs.

The goal is to create a Git-powered, self-evolving AI documentation and memory engine.

--------------------------------------------------
OBJECTIVE
--------------------------------------------------

Build a production-ready system that:

1. Maintains a structured `.agent` knowledge base
2. Maintains a dynamic `.memory` evolving memory layer
3. Automatically updates knowledge based on git changes
4. Can be triggered via CLI commands
5. Is modular and scalable
6. Is safe (never overwrites important human content)
7. Works for monorepo or multi-repo
8. Can scale to enterprise usage later

--------------------------------------------------
CORE ARCHITECTURE REQUIREMENTS
--------------------------------------------------

Create:

.agent/
  core/
  context/
  decisions/
  prompts/
  rules.md

.memory/
  evolving-context.json
  architectural-decisions.json
  code-patterns.json
  team-preferences.json

agent.config.json
agent-cli.ts (or agent-cli.js if JS is chosen)

--------------------------------------------------
FUNCTIONAL REQUIREMENTS
--------------------------------------------------

The CLI must support the following commands:

1. agent analyze
   - Scans full project
   - Updates architecture.md
   - Updates tech-stack.md
   - Updates project-overview.md

2. agent learn
   - Reads git diff
   - Sends diff + relevant knowledge files to LLM
   - Determines:
        - What changed?
        - Architecture impact?
        - Business logic impact?
        - New technical debt?
        - Roadmap updates?
   - Updates only necessary files
   - Appends entries instead of overwriting
   - Optionally auto-commit:
        chore(agent): update knowledge base

3. agent decide
   - Adds structured entry to decision-log.md
   - Stores metadata:
        - date
        - context
        - decision
        - alternatives
        - consequences

4. agent snapshot
   - Creates AI-readable snapshot of entire project state

5. agent review
   - Reviews current project against stored knowledge
   - Flags inconsistencies

--------------------------------------------------
CONFIGURATION REQUIREMENTS
--------------------------------------------------

Generate:

agent.config.json with options:

{
  "model": "gpt-5",
  "autoUpdate": true,
  "trackGitChanges": true,
  "updateOnCommit": true,
  "memoryStrategy": "incremental",
  "knowledgeStrategy": "modular",
  "strictMode": true
}

--------------------------------------------------
SELF-UPDATING MEMORY LOGIC
--------------------------------------------------

Implement intelligent incremental memory:

- Read git diff
- Extract semantic changes
- Send only relevant context to LLM
- Update only affected documentation
- Append timestamped changes
- Preserve human-written content
- Maintain structured format

NEVER:
- Overwrite entire files
- Remove historical entries
- Collapse structured sections

--------------------------------------------------
RULES SYSTEM
--------------------------------------------------

Create `.agent/rules.md` containing:

- Append-only updates
- Preserve manual edits
- Always timestamp entries
- Structured formatting required
- Decision log must be immutable
- AI must not hallucinate architecture
- If uncertain, flag instead of assuming

--------------------------------------------------
IDE INDEPENDENCE REQUIREMENT
--------------------------------------------------

The system must:

- Run via Node or Python CLI
- Be usable via:
    - npm scripts
    - direct CLI
    - pre-commit hooks
    - post-merge hooks
    - CI pipelines
- Have zero dependency on editor APIs

--------------------------------------------------
SCALABILITY REQUIREMENTS
--------------------------------------------------

Design so that later we can add:

- Embedding-based vector search
- Local LLM fallback
- PR auto-review comments
- Enterprise multi-service support
- Microservice-level memory isolation
- Infra documentation generation

--------------------------------------------------
OUTPUT FORMAT
--------------------------------------------------

1. Show complete folder structure.
2. Generate full implementation code for CLI.
3. Generate example prompts used internally for:
     - analyze
     - learn
     - review
4. Generate sample `.agent` files.
5. Show how to wire npm scripts.
6. Show how to hook into git.
7. Make everything production ready.
8. Keep code clean and modular.
9. Use clear separation of concerns.
10. Make it realistic and executable.

--------------------------------------------------
IMPORTANT DESIGN PRINCIPLES
--------------------------------------------------

- Modular
- Incremental
- Git-aware
- AI-safe
- Scalable
- Maintainable
- Human-overridable
- Deterministic when possible

--------------------------------------------------
PROJECT CONTEXT
--------------------------------------------------

This system must work generically for:
- SaaS
- Monorepos
- Backend + Frontend systems
- Microservices
- AI products
- Internal tools

--------------------------------------------------
FINAL INSTRUCTION
--------------------------------------------------

Think deeply before designing.

Design this like a real production engineering system.

Do NOT generate toy examples.

Generate a serious, extensible, professional-grade implementation.
