# Zixsa (Kozphy)

**Risk Advisory / Tech Risk · Financial Analysis · Python · Taiwan**

I build checkable financial analysis and technology-risk evidence: cases you can re-perform, control workpapers, and Python workflows with explicit exceptions.

Focus: associate-level Technology Risk / Risk Advisory and Financial Analysis support — remote and international scopes welcome. Portfolio brand is Zixsa; legal identity stays with HR when required.

## Start here: one case in three minutes

### From financial statements to a checkable analysis

**The problem:** A financial analysis is difficult to review when its inputs, assumptions, calculations, and conclusions are disconnected.

**The case:** [Apple FY2025 financial-analysis workflow](https://github.com/Kozphy/financial-analysis-tool). An educational portfolio case using a public-company snapshot, explicit assumptions, Python calculations, and an analysis memo.

```text
Financial inputs → cash-flow and net-debt calculations
                 → valuation sensitivity → analysis memo
                 → tests for the headline numbers
```

| Step | What you can inspect |
| --- | --- |
| **1. Check the inputs** | [Case data](https://github.com/Kozphy/financial-analysis-tool/blob/main/data/apple_fy2025_case.csv) and [source references and assumptions](https://github.com/Kozphy/financial-analysis-tool/blob/main/case_studies/apple_fy2025.md) |
| **2. Read the result** | [Analysis memo](https://github.com/Kozphy/financial-analysis-tool/blob/main/case_studies/apple_fy2025.md), including sensitivity analysis and open diligence questions |
| **3. Verify the calculations** | [Calculation code](https://github.com/Kozphy/financial-analysis-tool/blob/main/src/financial_analysis_tool/case_study.py) and [case tests](https://github.com/Kozphy/financial-analysis-tool/blob/main/tests/test_case_study.py) |

**Two numbers you can trace** — USD millions:

- Operating cash flow **111,482** − capital expenditure **12,715** = **98,767** simplified free-cash-flow proxy.
- Debt **98,657** − cash and securities **132,420** = **−33,763** net debt, meaning net cash under this simplified definition.

The memo separates reported inputs from model assumptions. Tests check the cash bridges, valuation scenarios, and sensitivity table.

### Reproduce the case calculations

With Git and the [project’s Python requirements](https://github.com/Kozphy/financial-analysis-tool/blob/main/pyproject.toml), use a virtual environment and run:

```bash
git clone https://github.com/Kozphy/financial-analysis-tool.git
cd financial-analysis-tool
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux: source .venv/bin/activate
pip install -e ".[dev]"
pytest -q
```

[Full reproduction walkthrough and expected outputs](https://github.com/Kozphy/financial-analysis-tool/blob/main/README.md)

**Scope:** A single-year educational case with illustrative valuation assumptions. The cash-flow proxy is not a full unlevered cash-flow model. The memo’s “Watch” stance is human-written; the tests verify arithmetic and table integrity, not investment advice.

Live walkthrough: [kozphy.github.io/case.html](https://kozphy.github.io/case.html) · Workpaper: [WP-FIN-001](https://kozphy.github.io/workpaper.html) · Résumé: [resume](https://kozphy.github.io/resume.html)

## Supporting work: finance-focused AI evaluation

[EvalForge](https://github.com/Kozphy/EvalForge) explores how to detect incorrect financial AI outputs using deterministic checks, error categories, regression comparisons, and policy gates.

[Read the evaluation report](https://github.com/Kozphy/EvalForge) · [Inspect the evidence limits](https://kozphy.github.io/)

The published benchmark uses self-authored synthetic data and offline candidate responses with planted errors. Its results demonstrate the evaluation workflow; they do not establish live-model performance.

## Where this work fits

- Technology Risk / Risk Advisory associate scopes (controls, testing, exceptions)
- Financial analysis, CSV reconciliation, and repeatable reporting
- Finance-focused AI evaluation and QA with explicit non-claims

For a project discussion, a useful starting brief is: **sample inputs, required output, acceptance checks, and deadline**.
