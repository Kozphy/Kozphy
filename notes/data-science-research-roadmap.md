# Data Science & Research Roadmap

**Goal:** Build from accounting + data + engineering into a quantitative, research-capable profile for Data Science, Decision Intelligence, AI Governance, FinOps, and competitive graduate-school applications.

**Learning model:** Learn with ChatGPT as tutor/TA, use university courses as syllabus/benchmark, and convert every topic into GitHub evidence.

---

## 12-Month Roadmap

### Phase 1 — Mathematical Foundations (Months 1–2)

#### Week 1–2: Algebra & Functions Review
- Functions, logs, exponentials
- Summation notation
- Basic algebra manipulation
- Python/NumPy numerical exercises

**GitHub output**
- `notebooks/math/01_algebra_functions.ipynb`
- Short note: why logarithms and exponentials matter in ML

#### Week 3–5: Linear Algebra
- Vectors and matrices
- Matrix multiplication
- Systems of linear equations
- Rank and linear independence
- Dot products and orthogonality
- Eigenvalues/eigenvectors
- SVD and PCA intuition

**Target benchmark:** MIT 18.06-level fundamentals

**GitHub output**
- Implement matrix operations with NumPy
- PCA from scratch on a small dataset
- `notes/linear-algebra-for-data-science.md`

#### Week 6–8: Calculus & Optimization
- Derivatives
- Partial derivatives
- Gradients
- Chain rule
- Convexity intuition
- Gradient descent

**GitHub output**
- Implement gradient descent for linear regression
- Plot and explain a loss surface
- `notebooks/math/gradient_descent_from_scratch.ipynb`

---

## Phase 2 — Probability & Statistics (Months 3–4)

### Week 9–10: Probability Fundamentals
- Sample spaces and events
- Conditional probability
- Independence
- Bayes' theorem
- Law of total probability

**Project connection**
Use Windows endpoint-risk examples such as:
- Proxy drift
- TLS mismatch
- Connectivity failure

**GitHub output**
- Probability exercises using synthetic endpoint-risk data
- Risk ratio calculations
- Bayes theorem examples

### Week 11–12: Random Variables & Distributions
- Discrete vs continuous variables
- Expectation
- Variance
- Bernoulli / Binomial / Normal distributions
- Law of Large Numbers
- Central Limit Theorem

**GitHub output**
- Simulations in Python
- `notebooks/statistics/distributions_and_clt.ipynb`

### Week 13–14: Statistical Inference
- Sampling distributions
- Confidence intervals
- Hypothesis testing
- p-values
- Type I / Type II errors
- Effect size

**GitHub output**
- Compare two endpoint-risk groups
- Report effect size + confidence interval, not only p-value

### Week 15–16: Regression
- Linear regression
- OLS assumptions
- Logistic regression
- Odds and log-odds
- Maximum likelihood intuition
- Multicollinearity
- Residual diagnostics

**GitHub output**
- Logistic regression for failure-risk prediction
- Coefficient interpretation
- Calibration plot

---

## Phase 3 — Machine Learning Foundations (Months 5–7)

### Week 17–18: ML Workflow
- Problem framing
- Train/validation/test split
- Data leakage
- Baselines
- Feature engineering
- Cross-validation

**GitHub output**
- Reusable experiment runner
- Baseline-first evaluation template

### Week 19–20: Supervised Learning
- Linear/logistic models
- Decision trees
- Random forests
- Gradient boosting
- XGBoost / LightGBM

**GitHub output**
- Benchmark table across models
- Reproducible seeds/configuration

### Week 21–22: Evaluation
- Accuracy
- Precision / Recall / F1
- ROC-AUC / PR-AUC
- Calibration
- Cost-sensitive evaluation

**Project connection**
Translate model error into business/risk impact.

### Week 23–24: Regularization & Generalization
- Bias-variance tradeoff
- L1 / L2 regularization
- Overfitting
- Learning curves
- Hyperparameter tuning

**GitHub output**
- Learning-curve analysis
- Regularization experiment

### Week 25–28: Unsupervised Learning & Dimensionality Reduction
- Clustering
- PCA
- Anomaly detection

**GitHub output**
- Endpoint anomaly detection experiment
- PCA visual interpretation

---

## Phase 4 — Time Series & Decision Intelligence (Months 8–9)

### Week 29–30: Time-Series Basics
- Trend
- Seasonality
- Stationarity
- Autocorrelation
- Rolling windows

