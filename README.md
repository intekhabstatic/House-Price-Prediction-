# Movie Recommendation System

A content-based movie recommendation system built using Python and
Scikit-learn. The system recommends movies similar to a movie selected
by the user based on information such as genres, keywords, cast,
director, and overview.

## Project Overview

The purpose of this project is to understand how a basic movie
recommendation system works using movie metadata.

This project uses a content-based filtering approach. Instead of relying
on user ratings or watch history, the system compares the content and
features of movies to find similar movies.

For example, when a user selects:

``` text
Batman Begins
```

the system calculates the similarity between this movie and other movies
in the dataset and returns the top 5 similar movies.

## How It Works

The recommendation system follows these steps:

1.  Load the movie and credits datasets.
2.  Merge the two datasets using the movie title.
3.  Select the important movie features.
4.  Remove missing values.
5.  Extract genres, keywords, cast, and director information.
6.  Combine the selected information into a `tags` feature.
7.  Convert the text data into numerical vectors using
    `CountVectorizer`.
8.  Calculate similarity between movies using cosine similarity.
9.  Return the top 5 most similar movies.

## Features Used

The recommendation system uses the following movie information:

-   Movie overview
-   Genres
-   Keywords
-   Top cast members
-   Director
-   Movie title
-   Movie ID

These features are combined to create a representation of each movie.

## Technologies Used

  Technology         Purpose
  ------------------ -----------------------------------------------
  Python             Main programming language
  Pandas             Data loading and preprocessing
  NumPy              Numerical operations
  NLTK               Text preprocessing
  Scikit-learn       Feature extraction and similarity calculation
  Jupyter Notebook   Development and experimentation

## Machine Learning Concepts Used

-   Content-Based Filtering
-   Feature Engineering
-   Text Preprocessing
-   Bag of Words
-   CountVectorizer
-   Cosine Similarity
-   Natural Language Processing

## Project Structure

``` text
movie_recommendation_system/
│
├── data/
│   ├── tmdb_5000_movies.csv
│   └── tmdb_5000_credits.csv
│
├── MovieRecommendation.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

## File Description

  -----------------------------------------------------------------------
  File / Folder                       Description
  ----------------------------------- -----------------------------------
  `data/`                             Contains the movie datasets

  `MovieRecommendation.ipynb`         Contains the complete data
                                      preprocessing and recommendation
                                      workflow

  `requirements.txt`                  Contains the Python dependencies

  `.gitignore`                        Specifies files that should not be
                                      tracked by Git

  `README.md`                         Project documentation
  -----------------------------------------------------------------------

## Dataset

This project uses the TMDB 5000 Movies and TMDB 5000 Credits datasets.

The datasets contain information about movies such as:

-   Movie titles
-   Movie overview
-   Genres
-   Keywords
-   Cast
-   Crew

The CSV files are expected to be inside the `data` folder.

## Installation

Clone the repository:

``` bash
git clone https://github.com/intekhabstatic/movie_recommendation_system.git
```

Go to the project directory:

``` bash
cd movie_recommendation_system
```

Install the required Python libraries:

``` bash
pip install -r requirements.txt
```

## Running the Project

Open the following notebook:

``` text
MovieRecommendation.ipynb
```

Run the notebook cells in order.

After the preprocessing and similarity calculation are completed, use
the recommendation function:

``` python
recommend('Batman Begins')
```

The function returns the top 5 movies that are most similar to the
selected movie.

## Example

``` python
recommend('Batman Begins')
```
![Movie Recommendation Output](recommendation-output.png)

The system compares `Batman Begins` with other movies using cosine
similarity and returns the most similar movies.

## Limitations

This project has some limitations:

-   It does not use user ratings.
-   It does not consider individual user preferences.
-   It does not use watch history.
-   It does not implement collaborative filtering.
-   The quality of recommendations depends on the available movie
    metadata.
-   Movies with incomplete information may produce less accurate
    recommendations.

## Future Improvements

The project can be improved in several ways:

-   Build a web interface using Streamlit.
-   Add movie posters to the recommendations.
-   Display similarity scores.
-   Improve the text preprocessing process.
-   Experiment with TF-IDF.
-   Use word embeddings or transformer-based embeddings.
-   Add collaborative filtering.
-   Build a hybrid recommendation system.
-   Deploy the application online.

## What I Learned

Through this project, I learned and practiced:

-   Data preprocessing using Pandas
-   Feature engineering
-   Text preprocessing
-   Natural Language Processing basics
-   Bag-of-Words representation
-   CountVectorizer
-   Cosine similarity
-   Content-based recommendation systems
-   Working with real-world datasets
-   Building an end-to-end machine learning project

## Author

**Intekhab Alam**

BTech CSE student

## Project Goal

The goal of this project is to understand the fundamentals of
recommendation systems and learn how movie metadata can be processed and
used to generate content-based movie recommendations.
