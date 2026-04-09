## Michael Winczuk

**Retired U.S. Marine MSgt | Agentic AI Engineer | Rust + Python**

I build multi-agent AI systems that replace LLM guesswork with deterministic computation. 20 years of military service taught me that complex systems succeed or fail based on their ability to self-correct under pressure. I apply that to AI agent infrastructure — verified computation, consensus, audit trails, self-healing.

---

### Flagship: Math Swarm — Zero-Hallucination Computation

**[Math Swarm](https://github.com/michaelwinczuk/math-swarm)** — Replaces LLM token prediction with SymPy symbolic computation. **1,079 tests, 12 categories, 100% accuracy, $0 cost.**

| System | Math Accuracy | Speed | Size |
|--------|-------------|-------|------|
| **Math Swarm** | **1,079/1,079 (100%)** | **1.9ms** | SymPy |
| Qwen2.5-3B alone | 52/94 (55%) | 200ms | 1.8 GB |
| Qwen2.5-7B alone | 72/94 (77%) | 300ms | 4.4 GB |
| Qwen2.5-32B alone | 87/94 (93%) | 2,600ms | 18.5 GB |

**A 3B model + Math Swarm outperforms a 32B model alone at math.** Scaling parameters doesn't fix computation — architecture does.

Includes 15 clinical healthcare formulas (BMI, eGFR, MELD, QTc, Cockcroft-Gault, anion gap, pediatric dosing) with guideline-based clinical decision support. Every interpretation sourced from KDIGO, AHA, FDA, WHO guidelines. Zero LLM involvement in computation or interpretation.

---

### Shipped Work

**[Math Swarm](https://github.com/michaelwinczuk/math-swarm)** — Zero-hallucination computation engine. 6-agent SymPy pipeline. 1,079 tests across arithmetic, finance, trig, combinatorics, statistics, healthcare. Benchmarked against 3B/7B/32B models. Clinical decision support with 15 medical formulas.

**[Swarm Orchestrator](https://github.com/michaelwinczuk/swarm-orchestrator)** — Claude Agent Skill for designing multi-agent systems. 8 archetypes, 5 communication patterns, deterministic-first cascade, chalkboard protocol. Patterns validated across 5+ production swarms.

**[Knowledge Graph Reasoning](https://github.com/michaelwinczuk/knowledge-graph-reasoning)** — Claude Agent Skill for building and reasoning over knowledge graphs. 77 graphs deployed across 69 domains. Adversarial 4-check validation. $0/query deterministic reasoning.

**[Bastion](https://github.com/michaelwinczuk/bastion)** — Safety kernel for agentic AI. Multi-model consensus gating, deterministic verification, SHA-256 hash-chained audit trails, checkpoint/rollback, self-healing. Rust + Tokio.
[![CI](https://github.com/michaelwinczuk/bastion/actions/workflows/ci.yml/badge.svg)](https://github.com/michaelwinczuk/bastion/actions/workflows/ci.yml)

**[PRISM](https://github.com/michaelwinczuk/prism)** — Reliability primitives for multi-agent systems. VotingMesh consensus (215K ops/sec), Sentinel safety pipeline, Aegis compliance, checkpoint/replay. Rust + Tokio + PyO3. 95 tests.
[![CI](https://github.com/michaelwinczuk/prism/actions/workflows/ci.yml/badge.svg)](https://github.com/michaelwinczuk/prism/actions/workflows/ci.yml)

**[Parameter Golf — SOTA](https://github.com/michaelwinczuk/parameter-golf)** — Beat the OpenAI Parameter Golf leaderboard. 3-seed mean **0.3958 BPB** (std 0.0011), improving on prior best of 0.4416 by 0.0458. [PR #1094](https://github.com/KellerJordan/modded-nanogpt/pull/1094).

### What I Build

Multi-agent systems where deterministic computation replaces LLM guesswork:

```
User query
    |
LLM: parse intent (ONLY job)
    |
Router: what domain?
    |--- Math?       -> SymPy (100% accuracy, 1.9ms, $0)
    |--- Facts?      -> Knowledge Graph (77 graphs, deterministic)
    |--- Logic?      -> Reasoning Brain (6 primitives, $0)
    |--- Healthcare? -> Clinical formulas + guideline lookup
    |--- Language?   -> LLM (stays here)
    |
Safety pipeline: consensus, verification, audit trail
    |
LLM: format verified results (ONLY job)
```

### Tech

```
Languages:    Rust, Python, TypeScript
Compute:      SymPy (symbolic math), deterministic pipelines
Safety:       Consensus gating, checkpoint/rollback, hash-chained audit
Runtime:      Tokio async, PyO3 bindings, MCP servers (11 deployed)
AI:           Claude, GPT-4o, Qwen 3B/7B (local), fine-tuning (QLoRA)
Knowledge:    77 knowledge graphs, BM25 search, 69 cluster domains
Infra:        Alienware (RTX 5070) + desktop, Redis, GitHub Actions
```

### Contact

Building at [Swarm Labs USA](https://swarmlabsusa.com) — autonomous AI systems for government and healthcare.

[GitHub](https://github.com/michaelwinczuk) · [@smartcontr67332](https://x.com/smartcontr67332)
