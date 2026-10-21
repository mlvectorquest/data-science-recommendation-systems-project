# Recommendation Systems with IBM

Udacity Data Science project. It builds article recommenders for users of the IBM Watson Studio community, using real user-article interaction data.

## What the notebook does

`starter/Recommendations_with_IBM.ipynb` has five parts:

1. **Exploratory data analysis**: users, articles and interactions.
2. **Rank-based recommendations**: the most-read articles. Used for new users with no history.
3. **User-user collaborative filtering**: recommend articles read by users with similar reading history.
4. **Content-based recommendations**: TF-IDF and latent semantic analysis on article titles.
5. **Matrix factorization**: SVD of the user-item matrix. The number of latent features (200) is chosen from the accuracy, precision and recall table and plot. Because those scores are measured on the same matrix the model was fitted to, they only show how well it reconstructs the data, so the notebook also explains why they can't be used to pick the number on their own.

## Getting started

Requires Python 3.13 (the version of the project's virtual environment).

```
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook starter/Recommendations_with_IBM.ipynb
```

Run all cells from the top. The data is `starter/data/user-item-interactions.csv`.

## Tests

`starter/project_tests.py` holds the checks the notebook calls after each exercise. They run inside the notebook and print whether your answer is correct.

## Exporting for submission

The last notebook cell converts the saved notebook to HTML:

```
python -m nbconvert --to html starter/Recommendations_with_IBM.ipynb
```

Save the notebook before running it, because it converts the file on disk. For PDF use `--to webpdf` (needs `pip install "nbconvert[webpdf]"` and `playwright install chromium`) or `--to pdf` (needs LaTeX and pandoc).

## Built with

* [pandas](https://pandas.pydata.org) and [NumPy](https://numpy.org): data handling
* [scikit-learn](https://scikit-learn.org): TF-IDF, SVD and metrics
* [Matplotlib](https://matplotlib.org): plots
* [Jupyter](https://jupyter.org) and nbconvert: notebook and export

## License

[License](LICENSE.txt)
