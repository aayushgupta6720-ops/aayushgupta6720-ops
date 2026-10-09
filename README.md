# Hi, I'm Aayush

Computer Science undergraduate at Jaypee University of Engineering & Technology (B.Tech, 2027), based in Guna, Madhya Pradesh.

I build AI systems that automate real work, and I use data to figure out what's worth building. I care most about the parts that make AI trustworthy: testing its output before relying on it, knowing when to hand a decision to a human, and making every run observable.

Currently looking for internships in AI engineering, applied AI, and data-driven business roles.

## Projects

**[Options Pricing & Volatility Lab](https://github.com/aayushgupta6720-ops/options-pricing-lab)** — option pricing models on real NSE data · [Live demo](https://options-pricing-lab.onrender.com)

Rebuilds the implied volatility surface for NIFTY, BANKNIFTY and RELIANCE from NSE's official end-of-day files, every trading day since July 2024, and calibrates Heston, SABR and rough Bergomi to it each evening. Prices vanilla and exotic options (Asian, barrier, lookback) under all three models, with variance reduction that cuts Monte Carlo variance about 200,000×. Findings include implied vol exceeding the volatility that followed on 67% of NIFTY days, and Black-Scholes pricing a NIFTY barrier option at ₹109 against ₹155 under the calibrated smile models. Uses live NIFTY prices from NSE during market hours; 225 automated tests.

`Python · NumPy · SciPy · numba · Streamlit · Plotly · GitHub Actions`

**[support-rag-agent](https://github.com/aayushgupta6720-ops/support-rag-agent)** — AI assistant for support tickets · [Live demo](https://support-rag-agent.onrender.com)

A help center for a fictional ticketing product, with the agent as its chat widget. A LangGraph agent decides when to search the knowledge base and when to answer directly, cites the articles it used, and keeps multi-turn sessions and per-visitor rate limits in Redis. Answers are graded against a 97-case golden set by an LLM-as-judge (97/97 on the latest run, including an 11-case held-out split), thumbs-down ratings become draft eval cases, and every call logs its latency, token usage and cost. Also available as an MCP server.

`Python · FastAPI · LangGraph · Qdrant · Redis · Gemini API · Docker · MCP`

**[api-dependabot](https://github.com/aayushgupta6720-ops/api-dependabot)** — AI agent for automated code maintenance · [Live dashboard](https://aayushgupta6720-ops.github.io/api-dependabot/)

Watches Stripe's Node SDK for breaking changes, finds the affected code through AST analysis, and opens one fix pull request per file using Gemini. Changes with no safe replacement become "Needs review" PRs instead of guessed fixes, and retries never duplicate or reopen a rejected fix. It runs daily on GitHub Actions, replays an eval harness of 13 real breaking changes from Stripe's changelog every week, and publishes its run history and eval pass rates to a live dashboard.

`TypeScript · Node.js · ts-morph · Octokit · Gemini API · GitHub Actions`

**[AI Student Assistant](https://github.com/aayushgupta6720-ops/AI_Student_Assistant)** — a study-notes chatbot built in five layers · [Live demo](https://ai-student-assistant-hz02.onrender.com)

Built to show how a production AI app is organised: client, intelligence, inference, knowledge and tools, each its own package, with a test that fails if a layer imports across the line. Answers stream token by token and call six tools, from note search to a web page reader. It retrieves over your own uploaded notes, including scanned PDFs that Gemini transcribes, and shows under every answer which layer did the work and how long it took. Its 20-question answer evaluation passes 20/20.

`Python · FastAPI · Gemini API · SQLite · NumPy · Server-Sent Events`

**[E-Commerce Product Analytics Dashboard](https://github.com/aayushgupta6720-ops/ecommerce-analytics-dashboard)** — interactive sales and customer analytics · [Live demo](https://ecommerce-analytics-dashboard-aapp.onrender.com)

Interactive dashboard over 1M invoice lines from a UK online retailer (UCI Online Retail II). Ten pages cover revenue trends, product concentration (22% of products bring in 80% of revenue), RFM customer segments (Champions are 14% of customers but 52% of revenue), cohort retention, market-basket rules, returns, five sized recommendations, and predictions scored on a holdout year (churn AUC 0.759 against a 0.707 baseline). Every metric is unit-tested, the core metrics also run as SQL in DuckDB, and a Power BI kit rebuilds the same model with tie-out numbers that match the app.

`Python · Pandas · Streamlit · Plotly · SciPy · DuckDB · Power BI · DAX`

## What I work with

- **AI:** LLM applications, RAG, AI agents (LangGraph), tool calling and MCP, evaluation (golden sets, LLM-as-judge), prompt engineering
- **Data:** SQL and DuckDB, Python (Pandas, NumPy, SciPy, Matplotlib), Streamlit and Plotly dashboards, Power BI, Excel
- **Quantitative finance:** option pricing (Black-Scholes, binomial trees, Monte Carlo), stochastic and rough volatility models (Heston, SABR, rough Bergomi), model calibration
- **Engineering:** Python (FastAPI), TypeScript, Node.js, React, Docker, Git, GitHub Actions, Render
- **Design:** Figma and design systems — as a UI/UX intern at Assemble Esports, I built a design system adopted across 7 products

## Get in touch

[Email](mailto:aayushgupta6720@gmail.com) · [LinkedIn](https://linkedin.com/in/aayush-gupta6720)

