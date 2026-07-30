<p align="center">
  <a href="https://www.getzep.com/">
    <img src="https://github.com/user-attachments/assets/119c5682-9654-4257-8922-56b7cb8ffd73" width="150" alt="Zep Logo">
  </a>
</p>

<h1 align="center">Zep Cloud: Examples & Integrations</h1>

<p align="center">
  <a href="https://discord.gg/W8Kw6bsgXQ"><img
    src="https://img.shields.io/badge/Discord-%235865F2.svg?&logo=discord&logoColor=white"
    alt="Chat on Discord"
  /></a>
  <a href="https://twitter.com/intent/follow?screen_name=zep_ai" target="_new"><img alt="Twitter Follow" src="https://img.shields.io/twitter/follow/zep_ai"></a>
</p>

## About This Repository

This repository is **not** Zep's product or service. It contains **example code, framework
integrations, and tools** for building agent memory with [Zep Cloud](https://www.getzep.com/),
Zep's managed agent memory platform.

To use Zep Cloud, sign up at [www.getzep.com](https://www.getzep.com/) and read the
documentation at [help.getzep.com](https://help.getzep.com). Zep's official SDKs are:

- **Python**: `pip install zep-cloud`
- **TypeScript/JavaScript**: `npm install @getzep/zep-cloud`
- **Go**: `go get github.com/getzep/zep-go/v3`

> Looking for the open-source temporal knowledge graph framework that powers Zep? See
> [Graphiti](https://github.com/getzep/graphiti).

## Contents

| Directory | Description |
|-----------|-------------|
| [`examples/`](examples/) | Example apps and snippets in Python, TypeScript, and Go |
| [`integrations/`](integrations/) | Agent-framework integration packages |
| [`ingestion/`](ingestion/) | `zep-ingest` — bulk data ingestion pipeline (Slack, documents, email, JSON/CSV, fact triples) |
| [`ontology/`](ontology/) | Default ontology definitions |
| [`plugins/`](plugins/) | Plugins for building with Zep |
| [`benchmarks/`](benchmarks/) | Memory benchmarks (LoCoMo, LongMemEval) |
| [`zep-eval-harness/`](zep-eval-harness/) | Evaluation harness for ingestion and retrieval |
| [`legacy/`](legacy/) | Deprecated Zep Community Edition (unsupported) |

## Python Examples (`examples/python`)

Reference implementations demonstrating Zep's memory features from an application-usage perspective:

- **`simple.py`** — A shoe-shopping support bot showing a customer's brand preference change
  over time (Adidas → Puma), illustrating that memory updates as preferences evolve rather than
  staying stuck on the first thing said.
- **`advanced.py`** — A travel-planning assistant across four real-world trip scenarios (a
  culinary trip with a spouse, an adventure trip with a friend, a business trip with a
  colleague, a multi-generational family reunion), tracking who's who, individual preferences,
  and bookings — including a customer whose food preferences later reverse.
- **`user_example.py`** — Basic account administration: creating, updating, and removing
  customer profiles.
- **`chat_history/`** — Replays a scripted customer-support conversation (shoe shopping with
  sizing/budget/pronation details) and summarizes the customer's needs from it.
- **`graph_example/`** — Five demos showing free-form info (chat messages, JSON records, notes)
  organized into a queryable knowledge graph: a business/leisure travel tracker, a concert
  ticket-sales bot (searches, purchases, waitlists), and a general "ask the memory about X" tour.
- **`quickstart/quickstart.ipynb`** — Flagship demo: a support bot automatically pulls in a
  customer's billing/account history from unrelated past sessions when she reports a new issue,
  without her needing to re-explain anything.
- **`autogen-agent/agent.ipynb`** — A mental-health check-in bot that remembers emotionally
  significant details from past sessions (rated by significance, not just recency) and raises
  them naturally when the user returns.
- **`langgraph-agent/agent.ipynb`** — A supportive counselor bot that stays grounded across a
  long conversation, correctly recalling earlier topics (a stressful work situation, a sick pet)
  even after the conversation has moved on.
- **`zep-quickstart-dashboard/`** — An interactive real-estate assistant dashboard comparing
  responses with vs. without memory, side by side, with latency stats.
- **`context-templates-example/`** — Same real-estate assistant, showing how the shape/format of
  the memory summary shown to the assistant can be customized.
- **`user-summary-instructions-example/`** — Same real-estate assistant, showing "standing
  questions" (budget, bedrooms, must-haves) that stay answered even if mentioned only once.
- **`agent-memory-full-example/`** — A fuller, ready-to-run chatbot template with sample
  pre-loaded conversation data.
- **`chunking-example/`** — Document ingestion demo: enriches document sections with contextual
  summaries before storage so later searches return more relevant results.
- **`claude-prompt-caching-example/`** — Compares two ways of feeding memory into Claude,
  showing one approach keeps long conversations getting cheaper/faster while the naive approach
  doesn't.
- **`openai-agents-sdk/`** — The same "remembers you across sessions" assistant, built on
  OpenAI's agent framework instead.
- **`elevenlabs-zep-example/`** — A voice assistant that remembers who you are and prior
  discussions, with memory lookups happening invisibly so they don't disrupt natural speech.

## Integrations

Framework integration packages live under [`integrations/`](integrations/), organized
framework-first then language: `integrations/<framework>/<language>/`. Each package is built,
tested, and released independently.

- **Python**: Google ADK, Microsoft Agent Framework, Microsoft AutoGen, AG2, CrewAI, LangGraph, LiveKit, Pydantic AI
- **TypeScript**: Google ADK, Mastra, Vercel AI SDK
- **Go**: Google ADK


See [`integrations/README.md`](integrations/README.md) for packages, release status, and
links, and [`integrations/CLAUDE.md`](integrations/CLAUDE.md) for conventions.

## Contributing

We welcome contributions. See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines covering code,
documentation, bug reports, and community examples.

## Community Edition (Deprecated)

Zep Community Edition is no longer supported. Its code has been moved to the
[`legacy/`](legacy/) folder. Read more in
[Announcing a New Direction for Zep's Open Source Strategy](https://blog.getzep.com/announcing-a-new-direction-for-zeps-open-source-strategy/).
