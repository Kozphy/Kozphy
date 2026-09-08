# Quant Math & Research Roadmap

**Goal:** Build the mathematical, statistical, and research capability required for serious quantitative trading research, while connecting the work to Python, reproducible experiments, AI/agent tooling, and production-quality GitHub evidence.

**Target profile:**

> Accounting / Finance Domain + Python + Statistics + Time Series + Econometrics + Optimization + Research Engineering + Quant Research

This roadmap is not about memorizing formulas or generating trading strategies with an LLM. The objective is to become capable of forming hypotheses, designing valid experiments, detecting bias, measuring uncertainty, and defending research conclusions under technical review.

---

## 1. Learning Principle: Math -> Code -> Research

For every topic, use the same loop:

1. Learn the concept.
2. Derive the main result by hand when practical.
3. Solve exercises without Python first.
4. Verify the result with NumPy / SciPy / statsmodels.
5. Apply it to market or financial data.
6. State assumptions explicitly.
7. Run robustness checks.
8. Write a short research note.
9. Commit code, data metadata, configuration, and results.
10. Explain what would invalidate the conclusion.

The goal is not "I finished a course." The goal is:

> I can use the concept correctly in a reproducible research decision.

---

# 12-Month Quant Research Roadmap

## Phase 1 — Mathematical Foundations (Months 1–2)

### 1.1 Algebra, Functions, Logs, and Summation

Topics:
- Functions and inverse functions
- Exponentials and logarithms
- Ratios and percentage change
- Compounding
- Summation notation
- Geometric series
- Basic inequalities

Quant applications:
- Simple vs log returns
- Compound growth
- Drawdown calculations
- Discounting
- Moving-window statistics

**GitHub evidence**
- `notebooks/math/01_returns_and_compounding.ipynb`
- Implement simple return and log return from scratch
- Explain when log returns can and cannot be added

---

### 1.2 Linear Algebra

Topics:
- Vectors and matrices
- Dot products
- Matrix multiplication
- Rank and linear independence
- Systems of linear equations
- Orthogonality
- Eigenvalues/eigenvectors
- Covariance matrices
- Positive semidefinite matrices
- SVD and PCA intuition

Quant applications:
- Portfolio weights
- Factor exposures
- Covariance matrices
- PCA for risk-factor compression
- Linear regression in matrix form

**Target benchmark:** MIT 18.06-level fundamentals.

**GitHub evidence**
- Build covariance matrix manually and compare with NumPy
- PCA from scratch on asset returns
- `notes/linear-algebra-for-quant.md`

---

### 1.3 Calculus

Topics:
- Limits intuition
- Derivatives
- Partial derivatives
- Chain rule
- Gradients
- Hessian intuition
- Integrals
- Taylor approximation

Quant applications:
- Optimization
- Sensitivity analysis
- Maximum likelihood
- Risk sensitivities
- Gradient-based model fitting

**GitHub evidence**
- Derive gradient for linear regression
- Implement gradient descent
- Compare analytical gradient with numerical finite differences

---

## Phase 2 — Probability & Statistical Inference (Months 3–4)

### 2.1 Probability

Topics:
- Sample spaces and events
- Conditional probability
- Independence
- Bayes' theorem
- Law of total probability
- Combinatorics basics

Quant applications:
- Conditional market events
- Regime probabilities
- Risk-event reasoning
- Bayesian updating

**Research question example**

> Does the probability of a positive next-day return change after an extreme volatility event?

---

### 2.2 Random Variables and Distributions

Topics:
- Discrete vs continuous random variables
- Expectation
- Variance
- Covariance
- Correlation
- Bernoulli / Binomial / Normal
- Student-t distribution
- Chi-square intuition
- Heavy tails
- Law of Large Numbers
- Central Limit Theorem

Quant applications:
- Return distributions
- Tail risk
- Volatility
- Monte Carlo simulation
- Confidence intervals

**GitHub evidence**
- Simulate normal vs heavy-tailed returns
- Compare empirical and theoretical quantiles
- Demonstrate why normality assumptions can underestimate tail risk

---

### 2.3 Statistical Inference

Topics:
- Sampling distributions
- Point estimates
- Confidence intervals
- Hypothesis testing
- p-values
- Type I / Type II errors
- Statistical power
- Effect size
- Bootstrap
- Permutation tests

Key research distinction:

> Statistical significance is not the same as economic significance.

A signal can have a tiny p-value and still be untradeable after costs.

**GitHub evidence**
- Bootstrap confidence interval for Sharpe ratio
- Compare two strategies with uncertainty estimates
- Report effect size + CI, not only p-value

