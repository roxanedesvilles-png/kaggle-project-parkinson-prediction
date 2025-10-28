# Parkinson’s Disease Progression Prediction

This project is based on the AMP® Parkinson’s Disease Progression Prediction (https://www.kaggle.com/competitions/amp-parkinsons-disease-progression-prediction/overview) Kaggle competition.

All analyses and model development were performed using **Python**, with libraries including **pandas, numpy, scikit-learn, Keras, TensorFlow, matplotlib, seaborn, and ydf**.


## Data Exploration

- Conducted exploratory data analysis (EDA) to examine dataset structure and identify potential clusters or patterns.

- Applied dimensionality reduction techniques such as **PCA and UMAP** to visualize groupings among samples.


## Data Processing

Handled missing values with two imputation strategies :

- Median imputation

- Linear interpolation (later recognized as problematic due to lack of linearity in NPX data)

The goal was to compare the effect of each method on model performance.


## 🤖 Model Development

- Multilayer Perceptron (MLP) neural network for capturing non-linear relationships.

- Random Forest (RF) regressor as a robust baseline for noisy data and small sample sizes.


## Observations

Identified a data leakage issue: imputation was performed before train-test split or cross-validation.

The same problem was observed in subsequent strategies, highlighting the need for proper pipeline structuring.


##  Discussion

Both models struggled due to high data noise and limited predictive signal.

Clinical data were sparse, further restricting model performance.

Comparison with the competition winner’s strategy showed the importance of advanced feature engineering and data integration.


## Getting Started

To run the notebook and reproduce results:

1. The dataset is available on Kaggle, here : https://www.kaggle.com/competitions/amp-parkinsons-disease-progression-prediction/overview

2. Open Google Colab.

3. Upload notebook.ipynb or open it directly from the repository.

4. Run the cells sequentially — all required libraries (pandas, numpy, scikit-learn, TensorFlow, Keras, matplotlib, seaborn, ydf) are pre-installed on Colab.
