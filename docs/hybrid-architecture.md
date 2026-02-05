# Hybrid Architecture: Future-State Local + Frontier Design

## Core Principle

API costs matter. Autonomous agents burn tokens fast.

Every API call to a frontier model costs money. A single complex analysis might consume thousands of tokens. An autonomous agent running continuously can burn through meaningful budget in hours. For solo operators and small teams, this isn't a minor concern -- it's a structural constraint that shapes what's viable.

The hybrid architecture addresses this by matching model capability to task requirements. Not everything needs frontier-level reasoning. Not everything can run on a local model. The right architecture puts the right model on the right task.

## The Three Layers

### Layer 1: Employees on Frontier Models (Claude, GPT-4 class)

**What runs here**: High-stakes work that requires peak reasoning, nuanced judgment, and deep context understanding. This is where AI employees live -- the strategic advisors, financial analysts, content strategists, and domain experts.

**Why frontier**: These tasks involve complex reasoning chains, subtle tradeoffs, ambiguous situations, and the kind of nuanced judgment where model quality directly impacts output quality. The difference between a frontier model and a mid-tier model on a complex financial analysis is significant and measurable.

**Cost profile**: Pay-per-use via API. Expensive per token but used in focused, high-value sessions. The human-in-the-loop model naturally limits token consumption because the human is directing the work, not the model.

**Key characteristic**: Human in the chair. The operator drives these sessions, which means token usage is bounded by human attention span and decision cadence. This is where the employee model has a natural cost advantage over autonomous agents -- humans don't process at API speed, so token burn is manageable.

### Layer 2: Document Processing on Large-Context Models (Gemini class)

**What runs here**: Volume work that exceeds standard context windows. Processing entire books for training material extraction. Analyzing large document sets. Ingesting extensive research material. Cross-referencing large bodies of text.

**Why large-context**: Some tasks aren't complex in reasoning but are massive in volume. Processing a 300-page book to extract actionable frameworks doesn't require frontier reasoning -- it requires a large context window and good extraction capability. This is where models optimized for large context windows provide the best cost-to-capability ratio.

**Cost profile**: Typically lower per-token than frontier models, designed for high-volume input processing.

**Key characteristic**: Batch processing. These aren't interactive sessions. They're processing jobs that take a large input and produce a structured output. Load the document, run the extraction, get the result. Minimal back-and-forth.

### Layer 3: Autonomous Scouts on Local Models (Ollama)

**What runs here**: 24/7 monitoring, filtering, triage, and pattern matching. Watching RSS feeds for relevant content. Monitoring financial data for threshold breaches. Scanning emails for urgency signals. Checking task lists for staleness.

**Why local**: After the initial hardware cost, every query is free. A local model running continuously costs electricity, not API fees. For tasks that need constant attention but not genius-level reasoning, this is the economically obvious choice.

**Cost profile**: $0 per query after hardware investment. Electricity costs are negligible compared to API pricing at equivalent query volumes.

**Key characteristic**: Always on. These models run continuously on dedicated hardware, watching and filtering. They don't need to be brilliant. They need to be reliable, fast, and free.

## System Architecture Flow

```
                    HUMAN OPERATOR
                         |
                         v
            +------------------------+
            |   Frontier Employees   |
            |   (Claude / GPT-4)     |
            |                        |
            |  Strategic analysis    |
            |  Complex reasoning     |
            |  Domain expertise      |
            |  Decision support      |
            +------------------------+
                    ^         ^
                    |         |
          Escalation|         |Processed docs
                    |         |
     +--------------+    +----+-----------+
     |  Local Scouts |    | Large-Context  |
     |  (Ollama)     |    | Processing     |
     |               |    | (Gemini)       |
     | Monitoring    |    |                |
     | Filtering     |    | Book ingestion |
     | Triage        |    | Doc analysis   |
     | Alerting      |    | Bulk extraction|
     +--------------+    +----------------+
           |
           v
    [Data feeds, files,
     emails, markets,
     task lists, logs]
```

