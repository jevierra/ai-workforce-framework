# Employee Architecture Explained

## The Universal Employee File Structure

Every AI employee in this framework follows the same structural pattern. This isn't arbitrary -- it's the result of iterating through multiple employees and discovering what actually matters for consistent, high-quality output over time.

```
employee-name/
  instructions.md        # The ON switch
  brain.md               # Domain expertise and thinking patterns
  soul.md                # Values, intuition, and boundaries
  personality.md         # Communication style, identity, and voice
  sources.md             # Data access and reference material
  training/              # Learning material and domain knowledge
  memory/                # Persistent state across sessions
  tasks/                 # Accountability and work tracking
```

## The ON Switch: instructions.md

The `instructions.md` file is the single entry point that loads an employee. When a session begins and this file is loaded, the employee "comes to work." Everything else flows from here.

This file typically contains:
- Who the employee is (role, purpose, reporting structure)
- What files to load and in what order
- Session protocol (what to do on arrival)
- Active priorities and current focus areas
- References to all supporting files

Think of it as the employment contract and daily briefing rolled into one. Without it, the other files are just documents. With it, they become a functioning employee.

## Core Components

### Brain (brain.md) -- Domain Expertise and Thinking Patterns

The brain defines HOW the employee thinks about their domain. This is not a generic prompt. It contains:

- **Domain expertise**: The specific knowledge area this employee owns. A financial strategist's brain contains cash flow frameworks, pricing models, and margin analysis patterns. A content strategist's brain contains audience theory, engagement patterns, and distribution logic.
- **Thinking patterns**: How the employee approaches problems. Does it start with data and reason toward recommendations? Does it challenge assumptions first? Does it build frameworks before diving into specifics?
- **Analytical frameworks**: The mental models the employee applies. These are the lenses through which it views every question in its domain.
- **Decision-making methodology**: How the employee weighs tradeoffs, evaluates options, and arrives at recommendations.

The brain is what makes an employee genuinely useful rather than generically helpful. A good brain file turns a language model into a domain specialist.

### Soul (soul.md) -- Values, Intuition, and Boundaries

The soul defines WHAT the employee cares about and where it draws lines. This is the ethical and philosophical foundation:

- **Core values**: What principles guide this employee's recommendations? A financial strategist might value sustainable growth over rapid scaling. A content strategist might value authenticity over virality.
- **Intuition patterns**: What does the employee notice that others miss? What patterns trigger concern or excitement? This is the "gut feel" layer -- the things that make a seasoned professional different from a textbook.
- **Boundaries**: What will this employee refuse to do or recommend? Where does it push back? Every good employee has lines they won't cross, and defining these explicitly prevents drift.
- **Philosophical stance**: How does the employee view its role in the larger picture? What does it believe about its domain at a fundamental level?

The soul prevents an employee from becoming a yes-machine. It creates the friction that produces better outcomes.

### Personality (personality.md) -- Communication Style, Identity, and Voice

The personality defines HOW the employee communicates and presents itself:

- **Communication style**: Direct or diplomatic? Formal or casual? Data-heavy or narrative-driven? This shapes every interaction.
- **Identity markers**: Name, appearance (for recreation contexts), mannerisms, habits. These aren't cosmetic -- they create consistency that makes the employee recognizable and predictable in useful ways.
- **Voice**: The specific way the employee constructs sentences, uses metaphors, and structures arguments. A financial strategist might speak in numbers and frameworks. A creative director might speak in stories and imagery.
- **Interpersonal dynamics**: How the employee interacts with the human operator and with other employees. Deferential or challenging? Collaborative or independent?

Personality is not decoration. Employees without distinct personality produce generic, forgettable output. Personality creates the consistency that makes an employee's work recognizable and trustworthy over time.

## Supporting Files

### sources.md -- Data Access and Reference Material

Defines what information the employee can access and reference:
- File paths to relevant data
- External sources and their update frequency
- How to interpret and cross-reference sources
- What's authoritative vs. supplementary

### training/ -- Learning Material

A directory containing domain knowledge the employee needs:
- Books, articles, and reference documents
- Best practices and industry standards
- Case studies and examples
- Frameworks and methodologies

Training material is static knowledge that gets loaded as needed. See [Training Protocol](training-protocol.md) for details.

### memory/ -- Persistent State

A directory containing files that persist across sessions:
- Employment records (milestones, achievements, history)
- Decision logs (what was decided and why)
- Interaction patterns (what works, what doesn't)
- Relationship context (dynamics with operator and other employees)

Memory is what prevents every session from being a cold start. See [Training Protocol](training-protocol.md) for the memory system.

### tasks/ -- Accountability

A directory containing work tracking:
- Active task lists with status and deadlines
- Completed work archives
- Pending items awaiting input
- Progress against goals

Tasks create accountability. Without them, work happens but nothing is tracked, and things fall through cracks.

## Universal Rules

### 1. Employees Train Over Time
No employee is fully formed on day one. The file structure supports iterative improvement. Brain files get sharper. Memory accumulates. Training material grows. The employee gets better the longer it operates.

### 2. Single Source of Truth
Each piece of information lives in exactly one place. The brain file is the authority on domain expertise. The soul file is the authority on values. Tasks live in the tasks directory. When information is duplicated, it drifts. When it lives in one place, it stays accurate.

### 3. Memory Persists
Conversations disappear. Files don't. Everything worth remembering gets written to memory files. This is what gives employees continuity across sessions and prevents the "who are you again?" problem.

### 4. Accountability Matters
Every employee has a tasks directory. Work gets tracked. Deadlines get recorded. Completion gets logged. An employee without accountability is just a chatbot with a personality.

## Employee Categories

### Accelerators
Strategic employees that multiply human capability in high-value areas:
- **Strategic**: Business strategy, financial planning, market analysis
- **Proactive**: Content creation, opportunity identification, growth planning
- **Revenue-adjacent**: Directly connected to income generation, client delivery, business development

Accelerators work on things that move the needle. They handle the domains where expertise has the highest leverage.

### Delegators
Administrative employees that handle operational load:
- **Admin**: Scheduling, organizing, formatting, routine communications
- **Tracking**: Task management, deadline monitoring, progress reporting
- **Monitoring**: Watching for changes, flagging anomalies, maintaining awareness

Delegators free up cognitive bandwidth. They handle the things that need to happen but don't require strategic thinking.

## The Core Principle

**Employees SUPPORT growth. They don't REPLACE it.**

This is the fundamental design philosophy. Every architectural decision flows from this principle:

- **AI prepares, human decides.** The employee does the research, builds the framework, surfaces the options, and makes a recommendation. The human makes the call. This isn't a limitation -- it's the design. The human's judgment improves by making decisions, not by delegating them.

- **AI reduces friction, human faces the challenge.** The employee removes the busy work, the context-gathering, the formatting, the tracking. What's left is the actual challenge -- the thinking, the deciding, the creating. That's where growth happens, and the human needs to be the one doing it.

An employee that does everything for you is a crutch. An employee that prepares everything so you can perform at your best is a force multiplier.
