# Movie Genre Classifier

This repository implements a multi-label classification model to predict movie genres based on their plot summaries. The project combines **NLP techniques**, **TF-IDF vectorization**, and **Logistic Regression** to develop a robust genre prediction system.

---

## Features
- **Multi-Label Classification**: Predicts multiple genres for a single movie.
- **Data Preprocessing**:
  - Cleaning text by removing special characters and stopwords.
  - Stemming words to their root forms.
- **Genre Encoding**: Uses `MultiLabelBinarizer` to encode genres as target variables.
- **Feature Extraction**: Applies `TfidfVectorizer` to convert text into numerical features.
- **Model Training**:
  - Utilizes Logistic Regression with a One-vs-Rest strategy for classification.
  - Supports threshold tuning for optimizing predictions.

---

## Dataset

The project uses two datasets:
1. **`movie_metadata.tsv`**: Contains metadata like movie IDs, names, and genres (in JSON format).
2. **`plot_summaries.tsv`**: Contains movie IDs and their plot summaries.

### Data Cleaning Steps
1. Renamed relevant columns for better readability.
2. Merged `movie_metadata` and `plot_summaries` datasets on `movie_id`.
3. Removed rows with zero genres.

---

## Visualizations

- Displayed the distribution of the top 50 most frequent genres in the dataset.
- Generated bar plots using **matplotlib** and **seaborn**.

---

## Model

- **Algorithm**: Logistic Regression with One-vs-Rest Classifier.
- **Evaluation**:
  - F1 Score: Achieved a micro F1 score of **0.60** with a threshold of 0.3.

---

