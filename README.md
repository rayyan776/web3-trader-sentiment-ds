
# Trader Behavior vs Market Sentiment - Web3 Trading Team Assignment

#Please run all the cells of the notebook first, for creating the project structure on run.


## One-Click Access
- Colab (view-only): <https://colab.research.google.com/drive/1NoK9SeFmne5Ci7rSjE8JNZTUKl_scZaT?usp=sharing>
- GitHub repo: <https://github.com/rayyan776/web3-trader-sentiment-ds.git>


Make sure Colab sharing is set to "Anyone with the link can view" and the GitHub repo is public.

## How to Run (Colab)
1. Open `notebook_1.ipynb` in Google Colab.
2. Run the setup cell to install packages and download both datasets (Hyperliquid trades + Fear & Greed Index).
3. Execute all cells. This will:
   - Clean and merge datasets; engineer `pnl_after_fees`, `is_win`, `regime`.
   - Run the 8 differentiators (analytics, stats, backtests).
   - Export CSVs to `csv_files/` and PNGs to `outputs/`.


## Data Sources
- Historical Trader Data (Hyperliquid): Google Drive link provided by the assignment.
- Bitcoin Fear & Greed Index: Google Drive link provided by the assignment.

## Deliverables
- Eight differentiators with statistical validation and regime-aware insights.
- High-resolution charts for each differentiator and an executive dashboard.
- Calibrated win-probability model with decile lift and policy backtest.
- `ds_report.pdf` summarizing findings and an actionable trading policy.

## Key Insights (Brief)
- Behavior × Regime: Contrarian wins in Fear; Momentum wins in Greed; chi-square confirms dependence.
- Order Type: Makers outperform net of fees; Taker vs Maker PnL differs significantly (Mann-Whitney).
- Regime Validity: T-test/ANOVA/chi-square show outcomes depend on sentiment; calibration enables profitable filtering.
- Policy: Trade only when predicted decile >= 10 (>= 9 in Fear), route Maker in Fear and Taker in Greed under score gating.

## Reproducibility Notes
- Randomness: Sensitivity sampling uses fixed seeds where applicable.
- Environment: Google Colab (Python 3.10+). Report build auto-installs Pandoc/LaTeX or uses HTML->PDF fallback.
- Filenames: Charts are saved with prefix `differentioator_XX_*` and referenced consistently in the report.

## Contact
For questions about this submission or to request raw notebooks/exports, please reach out: <rayyanmohmmed49@gmail.com>