**The flow**:
1. Local scouts monitor data sources continuously
2. When something requires attention, scouts escalate to frontier employees or flag for the human
3. Large-context models process bulk documents and feed structured output into employee training files
4. Frontier employees operate in interactive sessions with the human, armed with pre-processed intelligence from both other layers
5. The human makes decisions, employees record them, and the cycle continues

## Hardware Separation

**Dedicated machine for local models**: A separate machine (or dedicated partition) runs Ollama and local models. This keeps resource usage isolated -- local model inference is CPU/GPU intensive and shouldn't compete with the operator's main work environment.

**Main machine for employees**: The operator's primary machine runs frontier employee sessions through API calls. These are network requests, not local compute, so they add negligible resource load.

This separation ensures that 24/7 monitoring doesn't degrade the operator's interactive experience, and that employee sessions aren't competing for compute with local inference.

## What Local Models Handle Well

- **Monitoring**: Watching data feeds, file changes, market movements. Simple pattern detection on continuous streams.
- **Filtering**: Separating signal from noise. "Is this email urgent?" "Does this article match our content criteria?" "Has this metric crossed a threshold?"
- **Triage**: Categorizing incoming information by type, urgency, and routing. "This goes to the financial strategist. This goes to the content pipeline. This can wait."
- **Pattern matching**: Detecting known patterns in data. Not discovering new patterns -- recognizing established ones.
- **Repetitive extraction**: Pulling structured data from consistent formats. Invoice processing, data normalization, format conversion.

## Where Local Models Struggle

- **Complex reasoning**: Multi-step logical chains with ambiguity. When the answer requires weighing subtle tradeoffs, local models produce noticeably inferior results.
- **Nuanced judgment**: Situations where context, tone, and implication matter as much as explicit content. Client communication, strategic recommendations, risk assessment.
- **Novel situations**: Problems that don't match established patterns. Local models excel at applying known patterns; they struggle when the pattern doesn't exist yet.

**The answer for all of these: Escalate to frontier.** Local models should know their limits and push anything complex upward. A well-designed local scout is valuable precisely because it knows what it can't handle.

## Tech Stack

### Ollama for Simplicity
Ollama provides the simplest path to running local models. Single install, straightforward model management, API-compatible interface. No complex infrastructure required.

### Model Selection
- **Mistral**: Strong general-purpose performance for its size. Good for monitoring and triage tasks.
- **Llama**: Meta's open models. Solid reasoning for local inference, multiple size options.
- **Phi**: Microsoft's small models. Excellent performance-to-size ratio for constrained hardware.

The specific model matters less than the architecture. As local models improve (and they improve rapidly), the same scout framework runs better models without structural changes.

## Connection Options

Local scouts need to communicate results to the broader system. Several patterns work:

### Shared Folders
The simplest approach. Local scouts write findings to markdown files in shared directories. Employees read those files during session loading. Low-tech, reliable, easy to debug.

### Git Repos
Scouts commit findings to a shared repository. Employees pull updates. Adds version control and history to the communication layer. Slightly more complex but more robust for multi-machine setups.

### Webhooks
Scouts send HTTP notifications when they detect something requiring attention. More real-time than file-based approaches. Requires a receiving endpoint but enables immediate escalation.

The right choice depends on urgency requirements. Most monitoring can tolerate minutes of latency, making shared folders perfectly adequate. Time-sensitive alerting benefits from webhooks.

## The Key Insight

The `.md` architecture stays universal regardless of which model runs it.

A brain file is a brain file whether it's loaded by Claude, GPT-4, Gemini, Llama, or Mistral. The employee structure doesn't depend on any specific model or provider. This is a deliberate design choice that provides:

- **Model portability**: Switch providers without restructuring employees
- **Future-proofing**: As models improve, employees automatically benefit
- **Cost flexibility**: Move tasks between tiers as pricing changes
- **Risk reduction**: No single-provider dependency

The markdown files are the source of truth. The model is the runtime. The architecture works because it separates knowledge from execution.