---

### 2.4 Multiple Testing

Topics:
- Multiple comparisons problem
- Family-wise error rate
- False discovery rate
- Bonferroni intuition
- Data snooping
- Selection bias

Critical Quant question:

> If 500 strategies are tested and the best one is reported, how much of the performance may be luck?

**GitHub evidence**
- Simulate hundreds of random strategies
- Show that some appear significant by chance
- Apply a simple multiple-testing correction

---

# Phase 3 — Regression, Econometrics, and Causal Thinking (Months 5–6)

## 3.1 Linear Regression

Topics:
- OLS
- Matrix formulation
- Residuals
- R-squared
- Confidence intervals
- Heteroskedasticity
- Multicollinearity
- Robust standard errors

Quant applications:
- Factor models
- Signal-return relationships
- Exposure estimation
- Return attribution

**GitHub evidence**
- CAPM-style regression
- Multi-factor regression
- Residual diagnostics
- Robust standard errors

---

## 3.2 Logistic Regression and Classification

Topics:
- Odds and log-odds
- Maximum likelihood
- Calibration
- Classification thresholds
- Precision / Recall / ROC / PR curves

Quant application:
- Probability of positive return
- Event classification
- Default/risk modeling

Warning:

Classification accuracy alone is usually not a trading objective. Translate predictions into expected return, risk, turnover, and cost.

---

## 3.3 Econometrics

Topics:
- Omitted-variable bias
- Endogeneity intuition
- Autocorrelation
- Heteroskedasticity
- Stationarity
- Unit roots
- Cointegration
- Granger-causality interpretation and limitations
- Panel-data intuition

Research mindset:

> Correlation can generate a signal hypothesis, but it does not automatically establish a stable economic relationship.

**GitHub evidence**
- Stationarity tests on market series
- Spurious regression demonstration
- Cointegration experiment on asset pairs

---

# Phase 4 — Time Series for Quant Research (Months 7–8)

## 4.1 Time-Series Foundations

Topics:
- Trend
- Seasonality
- Stationarity
- ACF / PACF
- Lag features
- Rolling statistics
- Expanding windows
- Structural breaks
- Regime changes

**GitHub evidence**
- ACF/PACF notebook
- Rolling volatility analysis
- Regime-change visualization

---

## 4.2 Forecasting Baselines

Always start with baselines:
- Naive forecast
- Historical mean
- Random walk
- Moving average
- Exponential smoothing

Then compare:
- AR / ARIMA
- GARCH intuition
- Feature-based ML
- Gradient boosting
- Neural approaches only when justified

Key principle:

> A complex model that cannot beat a leakage-safe baseline is not an improvement.

---

## 4.3 Time-Series Validation

Do not use ordinary random train/test splitting for market time series.

Learn:
- Expanding-window evaluation
- Rolling-window evaluation
- Walk-forward testing
- Purging / embargo concepts
- Nested model selection intuition
- Regime-aware validation

**GitHub evidence**
- Reusable `walk_forward.py`
- Leakage-safe experiment runner
- Comparison of random split vs temporal split

---

# Phase 5 — Optimization, Portfolio Theory, and Risk (Month 9)

## 5.1 Optimization

Topics:
- Objective functions
- Constraints
- Convexity intuition
- Lagrange multipliers
- Numerical optimization
- Regularization

Applications:
- Portfolio allocation
- Position sizing
- Risk budgets
- Transaction-cost-aware optimization

---

## 5.2 Portfolio Mathematics

Topics:
- Expected return
- Variance / volatility
- Covariance
- Portfolio variance
- Diversification
- Sharpe ratio
- Maximum drawdown
- Beta
- Tracking error
- Value-at-Risk intuition
- Expected Shortfall intuition

Do not treat Sharpe ratio as sufficient evidence by itself.

Report at minimum:
- Return
- Volatility
- Sharpe
- Maximum drawdown
- Turnover
- Transaction costs
- Exposure concentration
- Out-of-sample stability

---

## 5.3 Monte Carlo

Topics:
- Random sampling
- Monte Carlo estimation
- Bootstrap simulation
- Scenario generation
- Parameter uncertainty

**GitHub evidence**
- Monte Carlo portfolio simulation
- Bootstrap Sharpe uncertainty
- Scenario-based drawdown analysis

---

# Phase 6 — Quant Research Methodology (Months 10–11)

## 6.1 Research Question

Every experiment starts with a precise research question.

Weak:

> Can I make money using momentum?

Better:

> Does a 12-1 month cross-sectional momentum signal produce positive out-of-sample risk-adjusted returns after realistic transaction costs across multiple market regimes?

