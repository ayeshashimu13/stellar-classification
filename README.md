# Predicting Stellar Class 🌌

Given telescope measurements, can we tell whether an object in the night sky
is a **star, a galaxy, or a quasar**? This project classifies 577,000+ space
objects into the three types.

**Result: 0.955 on a live, medal-eligible Kaggle competition (Playground Series S6E6).**

## The approach
- Explored 577K objects across brightness filters (u, g, r, i, z), sky position, and redshift
- Engineered astronomer-style "color" features (differences between filters)
- Compared HistGradientBoosting, LightGBM, and XGBoost with 3-fold cross-validation
- **XGBoost won** (CV 0.967), beating an ensemble — a reminder that the right single model can beat blending

## Key learning
Color-difference features didn't help the tree models (trees already capture those
splits), but switching from HistGradientBoosting to XGBoost gave a real jump. The
algorithm choice mattered more than feature tweaks here.

## Tech
Python · pandas · scikit-learn · XGBoost · LightGBM

## Data
Kaggle Playground Series, Season 6 Episode 6 (Predicting Stellar Class)
