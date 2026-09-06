# Career Path Map — Shared Core → Multiple High-Impact Paths

**Created:** 2026-09-06  
**Purpose:** Connect the existing Data Science, Engineering Career, and Frontier AI roadmaps into one decision map so learning stays coherent rather than becoming a collection of disconnected technologies.

> The objective is optionality: build a strong shared foundation first, then specialize based on demonstrated strengths, interests, job-market evidence, and real-world impact.

---

## 1. The Shared Core

All major paths start from largely the same foundation:

```text
Accounting / Finance Domain
          ↓
Python + SQL + Data Modeling
          ↓
Linear Algebra + Calculus
          ↓
Probability + Statistics
          ↓
Machine Learning
          ↓
Software Engineering
          ↓
Experimentation + Evaluation
          ↓
Production Systems
```

### Shared exit criteria

- [ ] Strong Python and SQL
- [ ] DS&A fundamentals
- [ ] Probability and statistical inference
- [ ] Regression and classical ML
- [ ] Experimental design
- [ ] Git / testing / CI
- [ ] PostgreSQL and data modeling
- [ ] APIs and backend fundamentals
- [ ] Docker / Linux
- [ ] Cloud fundamentals
- [ ] Ability to explain technical decisions without relying on generated wording
- [ ] 2–3 deep flagship repositories rather than many shallow demos

---

# 2. Career Branches

```text
                         SHARED CORE
                              │
        ┌─────────────┬───────┼────────┬──────────────┐
        ↓             ↓       ↓        ↓              ↓
 AI Research      AI Systems Decision  AI Governance FinTech /
 Engineering      / Agents   Science   / Evals       Quant
        │             │       │        │              │
        └─────────────┴───────┼────────┴──────────────┘
                              ↓
                    AI Decision Platforms
                              │
                       Staff+ / Founder
```

A sixth path—Cloud / Platform Engineering—can support almost every branch.

---

# Path A — AI Research Engineer

## Best fit if

You enjoy:

- mathematics
- reading papers
- designing experiments
- understanding model behavior
- reproducing results
- deep learning / transformers

## Additional skills

```text
Deep Learning
→ PyTorch
→ Transformers
→ LLM internals
→ Evals
→ Post-training
→ RL
→ Distributed ML
→ Research methodology
```

## Evidence

- Paper reproduction
- Controlled experiments
- Strong baselines
- Ablations
- Statistical analysis
- Failure analysis
- Reproducible research artifacts
- Open-source research contributions
- Research collaboration / preprint when justified

## Representative roles

- Research Engineer
- ML Research Engineer
- Applied Scientist
- Evaluation Research Engineer
- Agent Research Engineer

## Flagship project

**Coding Agent Research Environment**

```text
Benchmark
→ sandbox
→ agent
→ grader
→ traces
→ failure taxonomy
→ experiment
→ statistical analysis
```

### Path-specific gap

Research depth is more important than adding additional application frameworks.

---

# Path B — ML Systems / Agent Infrastructure

## Best fit if

You enjoy:

- architecture
- infrastructure
- performance
- reliability
- orchestration
- debugging complex systems

## Additional skills

```text
Linux
→ Networking
→ Distributed Systems
→ Cloud
→ Kubernetes
→ Observability
→ GPU fundamentals
→ Distributed ML
→ Model serving
→ Agent runtime infrastructure
```

## Evidence

- Production ownership
- Reliability metrics
- Performance profiling
- Distributed workload design
- Fault tolerance
- Cost/performance optimization
- Systems adopted by other developers

## Representative roles

- ML Systems Engineer
- AI Infrastructure Engineer
- Agent Infrastructure Engineer
- Platform Engineer
- Distributed Systems Engineer
- ML Platform Engineer

## Flagship project

**Agent Engineering Platform**

```text
Developer request
→ planner
→ orchestrator
→ isolated worktree/sandbox
→ coder/tester/reviewer
→ CI
→ evals
→ policy gate
→ approval
→ deployment
→ observability
```

### Research question

Do not assume more agents are better.

Compare:

```text
Single Agent
vs Planner/Executor
vs Multi-Agent
```

Measure success, latency, compute/token cost, retries, regressions, and human intervention.

---

# Path C — Decision Scientist / Decision Intelligence

## Best fit if

You enjoy:

- statistics
- business problems
- uncertainty
- forecasting
- causal questions
- optimization
- translating predictions into actions

## Additional skills

```text
Advanced Statistics
→ Forecasting
→ Bayesian methods
→ Causal inference
→ Experimentation
→ Optimization
→ Operations Research
→ Decision theory
```

## Core model

```text
Data
→ Prediction
→ Uncertainty
→ Decision
→ Action
→ Outcome
→ Learning
```

Prediction alone is incomplete.

## Representative roles

- Data Scientist
- Decision Scientist
- Product Data Scientist
- Forecasting Scientist
- Operations Research / Optimization roles
- Risk Data Scientist

## Flagship project

**Cloud Cost Decision Intelligence Platform**

```text
Billing
→ allocation
→ forecasting
→ uncertainty
→ anomaly detection
→ recommendation
→ approval policy
→ remediation
→ savings verification
```

