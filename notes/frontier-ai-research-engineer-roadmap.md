# Frontier AI Research Engineer Roadmap

**Created:** 2026-09-06  
**Goal:** Build from quantitative/data/software foundations toward frontier AI Research Engineering capability.  
**Target environments:** frontier AI labs and research-heavy ML/agent teams.  

> This roadmap is a capability roadmap, not a guarantee of employment at OpenAI or any other lab.

---

## Starting Point

Existing direction:

```text
Accounting / Finance
→ Python / SQL / Data
→ Technology Risk / FinOps
→ Software Engineering
→ Statistics / ML
→ Decision Intelligence
```

Frontier AI extension:

```text
Quantitative Foundation
→ Deep Learning
→ Transformers / LLMs
→ Evals
→ Post-training / RL
→ Agent Systems
→ Distributed ML Systems
→ Research Engineering
→ Frontier-scale Research
```

---

# Phase 0 — Prerequisites

Complete the quantitative/data-science roadmap first or study these in parallel.

## Mathematics
- [ ] Linear algebra
- [ ] Multivariable calculus basics
- [ ] Probability
- [ ] Statistics
- [ ] Optimization
- [ ] Information theory basics

## Computer Science
- [ ] Python deeply
- [ ] Data structures and algorithms
- [ ] Linux
- [ ] Networking basics
- [ ] Processes / threads / concurrency
- [ ] Databases
- [ ] Git
- [ ] Testing / CI
- [ ] Docker

## ML
- [ ] Regression/classification
- [ ] Loss functions
- [ ] Gradient descent
- [ ] Regularization
- [ ] Generalization
- [ ] Calibration
- [ ] Experimental design

### Exit test
Explain and implement a small ML experiment without relying on generated code, including baseline, train/validation/test design, metrics, uncertainty, and error analysis.

---

# Phase 1 — Deep Learning Foundations

## Theory
- [ ] Neural networks
- [ ] Backpropagation
- [ ] Automatic differentiation
- [ ] SGD / Adam
- [ ] Initialization
- [ ] Normalization
- [ ] Regularization
- [ ] Representation learning

## Engineering
- [ ] PyTorch tensors
- [ ] autograd
- [ ] nn.Module
- [ ] Dataset / DataLoader
- [ ] training loops
- [ ] checkpoints
- [ ] mixed precision basics
- [ ] experiment tracking

## Build
Implement from progressively lower abstraction levels:

```text
Linear regression
→ MLP
→ classifier
→ training/evaluation pipeline
```

### Exit criteria
- [ ] Derive backprop for a small network
- [ ] Implement training loop manually
- [ ] Diagnose overfitting/underfitting
- [ ] Reproduce experiments from fixed seeds/configs

---

# Phase 2 — Attention & Transformers

## Learn
- [ ] Embeddings
- [ ] Positional representations
- [ ] Query / Key / Value
- [ ] Scaled dot-product attention
- [ ] Multi-head attention
- [ ] Residual connections
- [ ] Layer normalization
- [ ] Feed-forward networks
- [ ] Causal masking
- [ ] Encoder vs decoder architectures

Core equation:

```text
Attention(Q,K,V) = softmax(QK^T / sqrt(d_k))V
```

Do not merely memorize it. Explain why scaling exists, what masking changes, and the computational/memory cost.

## Build

```text
Tokenizer
→ embeddings
→ self-attention
→ transformer block
→ tiny decoder-only language model
```

Train a small model on a manageable dataset.

### Exit criteria
- [ ] Implement attention
- [ ] Explain transformer forward pass
- [ ] Understand tensor shapes throughout the model
- [ ] Profile memory/runtime at small scale

---

# Phase 3 — LLM Engineering

## Learn
- [ ] Tokenization: BPE-like concepts
- [ ] Language-model objectives
- [ ] Pretraining data pipeline concepts
- [ ] Context windows
- [ ] Sampling: temperature/top-k/top-p
- [ ] KV cache
- [ ] Batching
- [ ] Quantization concepts
- [ ] LoRA / parameter-efficient fine-tuning
- [ ] Model serving fundamentals

## Build

Create a small LLM engineering lab:

```text
model/
data/
training/
inference/
evals/
experiments/
```

Compare at least two controlled changes and report results rather than claiming improvements from a single run.

---

# Phase 4 — Evaluation Science

This is a particularly strong bridge from existing risk/governance work.

Transform the existing mindset:

```text
Evidence → Control → Decision → Audit Trail
```

into:

