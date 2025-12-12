Housing Recommendation System using KNN

This project implements a housing recommendation system using the **K-Nearest Neighbors (KNN)** algorithm to suggest rental listings based on user-defined preferences. The model is built in Python and uses basic preprocessing techniques and cosine similarity for neighbor retrieval.


Project Overview

The system processes a dataset of rental listings and provides personalized recommendations by:

- Cleaning and preprocessing raw housing data
- Encoding categorical variables
- Normalizing features
- Applying the KNN model with cosine similarity
- Defining a dynamic recommendation function using user input

Workflow Summary

1. **Import Libraries**: 
   - Uses `pandas`, `numpy`, `sklearn`, etc.

2. **Load Dataset**: 
   - Reads rental data from a CSV file.

3. **Preprocessing**:
   - Drops irrelevant columns and rows.
   - Cleans the `rent` column to remove non-numeric values.
   - Encodes categorical data using label encoding.
   - Normalizes all features to a range of `[0, 1]`.

4. **Model Setup**:
   - Combines numerical and encoded categorical columns to form a feature matrix.
   - Uses the K-Nearest Neighbors model with `n_neighbors=6` and `metric='cosine'`.

5. **Recommendation Function**:
   - Accepts any number of user-defined attributes via `**kwargs`.
   - Validates user input against dataset columns.
   - Queries the trained KNN model to return the top 6 similar listings.
Example Usage

```python
recommend_housing(location='Bangalore', BHK=2, size=1000)
```
You can enter any number of criteria to get relevant recommendations.

Requirements

- Python 3.7+
- pandas
- numpy
- scikit-learn

Output

The system returns the top 6 housing listings most similar to the user's preferences based on cosine similarity.