Example output should evolve from:

> Next month's cost = $X

into:

> Probability of exceeding budget is 73%; action A has expected savings Y with uncertainty Z and defined operational risk.

---

# Path D — AI Governance / Evaluation / Assurance

## Best fit if

You enjoy:

- risk
- controls
- auditability
- evaluation
- policy
- evidence
- model/agent failure analysis

This path strongly compounds an Accounting / Technology Risk background.

## Existing mental model

```text
Evidence
→ Control
→ Policy
→ Audit
```

## AI version

```text
AI behavior
→ Evaluation
→ Risk classification
→ Policy
→ Human review
→ Action
→ Verification
→ Audit evidence
```

## Additional skills

- AI/ML evaluation
- Statistics
- Benchmark design
- Model risk
- Security fundamentals
- Responsible AI concepts
- Governance frameworks
- Policy-as-code
- Human-in-the-loop systems
- Evidence engineering

## Representative roles

- AI Governance Engineer
- AI Evaluation Engineer
- AI Assurance
- Model Risk / AI Risk
- Responsible AI technical roles
- Technology Risk Analytics

## Flagship project

**AI Assurance & Agent Governance Platform**

```text
Agent/model output
→ evals
→ risk score
→ policy engine
→ human review
→ execution
→ verification
→ evidence store
→ governance report
```

This is one of the clearest ways to turn accounting/audit thinking into an AI engineering differentiator.

---

# Path E — FinTech / Quantitative Engineering

## Best fit if

You enjoy:

- finance
- probability
- time series
- optimization
- markets
- financial modeling

## Additional skills

```text
Probability
→ Advanced Statistics
→ Time Series
→ Econometrics
→ Optimization
→ Financial mathematics
→ Backtesting
→ Risk modeling
```

For true Quant Research, mathematical depth must be substantially higher than ordinary analytics.

## Representative roles

- Financial Data Scientist
- Quantitative Developer
- Quantitative Analyst
- Risk Analytics
- FinTech ML Engineer
- Quant Research — longer-term reach

## Flagship project

**Research-Grade Financial Decision System**

Require:

- walk-forward validation
- transaction costs
- realistic baselines
- leakage prevention
- uncertainty
- risk-adjusted metrics
- robustness tests
- reproducibility

Avoid portfolio projects that report only a high backtest return.

---

# Path F — Cloud / Platform / Reliability Engineering

## Best fit if

You enjoy:

- operating systems
- infrastructure
- networking
- cloud
- reliability
- automation

This path naturally extends the Windows Endpoint Reliability work.

## Additional skills

```text
Linux
→ Networking
→ Cloud
→ Infrastructure as Code
→ Containers
→ Kubernetes
→ Observability
→ Distributed Systems
→ SRE
→ Security
```

## Representative roles

- Platform Engineer
- Cloud Engineer
- SRE
- Reliability Engineer
- Infrastructure Engineer
- FinOps Platform Engineer

## Flagship project

Evolve Windows Network Recovery Toolkit into:

```text
Endpoint telemetry
→ configuration drift
→ risk detection
→ automated controls
→ remediation
→ observability
→ evidence
→ fleet-level governance
```

The goal is to demonstrate platform/reliability engineering, not merely desktop troubleshooting.

---

# Path G — Founder / Technical Product Builder

## Best fit if

You increasingly enjoy:

- talking to users
- identifying painful workflows
- selling
- product design
- rapid iteration
- owning business outcomes

## Required additions

```text
Customer Discovery
→ Problem Selection
→ Product
→ Distribution
→ Sales
→ Pricing
→ Unit Economics
→ Operations
```

Technical sophistication does not automatically produce a business.

## Evidence

- users
- retention
- revenue
- reduced customer cost/time/risk
- repeatable acquisition

A useful founder path could emerge from FinOps, AI Governance, Technology Risk, or agent infrastructure if real customers demonstrate willingness to pay.

---

# 3. How the Paths Reinforce Each Other

These are not isolated careers.

## AI Research + AI Systems

```text
New model/agent idea
→ scalable implementation
→ evaluation
→ production
```

Creates a strong Research Engineer profile.

## Decision Science + FinOps

```text
Forecast
→ uncertainty
→ optimization
→ financial decision
```

Creates a differentiated financial decision profile.

## AI Evals + Governance

```text
Model behavior
→ benchmark
→ risk
→ control
→ evidence
```

Creates AI Assurance capability.

## Agents + Governance

```text
Agent action
→ permission
→ policy
→ execution
→ verification
→ audit
```

Potentially valuable enterprise AI infrastructure.

## Platform + FinOps

```text
Infrastructure telemetry
→ cost allocation
→ forecast
→ remediation
→ savings verification
```

Combines engineering and accounting unusually well.

---

# 4. Recommended T-Shaped Strategy

Do not attempt to become world-class in every branch simultaneously.

Use:

```text
                 Broad Engineering Foundation
                            ─────────────
                                  │
                                  │
                                  │
                         Deep Specialization
```

### Suggested current combination

**Primary depth:**

> Decision Intelligence + AI Evaluation / Governance

