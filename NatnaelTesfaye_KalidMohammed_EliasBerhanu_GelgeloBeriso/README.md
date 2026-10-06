# Qiyas Hackathon Ethiopian Smallholder Crop-Yield Challenge

**Title:** Crop Yield Forecasting
**Members:** 
- Natnael Tesfaye (qiyas-2026-004013) 
- Kalid Mohammed (qiyas-2026-006697) 
- Elias Berhanu (qiyas-2026-002030) 
- Gelgelo Beriso (qiyas-2026-000133) 
- Alemedin Kiyar (qiyas-2026-006942)

## Summary
A reproducible regression workflow for Ethiopian smallholder crop-yield forecasting. The final model uses plot-level agronomic inputs plus growing-season weather features; market price is excluded from yield modeling and used for revenue analysis/demo.

## Validation
- RMSE: **0.473 t/ha**
- MAE: **0.349 t/ha**
- R²: **0.880**
- 5-fold RMSE: **0.488 ± 0.013 t/ha**
- 2024 out-of-time RMSE: **0.506 t/ha**

The hidden leaderboard score is not known until official scoring.

## Setup
```bash
pip install -r requirements.txt
```
Demo:
```bash
pip install -r app/requirements.txt
python app/app.py
```

## Notebook order
1. `notebooks/01_cleaning_and_integration.ipynb` — A
2. `notebooks/02_analysis_report.ipynb` — B
3. `notebooks/03_visualizations.ipynb` — C
4. `notebooks/04_modeling_and_evaluation.ipynb` — D

## Deliverables
A: `reports/A_cleaning_and_integration.md` + cleaning/join/feature/check files + `data/processed/`.
B: `reports/B_analysis_report.md`.
C: exact `fig01`–`fig12` PNGs + `figure_captions.md`.
D: `reports/D_model_evaluation.md`, model/tuning/CV/ablation/error files, `models/final_model.joblib`.
E: `app/app.py` + bundled weather/price assets.
F: `presentation/team_qiyas_crop_yield_slides.pptx`.
G: README + pinned requirements + valid submission.

## Submission
`submission/team_qiyas_crop_yield_submission.csv` contains exactly `plot_id` and `predicted_yield_tons_per_ha`, 3,750 rows, original order, unique IDs and numeric predictions.

## Hygiene
Weather-derived features are included in the final model; price is not. Raw files are unchanged. Cleaning and model preprocessing statistics are derived from training data. Random seed is 42.
