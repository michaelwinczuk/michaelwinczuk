## Michael Winczuk

**Retired Marine | Rust Principal Engineer | AI Swarm Architect**

20 years of service taught me one thing: complex systems succeed or fail based on their ability to self-correct under pressure. I build AI agent infrastructure that does exactly that.

---

### Latest: OpenAI Parameter Golf — Beat the SOTA

My think tank swarm discovered that changing one hyperparameter (`LeakyReLU negative_slope=0.5` → `0.75`) improves the SOTA by **0.008 BPB**. Nobody in the competition's 50+ submissions had swept this parameter.

**Result: 1.1185 BPB mean across 3 seeds** (vs SOTA 1.1194). [Submission PR #977](https://github.com/openai/parameter-golf/pull/977).

How it was found: 8 specialist AI agents traversing competition-specific knowledge graphs (264 nodes, 122 typed edges), validated by Grok, Claude Opus, and Gemini. The Visionary agent flagged the opportunity. I designed the system, directed the research, and ran the experiments.

---

### What I Build

**[Bastion](https://github.com/michaelwinczuk/bastion)** — Open-source production kernel for agentic AI. Multi-model consensus, self-healing pipelines, deterministic checkpoints, immutable audit trails.

**[Prism](https://github.com/michaelwinczuk/prism)** — Production reliability layer. VotingMesh consensus, checkpoint recovery, CodeForge generation. Native Rust + Tokio core with Python bindings via PyO3.

**The Think Tank Swarm** — Multi-agent research system with 8 specialist personalities, adversarial Alpha/Omega deliberation, 145K+ node knowledge graphs, ontological inference, and live research claws. Zero API calls in experimental mode.

### The Swarm Architecture

```
Messenger decomposes the mission into objectives
     |
Environment maps the landscape
     |
8 Edge-Type Specialists (causes, solves, contradicts, tradeoff, systems, visionary...)
     |
Mission-specific knowledge graphs (isolated from 500K+ general nodes)
     |
Ontological Reasoner (transitive relationship discovery)
     |
Synthesis + Benchmark scoring
```

Every agent has a machine-readable cartridge (JSON-LD), gets benchmarked after every mission, and has a dedicated Mechanic that adjusts parameters based on performance.

### Tech Stack

```
Languages:    Rust, TypeScript, Python
Runtime:      Tokio (async), native binaries — no containers
AI Routing:   Claude Sonnet/Opus, GPT-4o (API-only)
Data:         JSON-LD knowledge graphs, BM25 search, binary mmap graphs
Infra:        PostgreSQL, Redis, RabbitMQ, Railway
```

### Contact

Open to roles in agentic AI infrastructure, distributed systems, Rust engineering, or AI efficiency research.

[GitHub](https://github.com/michaelwinczuk) · [@smartcontr67332](https://x.com/smartcontr67332)