```text
Task
→ Environment
→ Model/Agent
→ Grader
→ Metrics
→ Failure Taxonomy
→ Regression Detection
→ Experiment
→ Improvement
```

## Learn
- [ ] Benchmark design
- [ ] Dataset contamination concerns
- [ ] Train/test leakage
- [ ] Human evaluation
- [ ] Model-based graders and limitations
- [ ] Pairwise evaluation
- [ ] Calibration
- [ ] Statistical uncertainty
- [ ] Confidence intervals
- [ ] Bootstrap concepts
- [ ] Failure taxonomy
- [ ] Adversarial evaluation
- [ ] Capability vs safety evaluation concepts

## Flagship project

### AgentEval / EvalForge-style platform

```text
Tasks
→ sandbox execution
→ traces
→ deterministic graders where possible
→ model graders where appropriate
→ statistical analysis
→ failure classification
→ regression dashboard
→ CI gate
```

### Exit criteria
- [ ] Design a benchmark
- [ ] Justify every metric
- [ ] Quantify uncertainty
- [ ] Identify grader failure modes
- [ ] Detect regressions across model/agent versions

---

# Phase 5 — Post-Training

## Learn
- [ ] Supervised fine-tuning
- [ ] Instruction tuning
- [ ] Preference data
- [ ] Reward modeling concepts
- [ ] RL fundamentals
- [ ] Policy/value concepts
- [ ] PPO concepts
- [ ] DPO and preference optimization concepts
- [ ] RLHF / RLAIF concepts
- [ ] Synthetic data
- [ ] Distillation concepts

The objective is not to memorize acronyms. Understand:

```text
Data
→ objective
→ optimization
→ behavior change
→ evaluation
```

## Experiments
Run small-scale controlled post-training experiments on open models where practical.

Measure:
- task performance
- regressions
- behavioral changes
- cost
- variance

---

# Phase 6 — Agent Systems

Move beyond using agents toward studying their behavior.

## Foundations
- [ ] Tool calling
- [ ] Structured outputs
- [ ] State machines
- [ ] Planning
- [ ] Memory
- [ ] Retrieval
- [ ] Sandboxed execution
- [ ] Computer/code execution concepts
- [ ] Failure recovery
- [ ] Long-horizon tasks

## Multi-agent topics
- [ ] Task decomposition
- [ ] Delegation
- [ ] Shared vs isolated context
- [ ] Coordination cost
- [ ] Agent specialization
- [ ] Verification
- [ ] Conflict resolution

## Build: Coding Agent Research Environment

```text
Task dataset
→ repository sandbox
→ agent
→ tool calls
→ code changes
→ tests
→ grader
→ trace collection
→ failure taxonomy
→ experiment analysis
```

Then compare:

```text
single-agent baseline
vs
planner/executor
vs
multi-agent orchestration
```

Do not assume multi-agent is better. Test it.

### Metrics
- success rate
- tests passed
- latency
- token/compute cost
- retries
- regression rate
- human intervention

---

# Phase 7 — ML Systems

Frontier research engineering requires systems knowledge.

## Systems
- [ ] Linux performance tools
- [ ] CPU/GPU memory hierarchy concepts
- [ ] GPU architecture fundamentals
- [ ] CUDA concepts
- [ ] Profiling
- [ ] Efficient data loading
- [ ] Mixed precision
- [ ] Checkpointing
- [ ] Fault tolerance

## Distributed ML
- [ ] Data parallelism
- [ ] Model/tensor parallelism concepts
- [ ] Pipeline parallelism concepts
- [ ] Collective communication concepts
- [ ] Distributed training failure modes
- [ ] Distributed checkpointing
- [ ] Cluster scheduling concepts

## Inference
- [ ] Continuous/dynamic batching concepts
- [ ] KV-cache management
- [ ] Throughput vs latency
- [ ] Quantization trade-offs
- [ ] Model serving
- [ ] Observability
- [ ] Cost/performance measurement

### Exit criteria
- [ ] Profile a training/inference workload
- [ ] Identify bottlenecks using evidence
- [ ] Explain distributed training architecture
- [ ] Reason about reliability and cost trade-offs

---

# Phase 8 — Research Engineering

This is the critical transition.

## Research loop

```text
Read paper
→ identify claim
→ reproduce baseline
→ verify result
→ formulate hypothesis
→ modify system/model
→ controlled experiment
→ statistical analysis
→ failure analysis
→ conclusion
→ next hypothesis
```

## Weekly practice

