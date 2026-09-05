# Rohan Mukherjee

Control management analyst at Wells Fargo, covering Wealth & Investment Management and CIB Operations. I build institutional-style portfolio analytics in Python - the kind of tooling that sits behind an allocation decision or a performance review meeting. CFA Level I candidate, November 2026.

The through-line across these projects: **implement the math from its formula, then prove it.** Every metric is written out explicitly rather than pulled from a library, unit-tested against hand-computed values, and cross-checked against an established package only as an independent reference. Reconciliation identities are asserted, not assumed. Assumptions and limitations are stated in the README rather than buried.

---

## Selected work

### [Active Return Attribution Toolkit](https://github.com/rohanmuk/Performance-attribution-factor-analysis)
Explains a US equity portfolio's performance against its benchmark two complementary ways and shows they tell one story. Holdings-based **Brinson-Fachler** attribution splits active return into allocation, selection, and interaction by GICS sector, with **Carino geometric linking** so single-period effects compound exactly to cumulative active return (reconciliation error ~5.8e-15). Returns-based factor attribution regresses portfolio, benchmark, and active returns on **CAPM / FF3 / FF5 / Carhart**, with **Newey-West** HAC standard errors, factor-contribution decomposition, and rolling 36-month betas to expose style drift. All regression and attribution math is hand-rolled in numpy; `statsmodels` appears only in the tests as a parity check.

### [Systematic Strategy Backtester & Performance Attribution Platform](https://github.com/rohanmuk/Systematic-Strategy-Backtester-Performance-Attribution-Platform)
Backtests multi-asset allocation strategies - static weights, equal weight, inverse vol, equal-risk-contribution risk parity, min-variance, target-vol, and glide-path - and evaluates them the way a portfolio analyst would: relative to a policy benchmark. Reports active return, tracking error, information ratio, up/down capture, and per-asset contribution to return and to risk, with transaction costs and turnover modeled explicitly. The test suite asserts the engine's invariants directly: weights sum to one, capital is conserved period by period, and perturbing only the final month leaves every earlier decision bit-identical (no lookahead).

### [Portfolio Construction & Risk Analytics Engine](https://github.com/rohanmuk/Portfolio-Construction-Risk-Analytics-Engine)
Portfolio optimization (Markowitz, risk parity) and institutional-grade risk analytics - VaR/CVaR, factor exposure, and stress testing.

### [Goals-Based Wealth & Retirement Planning Simulator](https://github.com/rohanmuk/Goals-Based-Wealth-Retirement-Planning-Simulator)
Tax-aware retirement planning with Monte Carlo projections, optimal withdrawal sequencing, and Social Security claiming analysis.

### [Trade Surveillance & Risk Dashboard](https://github.com/rohanmuk/trade-surveillance-risk-dashboard)
A Python and Streamlit dashboard over **simulated** trade activity, flagging unusual trading patterns, concentration risk, large notional trades, and operational risk indicators.

### [DCF & Comparables Valuation Model](https://github.com/rohanmuk/DCF-Comparables-Valuation-Model-)
Discounted cash flow and trading comparables valuation in Python.

---

## Background

BS Finance, University of Illinois Gies College of Business. Previously client-facing work at Intapp serving hedge fund and private equity clients, and a risk and compliance internship at EY. I also write cross-asset notes on rates, credit, commodities, and positioning.

Everything here is personal work built on public data - yfinance, the Ken French Data Library, and simulated inputs. Nothing in these repositories derives from any employer's data or systems.

📍 Charlotte, NC · [LinkedIn](https://www.linkedin.com/in/rohanmuk)
