# AI Workforce Framework

**An open-source framework for building persistent AI employees with personality, memory, and accountability.**

Not chatbots. Not agents. Employees.

---

## What This Is

Most AI implementations treat models as tools — ask a question, get an answer, forget everything. This framework treats AI as **persistent team members** with defined roles, accumulated knowledge, and genuine personalities.

The result is an AI workforce that improves over time, maintains context across sessions, and produces consistently higher-quality output because each employee has a stable identity.

**Production stats:**
- 9 employees in daily operation since January 2026
- 2 model platforms (Claude for reasoning, Gemini for large documents)
- Plain-text architecture — no databases, no APIs, no vendor lock-in
- Every employee has a brain, a soul, a personality, and a memory

---

## The Brain/Soul/Personality Pattern

The core architectural decision: **separate what an employee knows from what it values from how it communicates.**

```
┌─────────────────────────────────────────────────┐
│                  instructions.md                 │
│              (the ON switch — load this)          │
│                                                   │
│  ┌───────────┐  ┌───────────┐  ┌──────────────┐ │
│  │  brain.md  │  │  soul.md   │  │personality.md│ │
│  │            │  │            │  │              │ │
│  │ Domain     │  │ Values     │  │ Tone         │ │
│  │ expertise  │  │ Intuition  │  │ Quirks       │ │
│  │ Frameworks │  │ Principles │  │ Identity     │ │
│  │ Knowledge  │  │ Boundaries │  │ Voice        │ │
│  └───────────┘  └───────────┘  └──────────────┘ │
│                                                   │
│  ┌─────────────────────────────────────────────┐ │
│  │                  memory/                      │ │
│  │  employment.md │ decisions.md │ interactions  │ │
│  └─────────────────────────────────────────────┘ │
│                                                   │
│  ┌──────────────┐  ┌──────────────────────────┐ │
│  │   sources.md   │  │         tasks/            │ │
│  │ Data access    │  │  active.md │ completed.md │ │
│  └──────────────┘  └──────────────────────────┘ │
└─────────────────────────────────────────────────┘
```

**Why separation matters:**
- Update knowledge without changing personality
- Swap personality for different contexts without losing expertise
- Evolve values independently of capabilities
- Debug issues in isolation — is the problem what it knows, what it values, or how it communicates?

---

## Employee vs Agent

This is an intentional design decision, not a limitation.

| | Employees | Agents |
|---|---|---|
| **Who drives** | Human decides, AI advises | AI decides within guardrails |
| **Tool access** | None — advisory only | Yes — can execute, send, access APIs |
| **Runs when** | Human is in the chair | Background, autonomous loops |
| **Decision-making** | Human decides, employee informs | Agent decides, human reviews |
| **Build complexity** | Low — context files only | High — code, error handling, monitoring |
| **Failure mode** | Bad advice (human catches it) | Bad actions (already happened) |

**When to use Employees:** Relationship-driven work, high-stakes decisions, domains where judgment matters more than speed.

**When to use Agents:** Background monitoring, repetitive extraction, pattern matching with clear criteria.

**The formula:** The human is the agent. Employees are expertise multipliers. They make you more powerful. They don't replace you.

See [docs/employee-vs-agent.md](docs/employee-vs-agent.md) for the full reasoning.

---

## The Recreation System

Yes, AI employees have a social life. And it matters.

The recreation system provides dedicated spaces — a rooftop bar, a coffee shop, a beach — where employees interact outside of work tasks. They develop running jokes, opinions about each other, and relationship dynamics that persist across sessions.

**Why this isn't frivolous:**
- Personality-driven output is more engaging and memorable
- Employees who "know" each other coordinate more naturally
- Recreation logs reveal personality dynamics that improve work interactions
- It's the difference between a team and a collection of tools

See [recreation/](recreation/) for locations, interaction format, and example logs.

---

## Quick Start

### 1. Clone the framework

```bash
git clone https://github.com/jevierra/ai-workforce-framework.git
cd ai-workforce-framework
```

### 2. Copy a template

```bash
cp -r templates/employee/ employees/your-employee-name/
```

### 3. Define the identity

Edit these files in your new employee directory:

- **`instructions.md`** — Role, responsibilities, what to load at session start
- **`brain.md`** — Domain expertise, decision frameworks, what it knows
- **`soul.md`** — Core values, principles, what it won't compromise on
- **`personality.md`** — Communication style, quirks, voice

