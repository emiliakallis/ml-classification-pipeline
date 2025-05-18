# ML Classification Pipeline: Maximizing Predictive Performance

This project showcases a complete machine learning pipeline to identify the best-performing model for a classification task on a structured dataset. It is designed as a professional portfolio piece to demonstrate proficiency in model comparison, preprocessing, hyperparameter tuning, and ensemble learning.

> Originally completed as part of a course assignment in **March 2025**. The core implementation remains intact, while documentation and comments have been added to enhance clarity and presentation.

## Project Overview

The objective is to classify the target variable `y` based on several categorical, binary, and numerical features. The notebook includes:

- Data loading from external files (e.g., Google Drive or local path)
- Preprocessing steps including encoding and scaling
- Train/test splitting with stratification
- Hyperparameter tuning using [Optuna](https://optuna.org/)
- Evaluation of individual models: **Logistic Regression**, **Random Forest**, **XGBoost**, **LightGBM**
- Stacked ensemble construction and comparison
- Final model selection and predictions on unseen data

## Highlights

- Applied Optuna for automated hyperparameter search across 3 model families
- Built a robust stacked ensemble using tuned base learners
- Evaluated 4 different meta-learners for stacking optimization
- Achieved final test accuracy of **70.5%** on unseen data

## Technologies Used

| Library        | Purpose                        |
| -------------- | ------------------------------ |
| `pandas`       | Data manipulation              |
| `numpy`        | Numerical computing            |
| `scikit-learn` | ML models and preprocessing    |
| `matplotlib`   | Plotting                       |
| `seaborn`      | Statistical data visualization |
| `optuna`       | Hyperparameter optimization    |
| `xgboost`      | Gradient boosting models       |
| `lightgbm`     | Fast gradient boosting models  |

Install dependencies:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn optuna xgboost lightgbm
```

## Best Model Results

After tuning and model comparison, the following stacking ensemble results were obtained:

```
`LogisticRegression`: **0.7040**
`RandomForest`:       **0.7010**
`XGBoost`:            **0.6930**
`LightGBM`:           **0.6880**
```

Final selection: `LogisticRegression` as the meta-learner in the stacking ensemble.

## Final Model Deployment

- The final ensemble was retrained on the full training data
- Final Stacking Accuracy: **0.7050**
- Predictions were made on an unseen dataset
- The predicted labels were saved to a CSV file (not included in the repo)

## What This Demonstrates

- End-to-end model pipeline development
- Clean and reusable notebook structure
- Practical tuning with cross-validation
- Clear, interpretable evaluation logic
- Attention to reproducibility and presentation

## File Structure

```
├── ml_classification_pipeline.ipynb   # Main notebook
├── README.md                          # Project overview (this file)
```

> ⚠️ Input/output data files are excluded from this repository due to privacy or distribution constraints.

## Author Notes

This project was developed as part of a course assignment, then refined to serve as a professional portfolio piece. While the core logic was written during the course, the notebook has been thoroughly commented and organized to highlight clarity, reproducibility, and strong ML workflow practices.

## License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

> Feel free to connect or reach out for collaborations or opportunities.
