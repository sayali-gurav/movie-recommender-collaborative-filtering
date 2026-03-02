# 🎬 Movie Recommendation Engine — Collaborative Filtering & Matrix Factorization

## Business Problem
Streaming platforms live and die by their recommendation quality. This project builds and benchmarks multiple recommendation algorithms on real user-movie rating data to identify which approach delivers the most accurate personalized recommendations — and why.

## Dataset
**MovieLens Small Dataset** — 100,000 ratings from 700 users across 9,000 movies  
Source: [Kaggle — The Movies Dataset](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset)  
Rating scale: 0.5 ⭐ to 5.0 ⭐

---

## Approach & Methods

### Models Compared
| Model | Type | Description |
|---|---|---|
| PMF (SVD, unbiased) | Matrix Factorization | Decomposes the user-item matrix into latent factors |
| User-CF | Collaborative Filtering | Recommends based on similar users' preferences |
| Item-CF | Collaborative Filtering | Recommends based on similar items to what you've rated |

### Experiments
1. **Baseline comparison** — RMSE & MAE across all 3 models using 5-fold cross-validation
2. **Similarity metric impact** — Tested Cosine, MSD, and Pearson correlation for both User-CF and Item-CF
3. **Neighbor tuning** — Swept k from 10 to 100 in steps of 10 to find the optimal neighborhood size

### Evaluation Metrics
- **RMSE** (Root Mean Squared Error) — penalizes large prediction errors
- **MAE** (Mean Absolute Error) — average magnitude of prediction error

---

## Key Results

- **Item-CF with Cosine similarity** achieved the lowest RMSE across similarity experiments
- Increasing neighbors (k) improved accuracy up to a point, then plateaued — suggesting diminishing returns beyond k=40
- PMF (SVD) was competitive with CF approaches despite requiring no explicit similarity computation
- User-CF was more sensitive to similarity metric choice than Item-CF

---

## Skills Demonstrated
`Python` `Scikit-Surprise` `NumPy` `Pandas` `Matplotlib` `Cross-Validation` `Hyperparameter Tuning` `Collaborative Filtering` `Matrix Factorization` `Recommender Systems`

---

## How to Run
```bash
pip install scikit-surprise numpy pandas matplotlib
jupyter notebook matrix-data-for-recommender-systems.ipynb
```

> **Note:** Requires the MovieLens dataset from Kaggle. Download and place `ratings_small.csv` in your working directory or update the path in the notebook.

---

## Files
```
matrix-data-for-recommender-systems.ipynb   # Main notebook
```

---

## Author
**Sayali Gurav**  
MS Data Science, Analytics & Engineering — Arizona State University  
[LinkedIn](https://linkedin.com/in/sayaligurav) | [GitHub](https://github.com/sayali-gurav)