**Strong secondary:**

> Agent Infrastructure / Software Engineering

**Research extension:**

> Frontier AI Research Engineering

**Domain moat:**

> Accounting / Finance / Risk / FinOps

This can evolve as actual performance and opportunities provide evidence.

---

# 5. 12-Month Common Foundation Before Heavy Specialization

## Quarter 1

- Linear algebra
- Probability
- Statistics
- Python depth
- SQL/PostgreSQL
- DS&A

## Quarter 2

- Regression
- Classical ML
- Forecasting
- Experimental design
- Docker/Linux
- APIs/backend

## Quarter 3

- Deep learning/PyTorch
- System design
- Cloud fundamentals
- Observability
- Research methodology

## Quarter 4

Run one serious cross-path project:

```text
FinOps / Technology Risk dataset
→ statistical model
→ prediction
→ uncertainty
→ decision policy
→ API/service
→ evals
→ audit evidence
→ reproducible research report
```

At the end of the year, choose specialization using evidence rather than prestige.

---

# 6. Specialization Decision Scorecard

Every quarter score 1–5:

| Dimension | Research | Systems | Decision | Governance | Quant | Founder |
|---|---:|---:|---:|---:|---:|---:|
| I enjoy the work | | | | | | |
| I learn unusually quickly | | | | | | |
| My projects show evidence | | | | | | |
| Interview feedback is strong | | | | | | |
| Market demand fits my constraints | | | | | | |
| I have mentors/collaborators | | | | | | |
| I can build a differentiated story | | | | | | |

Do not select a path solely because its maximum compensation or prestige is high.

---

# 7. Project-to-Path Matrix

| Existing / Planned Project | DS/Decision | Research AI | Agent/Systems | Governance | FinTech | Platform |
|---|---:|---:|---:|---:|---:|---:|
| Windows Risk Toolkit | ★★ | ★ | ★★★ | ★★★ | ★ | ★★★ |
| FinOps Platform | ★★★ | ★ | ★★ | ★★★ | ★★★ | ★★ |
| EvalForge / Agent Evals | ★★ | ★★★ | ★★★ | ★★★ | ★ | ★★ |
| AI Quant Dashboard | ★★ | ★ | ★ | ★ | ★★★ | ★ |
| Agent Orchestrator | ★ | ★★★ | ★★★ | ★★ | — | ★★★ |

Instead of creating a new repo for every career path, deepen existing projects so one artifact demonstrates multiple capabilities.

---

# 8. Role Ladder

## Near-term roles

```text
Data Analyst
Risk Data Analyst
Technology Risk Analyst
FinOps Analyst / Engineer
Python Automation Engineer
Junior Data Scientist
Junior Platform / Reliability Engineer
AI Evaluation / Governance Engineer
```

## Next layer

```text
Data Scientist
Decision Scientist
ML Engineer
AI/Agent Engineer
Platform Engineer
ML Platform Engineer
AI Governance / Evaluation Engineer
```

## Advanced

```text
Senior DS / Senior Engineer
Research Engineer
Senior ML Systems Engineer
Staff Engineer
Principal Data Scientist
AI Governance Technical Lead
```

## Extreme long-term outcomes

```text
Principal / Distinguished Engineer
Frontier AI Research Engineer / Research leadership
Organization-level technical leader
Founder
Industry-level contributor
```

Titles vary significantly between companies. Optimize for scope and evidence rather than title equivalence.

---

# 9. The Portfolio Narrative

A coherent long-term narrative could be:

```text
Accounting
↓
Financial Data
↓
Technology Risk
↓
Statistics / ML
↓
Prediction + Uncertainty
↓
Decision Intelligence
↓
Automated Action
↓
AI Agents
↓
Evaluation + Governance
↓
Auditable Enterprise AI Systems
```

This is substantially more differentiated than presenting yourself as another generic junior AI developer.

---

# 10. Current Priority

Do not choose between OpenAI Research Engineer, Google Staff+, Quant, and Founder today.

The immediate goal is to build the shared core strongly enough that these branches remain available.

```text
NOW
│
├── Quantitative roadmap
├── DS&A
├── Software engineering depth
├── 2–3 flagship projects
└── Apply to appropriate real roles
        ↓
Production + research evidence
        ↓
Observe strongest capability
        ↓
Specialize
```

## Current milestone

> **Become a strong quantitative software/data builder who can formulate a problem, build a system/model, evaluate it rigorously, explain uncertainty and trade-offs, and produce reproducible evidence.**

Once this is repeatable, selecting among Research AI, AI Systems, Decision Science, Governance, FinTech/Quant, Platform Engineering, and Founder paths becomes an evidence-based decision rather than a guess.

---

## Related Roadmaps

1. `notes/data-science-research-roadmap.md` — quantitative and Data Science foundations.
2. `notes/engineering-career-roadmap-junior-to-industry-impact.md` — engineering scope from Junior toward Staff+/industry impact.
3. `notes/frontier-ai-research-engineer-roadmap.md` — Deep Learning, LLMs, Evals, Agents, ML Systems, and Research Engineering.
4. **This document** — integrates the above into a multi-path career decision system.
