# Data Analysis Pipeline

This repository contains a data analysis pipeline that processes sales data and generates insights.

## Overview

The pipeline:
1. Reads sales data from `data.csv`
2. Computes revenue metrics
3. Calculates top products by revenue
4. Generates rolling 7-day revenue averages by region
5. Outputs results as JSON

## Files

- `execute.py`: Main Python script that performs the data analysis
- `data.csv`: Input data file containing sales records
- `.github/workflows/ci.yml`: GitHub Actions workflow for CI/CD

## CI/CD Pipeline

The GitHub Actions workflow:
1. Runs `ruff` linter for code quality checks
2. Executes `execute.py` to generate `result.json`
3. Publishes the results to GitHub Pages

## Requirements

- Python 3.11+
- pandas 2.2.3+

## Running Locally

```bash
# Install dependencies
pip install pandas==2.2.3

# Run the analysis
python execute.py > result.json
```

## Output

The script generates a JSON file with:
- Total row count
- Number of distinct regions
- Top 3 products by revenue
- Rolling 7-day revenue averages by region

## GitHub Pages

Results are automatically published to GitHub Pages after each push to the main branch.