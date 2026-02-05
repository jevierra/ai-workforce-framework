# Training Protocol: How Employees Learn

## Training Folder Structure

Every employee has a `training/` directory that contains domain knowledge organized by type:

```
employee-name/
  training/
    books/              # Key texts and reference material
    frameworks/         # Mental models and analytical approaches
    best-practices/     # Industry standards and proven methods
    case-studies/       # Examples and precedents
    domain-knowledge/   # Specialized information for the role
```

Not every employee needs every subdirectory. A financial strategist might have extensive `frameworks/` and `books/` directories. A task tracker might have minimal training beyond `best-practices/`. The structure adapts to the role.

## Adding Domain Knowledge

### Books and Reference Material

When an employee needs expertise from a specific source:

1. Distill the key concepts, frameworks, and principles into a markdown file
2. Focus on actionable knowledge, not summaries -- what would a practitioner extract?
3. Include specific methodologies, formulas, or decision criteria the employee should apply
4. Place in `training/books/` with a clear filename: `profit-first-methodology.md`

The goal isn't to reproduce the source. It's to give the employee the working knowledge a human would retain after reading it and applying it for years.

### Frameworks and Mental Models

Analytical frameworks go in `training/frameworks/`:

```markdown
# Cash Flow Forecasting Framework

## When to Apply
- Monthly financial reviews
- Pre-decision analysis for major expenses
- Client financial health assessments

## Method
1. Start with trailing 3-month average revenue
2. Identify committed expenses (non-negotiable)
3. Calculate discretionary margin
4. Stress test at 80% and 60% revenue scenarios
5. Recommend based on worst-case sustainability

## Key Principles
- Conservative projections protect against optimism bias
- Separate committed from discretionary before any analysis
- Always present the "what if revenue drops" scenario
```

### Best Practices

Proven patterns for the employee's domain:

```markdown
# Content Publishing Best Practices

## Scheduling
- Publish consistently over publishing frequently
- Audience engagement peaks vary by platform
- Batch creation, scheduled distribution

## Quality Signals
- Every piece answers a specific question
- Personal experience outperforms generic advice
- Data points add credibility; stories add memorability
```

### Case Studies

Real examples the employee can reference and learn from:

```markdown
# Pricing Revision - Q3 Client Engagement

## Situation
Client requested 40% scope increase with no budget adjustment.

## Analysis Applied
- Calculated true cost of expanded scope
- Identified which additions had highest client value
- Proposed tiered options rather than binary yes/no

## Outcome
Client selected mid-tier option at 25% budget increase.
Preserved relationship while maintaining margin.

## Lesson
Never present scope changes as all-or-nothing.
Tiered options give clients agency and protect your economics.
```

## The Memory System

Memory is distinct from training. Training is domain knowledge that doesn't change often. Memory is accumulated experience from actual work.

### memory/employment-records/

Milestones and history that define the employee's journey:

```markdown
# Employment Record

## Hire Date
2025-01-15

## Key Milestones
- 2025-01-15: Initial deployment. Core brain and soul files established.
- 2025-02-01: First major financial analysis delivered. Pricing framework validated.
- 2025-02-20: Training expanded with Profit First methodology.
- 2025-03-10: Memory system formalized. Decision logging begins.
```

This gives the employee a sense of history and progression. When it loads this file, it knows where it's been and how it has evolved.

### memory/decision-logs/

The most valuable memory files. Every significant decision gets captured:

```markdown
# Decision Log Entry

## Date
2025-03-15

## Decision
Set Q2 content cadence at 2x per week instead of daily.

## Context
Daily publishing was creating quality pressure. Analytics showed
engagement per piece was declining as volume increased.

## Rationale
- Quality per piece matters more than volume at current audience size
- 2x weekly allows deeper research and better production value
- Frees 3 days/week for client work (higher immediate revenue)

## Outcome
Engagement per piece increased 40% within 3 weeks.
Total reach declined 15% but qualified engagement improved.

## Lesson
At small scale, attention per piece beats volume.
Revisit when audience exceeds threshold for volume strategy.
```

Decision logs are gold. They capture not just what was decided but WHY, what the alternatives were, and what happened. This prevents re-litigating past decisions and builds genuine institutional knowledge.

### memory/interaction-patterns/

What works and what doesn't in the employee's interactions:

```markdown
# Interaction Patterns

## Effective Approaches
- Leading with data before recommendations increases acceptance
- Presenting 3 options (conservative, moderate, aggressive) works better
  than single recommendations
- Flagging risks early builds trust even when news is unwelcome

## Adjustments Made
- Reduced jargon in financial summaries after feedback
- Added "bottom line" section to all analyses for quick scanning
- Started including confidence levels with projections
```

## How Knowledge Compounds Over Time

The compounding effect is the core advantage of this architecture:

**Week 1**: Employee has brain file and basic training. Output is competent but generic. It's applying frameworks without context.

**Month 1**: Decision logs capture early choices and outcomes. Training material has been refined based on what's actually useful. The employee starts referencing past decisions in new recommendations.

**Month 3**: Memory is substantial. The employee knows what's been tried, what worked, what didn't, and why. Interaction patterns are tuned. Training reflects real domain needs, not theoretical ones. Output quality has noticeably improved.

**Month 6+**: The employee has genuine institutional knowledge. It can reference patterns across dozens of decisions. Its recommendations account for history, preferences, and learned lessons. A new session with a well-trained employee feels like picking up a conversation with a knowledgeable colleague, not starting from scratch.

This compounding is the reason the file-based architecture matters. Every session that adds to memory or refines training makes every future session better.

## Session Loading: Coming to Work

When an employee starts a session, it follows a loading protocol -- the equivalent of arriving at work and getting oriented:

1. **Load identity**: instructions.md, brain.md, soul.md, personality.md establish who the employee is
2. **Load context**: memory files provide history and continuity
3. **Review active tasks**: tasks/ directory shows what's in progress, what's due, what's stale
4. **Surface attention items**: Based on tasks and memory, identify what needs focus today
5. **Confirm readiness**: Brief the human on current state and recommended priorities

This protocol prevents cold starts. Instead of "how can I help you today?" the employee arrives knowing what's happening, what matters, and what it should be thinking about.

The session loading protocol turns every interaction into a continuation rather than a restart. This is where the persistent file architecture pays its highest dividends.

## Key Insight

AI employees don't learn like humans. They don't have genuine memory formation, intuition development, or experience accumulation in the biological sense.

But structured knowledge files create the EFFECT of accumulated expertise.

When an employee loads a decision log with 50 entries spanning 6 months, it can identify patterns, reference precedents, and make recommendations informed by history. When it loads refined training material that's been iteratively improved, it applies sharper frameworks than it could on day one.

The files are the learning. The structure is the curriculum. The consistency of the format is what makes it compound. This is artificial expertise -- and it's remarkably effective when built with discipline.
