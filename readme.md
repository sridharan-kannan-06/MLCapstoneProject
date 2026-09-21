# Machine Learning Capstone Project

A case study comparing classical ML algorithms on two real-world datasets, one regression problem and one classification problem.

## Datasets

| Dataset | Rows | Target | Task |
|---------|------|--------|------|
| [Online News Popularity](https://archive.ics.uci.edu/dataset/332/online+news+popularity) | 39,644 articles | `shares` | Regression |
| [Airline Passenger Satisfaction](https://www.kaggle.com/datasets/mohamedsyoussef/airline-data-and-cleaned-dataset) | 103,904 passengers | `satisfaction` | Classification |

Both use an 80/20 train-test split (seed 42) with stratification.

## Repo Structure

```
eda/                  EDA and preprocessing notebooks
review1/              Model training and evaluation notebooks
datasets/             Raw CSV files
processed_datasets/   Cleaned, split, and scaled CSVs
results/              Model comparison tables
```

## Setup

```bash
pip install numpy pandas scikit-learn matplotlib seaborn ipykernel nbformat nbclient threadpoolctl
```

## Results

| Task | Best Model | Key Metrics |
|------|-----------|-------------|
| Regression (News) | Linear Regression | R2 = 0.0192, MAE = 3,029 shares |
| Classification (Airline) | SVC | Accuracy = 95.30%, F1 = 0.9530, ROC-AUC = 0.9886 |

Predicting article virality from metadata alone turned out to be really hard. Most models couldn't beat a simple mean prediction. Airline satisfaction, on the other hand, was much more predictable from the service ratings and flight details.

## Acknowledgements

Dataset sources are linked above. AI was used to understand and explore the datasets and to analyse results. No external notebook code was copied.

## License

This project is licensed under the [MIT License](LICENSE).
