# Flop Score Distribution Visualization

This notebook visualizes the distribution of flop scores for the **worst 200 movies** based on the enriched IMDb dataset.

## Overview

The **flop score** is a metric combining movie budget, revenue, and audience ratings to identify movies that performed poorly commercially and critically.

This notebook creates a histogram with a kernel density estimate (KDE) to display the spread of flop scores, highlighting the 50% threshold used to categorize movies as "flops."

## Key Insights

- The **blue bars** show the count of movies in different flop score ranges.
- The **blue KDE curve** provides a smooth estimate of the overall flop score distribution.
- The **red dashed vertical line** indicates the 50% cutoff threshold distinguishing flops from non-flops.

## Why This Matters

- Helps to visualize the distribution of poor-performing movies.
- Validates the choice of the 50% threshold for defining a flop.
- Supports further analysis, including classification and predictive modeling of movie flops.

## How to Use

1. Upload your `enriched_worst_200_with_flop_score.csv` dataset when prompted.
2. Run all cells to generate the visualization.
3. Use the plot to understand flop score dynamics and class balance for modeling.

---

**Note:** This notebook is part of the larger IMDb Flop Score Analysis project. For more details, visit the [project repository](https://github.com/yourusername/imdb-flop-score).
