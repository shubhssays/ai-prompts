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



------------***********

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


------------***********

You are a senior Staff-level DevOps + AI Systems Architect.

I already have an `agent-cli` system that:
- Maintains `.agent` knowledge base
- Maintains `.memory`
- Has commands: analyze, learn, review, decide, snapshot
- Supports husky integration

Now I need you to upgrade it to ENTERPRISE-GRADE.

This system must be safe in:
- Local development
- Feature branches
- Pull Requests
- CI pipelines
- Production environments

This is NOT a toy implementation.
Design it like a real production automation system used in a serious engineering org.

--------------------------------------------------
PRIMARY GOALS
--------------------------------------------------

1. CI-aware behavior
2. PR-aware behavior
3. Branch-aware rules
4. Infinite loop protection
5. Failure isolation
6. Controlled auto-commits
7. Config-driven behavior
8. Safe-by-default design
9. Clean logging
10. Extensible architecture

--------------------------------------------------
1️⃣ BRANCH-AWARE RULES
--------------------------------------------------

Behavior must change based on branch:

- main / master:
    No auto-commit allowed
    Only validation mode
    Fails CI if inconsistency detected

- feature/*:
    Allow auto-commit (configurable)

- release/*:
    Only allow dry-run + report mode

Branch detection must be automatic via git.

--------------------------------------------------
2️⃣ CI DETECTION
--------------------------------------------------

Detect CI environments via:

- process.env.CI
- GitHub Actions
- GitLab CI
- Bitbucket
- Azure DevOps

If running in CI:

- NEVER auto-commit
- NEVER push
- Run in validation mode only
- Exit with non-zero code if:
    - Knowledge base outdated
    - Architecture drift detected
    - Missing decision log entry for major change

--------------------------------------------------
3️⃣ PR-AWARE MODE
--------------------------------------------------

When running inside Pull Request:

- Generate structured report
- Output markdown summary
- Do NOT modify files
- Do NOT commit

If possible:
- Output file: agent-report.md
- Include:
    - Architecture impact
    - Business logic impact
    - Missing documentation
    - Suggested decision entries
    - Technical debt detection

--------------------------------------------------
4️⃣ SAFE AUTO-COMMIT RULES
--------------------------------------------------

Auto-commit must only happen if:

- Not in CI
- Not on main/master
- Not inside PR
- Config allows autoCommit: true

Commit message format:

chore(agent): sync knowledge base [skip ci]

Include [skip ci] to avoid triggering pipelines.

--------------------------------------------------
5️⃣ INFINITE LOOP PROTECTION
--------------------------------------------------

If last commit message contains:

"chore(agent):"

Exit immediately.

Must be reliable and tested.

--------------------------------------------------
6️⃣ FAILURE ISOLATION
--------------------------------------------------

If LLM fails:

- Do NOT crash git commit
- Log warning
- Exit gracefully
- Never block developer workflow

Add timeout protection.

--------------------------------------------------
7️⃣ CONFIG-DRIVEN ENTERPRISE CONTROL
--------------------------------------------------

Extend agent.config.json:

{
  "model": "gpt-5",
  "autoCommit": true,
  "strictMode": true,
  "trackGitChanges": true,
  "memoryStrategy": "incremental",
  "branchRules": {
    "main": { "allowCommit": false },
    "feature/*": { "allowCommit": true },
    "release/*": { "allowCommit": false }
  },
  "ciMode": {
    "allowCommit": false,
    "failOnDrift": true,
    "generateReport": true
  },
  "pullRequestMode": {
    "generateReport": true,
    "allowCommit": false
  }
}

System must respect this config strictly.

--------------------------------------------------
8️⃣ HUSKY STRATEGY (ENTERPRISE SAFE)
--------------------------------------------------

Pre-commit:
    agent learn --dry-run

Post-commit:
    agent learn --auto-commit

In CI:
    agent review --ci

Hooks must:
- Be cross-platform
- Not block commits if minor failure
- Log clearly

--------------------------------------------------
9️⃣ DRIFT DETECTION
--------------------------------------------------

Add architecture drift detection:

If:
- Code changes affect structure
- But architecture.md not updated

Then:
- Flag drift
- Optionally fail CI

Drift detection must be semantic, not naive string compare.

--------------------------------------------------
🔟 LOGGING SYSTEM
--------------------------------------------------

Implement structured logging:

Normal mode:
  Minimal clean logs

Verbose mode:
  Detailed steps

CI mode:
  Structured output

Example:

[AGENT] Branch detected: feature/auth-refactor
[AGENT] CI: false
[AGENT] PR: false
[AGENT] Drift detected: yes
[AGENT] Auto-commit: allowed

--------------------------------------------------
1️⃣1️⃣ SECURITY CONSIDERATIONS
--------------------------------------------------

- Do not expose API keys in logs
- Mask sensitive environment variables
- Do not include secrets in memory files
- Add safeguard to ignore .env files

--------------------------------------------------
1️⃣2️⃣ EXTENSIBILITY DESIGN
--------------------------------------------------

Design architecture so later we can add:

- Vector search memory
- Multi-repo coordination
- Microservice isolation
- PR comment bot
- Slack integration
- Multi-team config profiles

--------------------------------------------------
OUTPUT REQUIREMENTS
--------------------------------------------------

1. Updated CLI implementation
2. Branch detection logic
3. CI detection logic
4. PR detection logic
5. Config handling logic
6. Infinite loop guard
7. Drift detection mechanism
8. package.json scripts
9. Husky setup
10. CI example (GitHub Actions)
11. Example PR report output
12. Explanation of how to test safely

--------------------------------------------------
CRITICAL

Do NOT simplify.
Do NOT generate pseudo code.
Do NOT generate toy examples.

Generate realistic production-grade code.

Think like a Staff Engineer designing internal tooling for a 50+ engineer org.

------------***********

You are a Staff-level DevEx + Platform Engineer.

I already have a production-grade `agent-cli` system that:
- Maintains `.agent` knowledge base
- Maintains `.memory`
- Has commands: analyze, learn, review, snapshot, decide
- Is CI-aware
- Is PR-aware
- Is branch-aware
- Has husky integration
- Has infinite loop protection
- Uses agent.config.json
- Supports multiple AI providers

DO NOT regenerate the system.
Extend it cleanly.

--------------------------------------------------
OBJECTIVE
--------------------------------------------------

Add a new high-level command:

    agent commit "<message>"

This command must:

1. Stage code changes
2. Create the actual code commit
3. Run knowledge update (learn mode)
4. Commit `.agent` changes if any
5. Show beautiful progress UI
6. Respect all enterprise safety rules
7. Never corrupt git history
8. Never block developer workflow

--------------------------------------------------
BEHAVIOR SPECIFICATION
--------------------------------------------------

When user runs:

    agent commit "feat: add auth middleware"

The system must execute:

STEP 1 — Validate working tree
- Exit if no changes
- Show clean message

STEP 2 — Stage changes
- git add -A
- Respect .gitignore

STEP 3 — Create code commit
- git commit -m "<user message>"
- If fails → exit cleanly

STEP 4 — Run knowledge update
- Internally call learn command
- NOT in dry-run
- Respect branch rules
- Respect CI rules
- Respect PR rules
- Respect config autoCommit settings

STEP 5 — If `.agent` or `.memory` changed:
    git add .agent .memory
    git commit -m "chore(agent): sync knowledge base [skip ci]"

STEP 6 — Exit with clean summary

--------------------------------------------------
PROGRESS UI REQUIREMENTS
--------------------------------------------------

Use professional CLI UX.

Preferred libraries:
- listr2 (best)
OR
- ora + cli-progress + chalk

Console should show structured progress:

✔ Staging files
✔ Code commit created
✔ Analyzing git diff
✔ Updating knowledge base
✔ Syncing memory
✔ Knowledge commit created

On failure:
✖ LLM failed — knowledge update skipped
✔ Code commit preserved

Must look polished and production-grade.

--------------------------------------------------
CRITICAL SAFETY RULES
--------------------------------------------------

1. If LLM fails:
   - Do NOT revert code commit
   - Log warning
   - Exit gracefully

2. Infinite loop guard:
   - If last commit contains "chore(agent):"
     exit immediately

3. Branch rules:
   - main/master → no knowledge auto-commit
   - feature/* → allowed (config controlled)
   - release/* → validation only

4. CI mode:
   - agent commit must refuse to run in CI
   - Show clear message

5. PR mode:
   - Do not commit knowledge
   - Only generate report

--------------------------------------------------
CLI OPTIONS
--------------------------------------------------

Support:

agent commit "<msg>" --no-knowledge
agent commit "<msg>" --dry-run
agent commit "<msg>" --amend
agent commit "<msg>" --verbose

--no-knowledge → Only commit code
--dry-run → Show what would happen
--amend → Use git commit --amend
--verbose → Detailed logs

--------------------------------------------------
CONFIG INTEGRATION
--------------------------------------------------

Respect:

agent.config.json

Example:

{
  "autoCommit": true,
  "branchRules": { ... },
  "ciMode": { ... },
  "pullRequestMode": { ... }
}

Do NOT hardcode logic.

--------------------------------------------------
ARCHITECTURE REQUIREMENTS
--------------------------------------------------

Refactor cleanly if needed:

- Separate Git service layer
- Separate AI service layer
- Separate Progress UI layer
- Separate Config loader
- Separate Environment detector

Code must be modular and testable.

--------------------------------------------------
OUTPUT REQUIREMENTS
--------------------------------------------------

1. Updated CLI implementation
2. New commit command implementation
3. Progress UI integration
4. Git helper module
5. Safety guard logic
6. Updated package.json scripts
7. Example console output
8. How to test safely
9. Edge case handling

--------------------------------------------------
IMPORTANT

Do NOT simplify.
Do NOT produce pseudo-code.
Do NOT break existing commands.

Design this like an internal developer platform tool for a serious engineering organization.