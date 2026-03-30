## Michael Winczuk

**Retired U.S. Marine MSgt | Agentic AI Engineer | Rust + Python**

I build multi-agent AI systems with safety guarantees. 20 years of military service taught me that complex systems succeed or fail based on their ability to self-correct under pressure. I apply that to AI agent infrastructure — consensus, verification, audit trails, self-healing.

---

### Shipped Work

**[Bastion](https://github.com/michaelwinczuk/bastion)** — Safety kernel for agentic AI. Multi-model consensus gating, deterministic verification (no LLM calls on the critical path), SHA-256 hash-chained audit trails, checkpoint/rollback, self-healing decision trees. Rust + Tokio.
[![CI](https://github.com/michaelwinczuk/bastion/actions/workflows/ci.yml/badge.svg)](https://github.com/michaelwinczuk/bastion/actions/workflows/ci.yml)

**[Prism](https://github.com/michaelwinczuk/prism)** — Reliability primitives for multi-agent systems. VotingMesh consensus (215K ops/sec with 3 agents), Sentinel safety pipeline, Aegis exchange compliance (wash trading/spoofing detection), checkpoint/replay with divergence detection. Rust + Tokio + Python bindings via PyO3. 95 tests.
[![CI](https://github.com/michaelwinczuk/prism/actions/workflows/ci.yml/badge.svg)](https://github.com/michaelwinczuk/prism/actions/workflows/ci.yml)

**[Parameter Golf — SOTA](https://github.com/michaelwinczuk/parameter-golf)** — Beat the OpenAI Parameter Golf leaderboard. 3-seed mean **0.3958 BPB** (std 0.0011), improving on prior best of 0.4416 by 0.0458. Causal BackoffNgramMixer architecture. [PR #1094](https://github.com/KellerJordan/modded-nanogpt/pull/1094).

### What I Build

I design multi-agent architectures where agents can't act without passing through a safety pipeline:

```
Action proposed
    |
Guardrails (spending limits, dangerous patterns, human-in-loop)
    |
Multi-model consensus (N agents must agree)
    |
Checkpoint state
    |
Execute
    |
Deterministic verification (hallucination detection, confidence checks)
    |
Pass: commit  |  Fail: rollback + self-heal
    |
SHA-256 hash-chained audit trail
```

All safety checks are deterministic — sub-millisecond overhead, zero LLM calls in the critical path.

### Tech

```
Languages:    Rust, Python, TypeScript
Safety:       Consensus gating, checkpoint/rollback, hash-chained audit, self-healing
Runtime:      Tokio async, PyO3 bindings, native binaries
AI:           Claude, GPT-4o, Phi-3 (local inference)
Data:         Knowledge graphs (330K nodes), BM25 search, mmap binary graphs
Infra:        PostgreSQL, Redis, GitHub Actions CI
```

### Contact

Open to remote roles in agentic AI, multi-agent systems, AI safety/reliability, or Rust + Python engineering.

[GitHub](https://github.com/michaelwinczuk) · [@smartcontr67332](https://x.com/smartcontr67332)