Each week:
1. Read one serious paper deeply.
2. Write the central research question.
3. Identify assumptions.
4. Identify experimental design.
5. Identify weaknesses.
6. Reproduce one meaningful component when feasible.

## Repository structure

```text
research-project/
├── README.md
├── paper-notes/
├── src/
├── experiments/
├── configs/
├── evals/
├── tests/
├── results/
├── analysis/
└── manuscript/
```

### Exit criteria
- [ ] Reproduce meaningful published results
- [ ] Design controlled experiments
- [ ] Defend methodological choices
- [ ] Analyze negative results
- [ ] Produce reproducible research artifacts

---

# Phase 9 — Frontier Research Portfolio

Build 2–3 deep artifacts, not dozens of demos.

## Project A — Coding Agent Evaluation Environment

Research question example:

> Under what conditions does multi-agent orchestration improve coding-task success relative to a strong single-agent baseline after accounting for compute cost?

Evidence:
- benchmark
- baselines
- controlled experiment
- statistical analysis
- failure taxonomy
- reproducible runner

## Project B — Long-Horizon Agent Reliability

Study:
- error accumulation
- recovery
- verification
- context management
- cost/quality trade-offs

## Project C — AI Decision & Governance Infrastructure

Combine existing domain strengths:

```text
Agent/model output
→ uncertainty/evaluation
→ policy
→ risk threshold
→ human review
→ execution
→ verification
→ immutable evidence
```

This can become a differentiated research identity rather than another generic chatbot project.

---

# Phase 10 — External Research Evidence

GitHub alone is insufficient for the strongest research profiles.

Build external evidence:

- [ ] Technical blog / research notes
- [ ] Reproduction reports
- [ ] Open-source contributions
- [ ] Collaborate with researchers/professors
- [ ] RA/research collaboration where possible
- [ ] Preprint when work justifies it
- [ ] Workshop/conference submission when appropriate
- [ ] Strong technical/research references

Focus on quality and intellectual honesty, not publication count.

---

# Interview Preparation Track

## Coding
- [ ] Data structures
- [ ] Algorithms
- [ ] Python fluency
- [ ] Debugging

## ML
- [ ] Probability/statistics
- [ ] Deep learning
- [ ] Transformers
- [ ] Optimization
- [ ] Evaluation

## Systems
- [ ] Distributed systems
- [ ] ML infrastructure
- [ ] Performance
- [ ] Reliability

## Research
Practice answering:

- Why this hypothesis?
- Why this baseline?
- Why this metric?
- What evidence would falsify your claim?
- What failed?
- What would you try next?
- How do you know the improvement is real?

---

# Suggested 24–36 Month Sequence

This is directional and may be accelerated or slowed based on mastery.

## Months 0–6

```text
Quantitative foundations
+ classical ML
+ DS&A
+ PyTorch
```

## Months 6–12

```text
Deep Learning
→ Transformers
→ tiny language model
→ LLM engineering
```

## Months 12–18

```text
Evals
→ agent environments
→ controlled experiments
→ paper reproduction
```

## Months 18–24

```text
Post-training / RL foundations
→ advanced agents
→ ML systems
→ distributed training concepts
```

## Months 24–36

```text
Research collaborations
→ original experiments
→ open-source/research output
→ frontier AI Research Engineer applications
```

Do not wait until month 36 to apply for jobs. Apply throughout the process to appropriate Data/ML/SWE/Research Engineering roles and use interview feedback as evidence about gaps.

---

# Capability Ladder

```text
AI Tool User
↓
ML Practitioner
↓
ML Engineer
↓
LLM Engineer
↓
Evaluation / Agent Engineer
↓
Research Engineer
↓
Frontier Research Engineer
```

The transitions depend on evidence, not labels.

---

# Anti-Patterns

Do not optimize for:

- 50 shallow AI repositories
- wrapper-only chatbot projects
- agent count
- certificate count
- copying paper code without understanding it
- benchmark scores without methodology
- claiming causality from correlation
- using LLM-generated analysis that you cannot defend

Optimize for:

> **Fundamentals × Experiments × Systems × Reproducibility × Research Judgment**

---

# Current Immediate Milestone

Before trying to simulate frontier-scale research, become able to do this independently:

> **Take one ML/agent paper, understand the hypothesis, reproduce a meaningful result, build an evaluation harness, identify failure modes, make one justified modification, run a controlled experiment, and explain whether the evidence supports the change.**

Once this becomes repeatable, the transition from AI application builder toward Research Engineer is real.