A strong question defines:
- Population / market
- Time horizon
- Signal
- Outcome
- Comparison baseline
- Evaluation period
- Cost assumptions
- Falsification criteria

---

## 6.2 Hypotheses

Example:

**H0:** Momentum signal returns are not different from the selected benchmark after costs.

**H1:** Momentum signal returns exceed the benchmark after costs.

Before running the experiment, define:
- Primary metric
- Secondary metrics
- Significance threshold if used
- Evaluation window
- Stop / reject conditions

This reduces retrospective storytelling.

---

## 6.3 Baselines

Possible baselines:
- Buy and hold
- Equal weight
- Random signal
- Historical mean
- Simple moving-average rule
- Published conventional factor

Never compare an advanced model only against a deliberately weak baseline.

---

## 6.4 Bias and Failure Checklist

Every research report must explicitly check:

- Look-ahead bias
- Data leakage
- Survivorship bias
- Selection bias
- Data-snooping bias
- Multiple testing
- Overfitting
- Incorrect timestamp alignment
- Corporate-action handling
- Delisting bias
- Unrealistic execution price
- Ignored transaction costs
- Ignored slippage
- Ignored market impact
- Small sample size
- Structural breaks
- Regime dependence

---

## 6.5 Robustness Tests

A strategy should survive reasonable perturbations.

Test:
- Different time periods
- Different markets/assets
- Different rebalance frequencies
- Different transaction costs
- Different parameter ranges
- Different train/test windows
- Different seeds for stochastic models
- Removal of extreme observations

If the strategy works only at one exact parameter, treat it as fragile evidence.

---

## 6.6 Ablation Studies

For multi-component models, remove components one at a time.

Example:

```text
Full model
├── momentum
├── volatility filter
├── liquidity filter
└── regime filter
```

Ask:
- What happens without momentum?
- What happens without the volatility filter?
- Which component actually contributes to performance?

---

## 6.7 Failure Analysis

Do not hide failed experiments.

Classify failure:
- No predictive signal
- Signal disappears OOS
- High turnover destroys edge
- Performance concentrated in one period
- Tail losses dominate
- Parameter instability
- Data quality issue
- Execution assumption failure

Negative results are useful when documented rigorously.

---

# Phase 7 — Flagship Quant Research Project (Month 12)

## Recommended project: Momentum Research Benchmark

### Research Question

> Does a simple momentum signal retain out-of-sample predictive and economic value after realistic costs and robustness testing?

### Pipeline

```text
Market Data
    ↓
Data Validation
    ↓
Research Question
    ↓
Signal Definition
    ↓
Baseline
    ↓
In-Sample Experiment
    ↓
Walk-Forward / OOS
    ↓
Transaction Costs
    ↓
Statistical Inference
    ↓
Multiple-Testing Control
    ↓
Robustness Tests
    ↓
Ablation / Failure Analysis
    ↓
Risk Analysis
    ↓
Paper Trading Candidate
    ↓
Research Report
```

### Required outputs

- Dataset description and timestamp policy
- Research question
- H0 / H1
- Baseline
- Signal formula
- Backtest specification
- Walk-forward evaluation
- Transaction-cost assumptions
- Confidence intervals
- Statistical tests
- Multiple-testing discussion
- Return / volatility / Sharpe / drawdown / turnover
- Robustness matrix
- Ablation study
- Failure taxonomy
- Threats to validity
- Reproducible environment
- Automated tests
- Paper-style manuscript

---

# Recommended Repository Structure

```text
quant-research/
├── README.md
├── pyproject.toml
├── configs/
│   ├── baseline.yaml
│   └── momentum.yaml
├── data/
│   └── README.md
├── src/
│   ├── data.py
│   ├── features.py
│   ├── signals.py
│   ├── portfolio.py
│   ├── backtest.py
│   ├── costs.py
│   ├── metrics.py
│   └── validation.py
├── notebooks/
│   ├── 01_eda.ipynb
│   ├── 02_signal.ipynb
│   └── 03_robustness.ipynb
├── experiments/
│   └── run_experiment.py
├── tests/
│   ├── test_no_lookahead.py
│   ├── test_signal_alignment.py
│   └── test_costs.py
├── results/
│   ├── benchmark.csv
│   └── robustness.csv
└── paper/
    └── manuscript.md
```

---

# Weekly Study Rhythm

Recommended workload: **8–12 focused hours/week**.

## Monday — Concept
- Learn one mathematical/statistical concept
- Explain it without notes
- Solve short exercises