### Week 31–32: Forecasting Baselines
- Naive forecast
- Seasonal naive
- Moving average
- Exponential smoothing

### Week 33–34: Statistical Forecasting
- ARIMA intuition
- ETS
- Forecast intervals

### Week 35–36: ML Forecasting
- Feature-based forecasting
- XGBoost / LightGBM
- Rolling-origin backtesting
- Leakage-safe evaluation

**Primary project:** Cloud FinOps Decision Intelligence Platform

**GitHub output**
- Naive vs ETS/ARIMA vs ML benchmark
- MAE / RMSE / MAPE
- Prediction intervals
- Rolling-window backtest
- Error analysis by month/service/category

---

## Phase 5 — Research Methods (Months 10–11)

### Week 37–38: Research Question Design
- What makes a good research question?
- Hypotheses
- Independent/dependent variables
- Confounders
- Correlation vs causation

### Week 39–40: Experimental Design
- Baselines
- Controls
- Ablation studies
- Robustness tests
- Distribution shift

### Week 41–42: Reproducibility
- Environment locking
- Dataset versioning
- Seeds
- Config files
- Experiment tracking
- CI tests

### Week 43–44: Scientific Writing
- Abstract
- Introduction
- Related work
- Methods
- Results
- Discussion
- Threats to validity
- Conclusion

**GitHub output**
- `paper/` directory
- 10–15 page paper-style manuscript
- Reproducible experiment commands

---

## Phase 6 — Flagship Research Project (Month 12)

Choose ONE flagship project and finish it deeply.

### Option A — Endpoint Technology Risk
Research example:
> Can proxy/configuration drift predict connectivity incidents, and how stable is the relationship across environments?

### Option B — Cloud FinOps Decision Intelligence
Research example:
> Which forecasting approach produces the most reliable cloud-cost forecasts under changing workload conditions?

### Option C — AI / Agent Governance
Research example:
> Which evaluation and policy-gating strategy best reduces unsafe or low-quality agent actions while preserving task success?

### Required final outputs
- Research question
- Dataset/data-generation methodology
- EDA
- Statistical analysis
- Baseline models
- Advanced models
- Confidence/prediction intervals
- Ablation study
- Error analysis
- Failure taxonomy
- Threats to validity
- Reproducible runner
- CI/tests
- Paper-style manuscript

---

# Weekly Study Rhythm

Recommended workload: **8–12 focused hours/week**.

## Monday — Concept
- Learn one core concept with ChatGPT
- Explain it in your own words
- 5–10 short exercises

## Tuesday — Mathematics
- Derive formulas by hand
- Solve quantitative problems without Python first

## Wednesday — Python Implementation
- Implement the concept from scratch when practical
- Compare against NumPy / scikit-learn

## Thursday — Applied Project
- Apply the concept to FinOps, Windows Risk, or AI Governance data

## Friday — Evaluation
- Write tests
- Check assumptions
- Analyze failure cases

## Weekend — Research Note
- Write a short Markdown note
- Commit notebook/code/results
- Answer: "What did I learn, and what evidence did I produce?"

---

# Course Benchmarks

These are benchmarks, not mandatory video-watching requirements.

- **Linear Algebra:** MIT 18.06
- **Probability:** Harvard Stat 110 / equivalent university probability
- **Statistics:** university-level inference + regression
- **Machine Learning:** Stanford CS229-level foundations
- **Research:** reproduce at least one paper-style experiment

Use ChatGPT as the primary interactive tutor:
1. Explain concept
2. Give exercises
3. Grade answers
4. Identify weak points
5. Increase difficulty
6. Connect lesson to repository code

---

# Graduation Criteria

Do not mark the roadmap complete just because videos or chapters were finished.

You should be able to:

- Explain conditional probability and Bayes theorem
- Derive and interpret linear/logistic regression
- Explain loss functions and regularization
- Detect data leakage
- Design a valid baseline
- Use cross-validation correctly
- Interpret confidence intervals
- Evaluate classification and forecasting models
- Explain calibration and uncertainty
- Run reproducible experiments
- Perform an ablation study
- Analyze model failures
- Write a research-style technical report
- Defend architecture and modeling choices in an interview

---

# Target Profile

Starting point:

**Accounting + Python + SQL + Data Analytics + Engineering Projects**

Target:

**Accounting / Finance Domain + Statistics + ML + Software Engineering + Research + Decision Intelligence**

This roadmap is designed to turn existing engineering projects into stronger quantitative and research evidence rather than creating many disconnected repositories.
