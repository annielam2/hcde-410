# A3 — Watching the Machine

Annie Lam · HCDE 410 · Assignment 3

A small mixed-methods study of LLM reliability and reproducibility. I gave LLMs a fixed prompt asking for NVIDIA (NVDA) stock's total and annualized return from 13 monthly closing prices (Jan 2024–Jan 2025), checked every answer against my own Python calculation, and observed two people doing the same task with their usual chatbot.

## Files

| File | What it is |
|---|---|
| `A3_watching_the_machine_starter.ipynb` | The full write-up: prior practice, reproducibility probe, observation, synthesis, and AI-use disclosure |
| `nvda_monthly.csv` | Input data: NVDA monthly closing prices (split-adjusted) from Yahoo Finance via `yfinance` |
| `a3_runs.csv` | Run log: 4 probe runs (3× Gemini, 1× ChatGPT) plus 2 participant runs, with prompt, model, version, timestamp, full output, verification, and notes |
| `a3_codes.csv` | Field-note observations coded into themes |

## How to run

Open the notebook and run all cells. Dependencies:

- `pandas`
- `yfinance` (installed by the first cell)

The notebook downloads the NVDA prices only if `nvda_monthly.csv` is missing. Otherwise it uses the saved file, so the input data stays fixed and results are reproducible.

## Privacy

Participants are identified only as P1 and P2. No names, recordings, or identifying details are included.

## License

Starter materials released under the MIT License — see [`LICENSE`](./LICENSE).