## Tuesday — Derivation
- Derive formulas by hand
- Identify assumptions
- Solve quantitative problems without Python first

## Wednesday — Code
- Implement the method from scratch where practical
- Compare with NumPy / SciPy / statsmodels

## Thursday — Quant Application
- Apply it to market data
- Define a research hypothesis

## Friday — Validation
- Check leakage
- Check assumptions
- Run robustness tests
- Analyze failure cases

## Weekend — Research Note
Write a Markdown note containing:
- Question
- Method
- Result
- Uncertainty
- Failure cases
- What would falsify the conclusion

Commit the notebook, tests, configuration, and results.

---

# ChatGPT as Quant Research Tutor

Use ChatGPT as an interactive tutor and reviewer, not as an oracle.

For each topic, the workflow should be:

```text
Explain
  ↓
Quiz me
  ↓
I solve it
  ↓
Grade my reasoning
  ↓
Make me derive it
  ↓
Verify with Python
  ↓
Apply to market data
  ↓
Attack the experiment
  ↓
Find bias / leakage
  ↓
Defend the conclusion
```

Useful prompts:

> Teach me conditional probability at a Quant Research interview level. Do not give the answer immediately. Give me one problem at a time and grade my reasoning.

> Review this backtest as a skeptical Quant Researcher. Look specifically for look-ahead bias, leakage, survivorship bias, overfitting, multiple testing, and unrealistic execution assumptions.

> Act as my research committee. Ask me to defend my baseline, hypothesis, statistical test, robustness design, and threats to validity.

> Give me a mathematical derivation first, then make me implement it in Python without using the high-level library function.

---

# Research Oral-Exam Checklist

You should eventually be able to answer questions such as:

1. Why is this the correct baseline?
2. What is your null hypothesis?
3. Why is this test statistically valid?
4. Are observations independent?
5. How did you handle autocorrelation?
6. How did you prevent look-ahead bias?
7. Was the strategy selected after trying many alternatives?
8. How did you handle multiple testing?
9. Is performance statistically significant?
10. Is performance economically significant after costs?
11. Is performance concentrated in a single regime?
12. What happens when parameters change?
13. What is the confidence interval around Sharpe?
14. What assumptions are unrealistic?
15. What result would cause you to reject the strategy?
16. Could another researcher reproduce the result?

If these questions cannot be answered, the project is not research-grade yet.

---

# AI / Agent Integration

AI agents can accelerate Quant Research, but they should not bypass scientific controls.

A useful architecture is:

```text
Research Question
      ↓
Research Agent
      ↓
Experiment Proposal
      ↓
Policy / Methodology Gate
      ↓
Sandbox Backtest
      ↓
Statistical Validation
      ↓
Bias Detector
      ↓
Robustness Tests
      ↓
Human Review
      ↓
Paper Trading
      ↓
Monitoring
```

Agents can help with:
- Literature triage
- Experiment scaffolding
- Code generation
- Backtest orchestration
- Parameter sweeps
- Report generation
- Failure analysis

Agents must not be allowed to turn a weak experiment into a positive conclusion by repeatedly searching until something looks profitable.

The research system should log:
- Hypotheses tested
- Parameter combinations
- Dataset versions
- Model versions
- Failed experiments
- Evaluation metrics
- Human approvals

This turns agentic Quant Research into an auditable research workflow rather than automated data snooping.

---

# Graduation Criteria

Do not mark this roadmap complete because courses were watched or notebooks were copied.

You should be able to:

- Work comfortably with vectors, matrices, derivatives, and probability
- Explain expectation, variance, covariance, and correlation mathematically
- Construct confidence intervals and hypothesis tests
- Explain statistical power and multiple testing
- Fit and diagnose regression models
- Explain stationarity and spurious regression
- Build leakage-safe time-series validation
- Implement a reproducible backtest
- Model transaction costs
- Quantify uncertainty in performance metrics
- Perform robustness and ablation analysis
- Detect look-ahead and survivorship bias
- Explain why a profitable backtest may still be invalid
- Document negative results
- Write a paper-style Quant Research report
- Defend the work under skeptical technical questioning

---

# Final Target

Starting point:

**Accounting + Finance + Python + Data / Engineering**

Intermediate:

**Probability + Statistics + Linear Algebra + Time Series + Econometrics + Backtesting**

Advanced:

**Optimization + Research Methodology + Risk + Reproducibility + Production Research Infrastructure**

Long-term:

> **Quant Research + AI Agent + Production Systems**

The strongest outcome is not a bot that claims to predict markets. It is a research system where every claim can be traced to data, assumptions, experiments, uncertainty, validation, and reproducible evidence.
