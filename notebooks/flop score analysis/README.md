# Notebook 03: Flop Score & EDA

This notebook defines a custom **Flop Score** and explores the top 10 worst-performing movies using budget and revenue data from TMDb.

## 📈 Outputs
- A saved CSV with flop scores: `enriched_worst_200_with_flop_score.csv`
- A chart of the top 10 flops (also shown in main README)

## 📊 Flop Score Formula

\[
\text{Flop Score} = \left(\frac{\text{budget} - \text{revenue}}{\text{budget}}\right) \times 100
\]

Higher is worse. Only movies with budgets > $1M and known revenue are included.