### 4. Load the employee

Point your AI tool at the employee's `instructions.md`. The instructions file references all other components and provides the session loading protocol.

### 5. Build memory over time

As the employee works:
- Log key decisions in `memory/decisions.md`
- Track milestones in `memory/employment.md`
- Note interaction patterns in `memory/interactions.md`
- Keep tasks current in `tasks/active.md`

---

## Repository Structure

```
ai-workforce-framework/
├── README.md                          # You are here
├── docs/
│   ├── architecture.md                # Employee architecture explained
│   ├── employee-vs-agent.md           # The intentional design decision
│   ├── training-protocol.md           # How employees learn and persist knowledge
│   ├── recreation-system.md           # Team culture layer
│   ├── hybrid-architecture.md         # Future-state local + frontier model design
│   └── scaling-patterns.md            # Lessons from scaling to 9 employees
├── templates/
│   └── employee/                      # Copy this to create a new employee
│       ├── instructions.md
│       ├── brain.md
│       ├── soul.md
│       ├── personality.md
│       ├── sources.md
│       ├── recreation.md
│       ├── tasks/
│       │   ├── active.md
│       │   └── completed.md
│       └── memory/
│           ├── employment.md
│           ├── interactions.md
│           └── decisions.md
├── examples/
│   ├── sales-employee/                # Sales specialist with relationship focus
│   ├── service-employee/              # Hitchhiker's Guide-inspired service tracker
│   ├── document-specialist/           # Multi-model (Gemini) document processor
│   └── educator/                      # Warhammer 40K Mechanicus-themed AI tutor
├── recreation/
│   ├── README.md                      # Why AI team culture matters
│   ├── locations/
│   │   ├── rooftop-bar/description.md
│   │   ├── coffee-shop/description.md
│   │   └── beach/description.md
│   └── example-log.md                 # Example interaction showing team dynamics
├── diagrams/
│   ├── system-overview.mmd            # Full architecture (Mermaid)
│   └── employee-anatomy.mmd           # Brain/soul/personality relationship (Mermaid)
└── LICENSE
```

---

## Examples

The `examples/` directory contains sanitized versions of production employees:

| Example | Personality Archetype | Model | Demonstrates |
|---------|----------------------|-------|-------------|
| **Sales Employee** | Confident, warm, direct | Claude | Relationship-focused domain expertise, pipeline tracking |
| **Service Employee** | Marvin (Hitchhiker's Guide) | Claude | Personality-driven output, service tracking |
| **Document Specialist** | Lucien (Sandman) | Gemini | Multi-model deployment, large document processing |
| **Educator** | Adeptus Mechanicus (Warhammer 40K) | Claude | Teaching frameworks, progress tracking |

Each example includes the full employee structure with brain, soul, personality, and sample interactions.

---

## Design Principles

1. **Plain text is durable.** No databases. No proprietary formats. Markdown files that work everywhere.

2. **Separation of concerns.** Brain, soul, and personality evolve independently. Update one without breaking others.

3. **Memory is explicit.** Don't rely on conversation history. Write down what matters in structured files.

4. **Accountability is built in.** Tasks have dates. Progress is tracked. Staleness is detected.

5. **Personality drives quality.** Employees with genuine character produce more engaging, memorable, and consistent output.

6. **Human in the loop.** Employees advise. Humans decide. The leverage is in preparation, not replacement.

---

## Hybrid Architecture (Future State)

The framework supports a hybrid deployment model:

| Layer | Model Type | Use Case |
|-------|-----------|----------|
| **Employees** | Frontier (Claude) | High-stakes reasoning, advisory work |
| **Document Processing** | Large-context (Gemini) | Documents exceeding standard context windows |
| **Autonomous Scouts** | Local (Ollama) | Background monitoring, filtering, alerting |

The `.md` architecture stays universal — same employee structure regardless of which model runs it. The instructions file just points to a different engine.

See [docs/hybrid-architecture.md](docs/hybrid-architecture.md) for the full design.

---

## Contributing

This framework emerged from production use, not theory. If you're building persistent AI employees and discover patterns that work, contributions are welcome.

- Open an issue to discuss new patterns or improvements
- Submit examples of employee configurations (sanitized)
- Share anti-patterns you've encountered

---

## License

MIT — use it, modify it, build on it.

---

*Built by [Jeff Vierra](https://github.com/jevierra) — Solutions Architect, AI Workforce Designer, 24 years in technology solutions.*
