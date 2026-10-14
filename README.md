# Hi, I'm Aayush

Computer Science undergraduate at Jaypee University of Engineering & Technology (B.Tech, 2027), based in India.

I build AI systems that automate real work, and I use data to figure out what's worth building. I care most about the parts that make AI trustworthy: testing its output before relying on it, knowing when to hand a decision to a human, and making every run observable.

Currently looking for internships in AI engineering, applied AI, and data-driven business roles.

## Projects

**[Options Pricing & Volatility Lab](https://github.com/aayushgupta6720-ops/options-pricing-lab)** — option pricing models on real NSE data · [Live demo](https://options-pricing-lab.onrender.com)

Rebuilds the implied volatility surface for NIFTY, BANKNIFTY and RELIANCE from NSE's official end-of-day files, back to July 2024 and updated every trading evening, and fits Heston and SABR to each day (rough Bergomi for NIFTY). Prices vanilla and exotic options (Asian, barrier, lookback) under Black-Scholes, Heston, local volatility and rough Bergomi, and shows how each variance-reduction method's error falls as paths grow. Findings include a variance risk premium of about one vol point on all three underlyings, measured against a variance swap replicated from the option strip, though with intervals that still include zero for both indices, and Black-Scholes pricing a NIFTY barrier option at ₹109 against ₹134–158 under the calibrated smile models. Stale closes that leave a static arbitrage are dropped, and rough Bergomi is fitted on a trading-day clock with its roughness checked across three Monte Carlo seeds; it fits short-dated smiles better than Heston even when Heston gets a long-run variance per expiry, though by only about 0.02 vol points. Uses live NIFTY prices from NSE during market hours; 248 automated tests.

`Python · NumPy · SciPy · numba · Streamlit · Plotly · GitHub Actions`

**[support-rag-agent](https://github.com/aayushgupta6720-ops/support-rag-agent)** — AI assistant for support tickets · [Live demo](https://support-rag-agent.onrender.com)

A help center for a fictional ticketing product, with the agent as its chat widget. A LangGraph agent decides when to search the knowledge base and when to answer directly, cites the articles it used, and keeps multi-turn sessions and per-visitor rate limits in Redis. Answers are graded by an LLM-as-judge that agreed with a person's labels on 29 of 30 answers and is cross-checked by a second model family: 113/115 on the developer's cases at the deployed settings, and 44/45 on 45 cases written by someone outside the project from the help articles alone. A separate check confirms the cited articles back each answer (87 of 89). A tool-loop agent was built and evaluated against it, and not shipped: it fixed two misses but made three new ones, at twice the cost a question. Every call logs its latency, tokens and cost, and a script turns the logs into p50/p95 and cost per 1,000 questions. Also available as an MCP server.

`Python · FastAPI · LangGraph · Qdrant · Redis · Gemini API · Docker · MCP`

**[api-dependabot](https://github.com/aayushgupta6720-ops/api-dependabot)** — AI agent for automated code maintenance · [Live dashboard](https://aayushgupta6720-ops.github.io/api-dependabot/)

Watches Stripe's Node SDK for breaking changes, finds the affected code through AST analysis, and opens one fix pull request per file using Gemini. Each patch sees the related lines of the release notes (so a removal paired with an addition becomes a rename), is type-checked against the new SDK before its PR opens, and gets one repair try with the compiler's errors; changes with no safe replacement, or that still don't type-check, become "Needs review" PRs instead of guessed fixes. PRs are keyed on the release-notes entry's text, so retries, and later releases that repeat an entry, never duplicate or reopen a rejected fix. It runs daily on GitHub Actions and publishes its run history and eval pass rates to a live dashboard. Its evals type-check every patch against the SDK release it targets, run a real release end to end, and replay a real open-source repo's Stripe upgrade, where it fixes 1 of the 2 breakages with no wrong PRs.

`TypeScript · Node.js · ts-morph · Octokit · Gemini API · GitHub Actions`

**[AI Student Assistant](https://github.com/aayushgupta6720-ops/AI_Student_Assistant)** — a study-notes chatbot built in five layers · [Live demo](https://ai-student-assistant-hz02.onrender.com)

Built to show how a production AI app is organised: client, intelligence, inference, knowledge and tools, each its own package, with a test that fails if a layer imports across the line. Answers stream token by token and call six tools, from note search to a web page reader that opens only links the user typed. It retrieves over your own uploaded notes, including scanned PDFs that Gemini transcribes, and shows under every answer which layer did the work and how long it took. Its answer evaluation counts an answer only if it came from the user's notes, and passes 28/28, including 8 held-out questions about a fictional course that the model can't answer from what it already knows.

`Python · FastAPI · Gemini API · SQLite · NumPy · Server-Sent Events`

**[E-Commerce Product Analytics Dashboard](https://github.com/aayushgupta6720-ops/ecommerce-analytics-dashboard)** — interactive sales and customer analytics · [Live demo](https://ecommerce-analytics-dashboard-aapp.onrender.com)

Interactive dashboard over 1M invoice lines from a UK online retailer (UCI Online Retail II). Eleven pages cover revenue trends, product concentration (22% of products bring in 80% of revenue), RFM customer segments (Champions are 14% of identified customers but 52% of their net revenue), cohort retention, market-basket rules, returns, five sized recommendations, and predictions scored on a holdout year against honest baselines (churn AUC 0.770, a small but real gain over a recency-and-frequency model at 0.758). An *Ask the data* page answers plain-English questions: Gemini turns each one into a structured request and the tested metric code computes the answer, so the model never produces the numbers (28/28 on a golden-set eval). Every metric is unit-tested, the core metrics also run as SQL in DuckDB, and a Power BI kit sets up the same model in DAX, with the app's numbers to tie out against (it hasn't been opened in Power BI Desktop yet).

`Python · Pandas · Streamlit · Plotly · SciPy · DuckDB · Gemini API · Power BI · DAX`

## What I work with

- **AI:** LLM applications, RAG, AI agents (LangGraph), tool calling and MCP, evaluation (golden sets, LLM-as-judge), prompt engineering
- **Data:** SQL and DuckDB, Python (Pandas, NumPy, SciPy, Matplotlib), Streamlit and Plotly dashboards, Power BI, Excel
- **Quantitative finance:** option pricing (Black-Scholes, binomial trees, Monte Carlo), stochastic and rough volatility models (Heston, SABR, rough Bergomi), model calibration
- **Engineering:** Python (FastAPI), TypeScript, Node.js, React, Docker, Git, GitHub Actions, Render
- **Design:** Figma and design systems — as a UI/UX intern at Assemble Esports, I built a design system adopted across 7 products

## Get in touch

[Email](mailto:aayushgupta6720@gmail.com) · [LinkedIn](https://linkedin.com/in/aayush-gupta6720)

