# Song Genre Analysis and Recommendation System

## Description
This project analyzes song lyrics and their genres using matrix decomposition. By applying TF-IDF (Term Frequency - Inverse Document Frequency), the algorithm assigns higher weights to unique, meaningful words rather than common prepositions. Singular Value Decomposition (SVD) is then used to reduce the dimensionality of the text matrix, allowing us to map and visualize the songs in a geometric space based on their latent topics. The project also features a Telegram bot that acts as a recommendation system, suggesting similar songs using cosine similarity.

## Project Structure

The project consists of three main Jupyter Notebooks:

* `preprocessing_dataset.ipynb`
  This notebook handles the initial data loading and cleaning. It downloads the Genius Song Lyrics dataset, filters the data, and prepares a clean CSV file that will be used for modeling.

* `project.ipynb`
  The core machine learning pipeline. It loads the cleaned dataset, builds a TF-IDF matrix to extract the semantic weight of words, and applies Truncated SVD to compress the vectors. It includes visualizations to plot the songs in a multi-dimensional space, revealing the hidden geometry of different music genres.

* `appliation_recsys.ipynb`
  The practical application of the model. It loads the precomputed vectors and uses cosine similarity to find the nearest neighbors for any given song. It also includes the code to launch a Telegram bot that interacts with users and provides top-5 song recommendations along with Spotify links.

## Installation

To run the notebooks, you need to install the required Python libraries. You can install them using the following command:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn plotly pyTelegramBotAPI
```

How to Run
Open and run preprocessing_dataset.ipynb to process the raw lyrics and generate the cleaned dataset.

Open and run project.ipynb to train the TF-IDF vectorizer, perform SVD, and view the genre projections.

Open appliation_recsys.ipynb, insert your Telegram bot token where required, and execute the cells to start the recommendation bot.
