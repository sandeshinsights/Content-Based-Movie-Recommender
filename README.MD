Movie Recommendation System

This project builds a movie recommendation system using a content-based method. It suggests movies based on how similar their descriptions (like genre, cast, and plot) are to each other.

Demo

Here is a screenshot of the Streamlit app running locally:
![Movie Recommender Screenshot](https://github.com/sandeshinsights/Content-Based-Movie-Recommender/blob/8a5873df7ccd1f5b5d3d84db9ac216ad0cbed678/Screenshot%202025-07-14%20174357.png)

Data Used

The system uses the TMDB 5000 Movie Dataset. You can find this dataset on Kaggle. It comes in two files: tmdb_5000_movies.csv and tmdb_5000_credits.csv.

How to Get Started

What You Need:

- Python version 3
- pandas library
- numpy library
- scikit-learn library
- nltk library

Install these libraries using pip:

pip install pandas numpy scikit-learn nltk

Setting Everything Up:

1. Download the two dataset files (tmdb_5000_movies.csv and tmdb_5000_credits.csv) from Kaggle.
2. Put these files where your Python code can access them. The code here expects them in /content/drive/MyDrive/Movies/. You might need to change the paths in the code if your files are somewhere else.
3. Make sure you have nltk data downloaded. Run this in Python:

import nltk
nltk.download('punkt')

How to Run the Code:

1. Open the Python file or Jupyter Notebook with the code.
2. Run all the steps in the code.
3. The code will:
    - Load and combine the movie data.
    - Clean and prepare the data, focusing on things like genres, cast, and plot summary.
    - Create a 'tags' feature by combining these prepared parts.
    - Use a tool called CountVectorizer to turn the text tags into numbers.
    - Figure out how similar movies are to each other using these numbers.
    - Create a function called 'recommend' that takes a movie title and gives you a list of similar movies.
4. To get recommendations for a movie, use the 'recommend' function like this:

recommend('Gandhi')

How the System Works

It uses content-based filtering:

1. Data Loading: The movie and credit data are loaded and linked together by movie title.
2. Data Prep: Important information like genres, actors, and directors is taken out and cleaned. The plot summary is broken into words.
3. Feature Creation: A new 'tags' section is made by putting together the cleaned plot summary, genres, keywords, actors, and directors.
4. Text to Numbers: The 'tags' are turned into numbers using CountVectorizer so the computer can understand them.
5. Finding Similarity: The system calculates how similar the numerical representations of the movies are.
6. Recommendations: When you ask for recommendations for a movie, the system finds the movies with the most similar numerical representation.

Main Files

- tmdb_5000_movies.csv: Has movie details.
- tmdb_5000_credits.csv: Has cast and crew details.
- The Python file or notebook with the recommendation code.
