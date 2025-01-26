# Algorithms-for-Information-Retrieval-and-Intelligence-Web_UE20CS332

This repository contains solutions to two assignments:

1. **Assignment 1: Implementation of a Search Engine for a given corpus.**
2. **Assignment 2: Implementation of a Recommender System based on a dataset of books, users, and ratings.**

The goal of these assignments was to apply concepts of Information Retrieval and Recommender Systems in practical scenarios using relevant data processing and machine learning techniques.

## Assignment 1: Search Engine Implementation
### Pre-processing Techniques
1. **Case Folding**: Converts all characters to lowercase to ensure consistency and reduce redundancy.
2. **Tokenization**:
    * Sentence Tokenization: Splits text into sentences to preserve contextual meaning.
    * Word Tokenization: Splits sentences into individual words for granular analysis.
3. **Stop Word Removal**: Removes common words that do not contribute significant meaning.
4. **Stemming and Lemmatization**:
    * Stemming: Reduces words to their root forms.
    * Lemmatization: Produces meaningful dictionary forms of words.
5. **TF-IDF Vectorization**: Converts text to numerical form, capturing term importance in a document and across the corpus.

### Data Structures Used
1. **Dictionary**:
    * Used for inverted and positional indexing.
    * Efficient for query intention analysis.
2. **Positional Index**:
    * Stores document IDs and positions of terms for precise phrase querying.
3. **List**:
    * Used for n-gram matching in language models.
4. **Sparse Matrix**:
    * Stores TF-IDF vectors to save memory and optimize similarity computations.

### Similarity Scoring Schemes
1. **Cosine Similarity**: Measures text similarity regardless of document length.
2. **Likelihood Scoring**: Considers the probability of query terms occurring together in text.


## Assignment 2: Recommender System Implementation
### Data Cleaning and Preprocessing
1. **Books Table**:
* Removed unnecessary columns (e.g., image URLs).
* Replaced null values and invalid data with appropriate defaults (e.g., mode of publication year).
* Standardized ISBN values.
2. **Users Table**:
* Replaced invalid ages with the mean of valid ages.
* Split location into city, state, and country columns.
3. **Ratings Table**:
* Removed invalid and duplicate rows.
* Ensured data consistency with the Books table.

### Algorithms Implemented
A. **Popularity-Based Recommendations**
   1. **Globally Popular Books**: Ranked books by total ratings.
   2. **Location-Based Popularity**: Filtered books by user location and sorted by ratings.
   3. **Author/Publisher-Based Recommendations**: Recommended books by the same author or publisher.
   4. **Yearly Popular Books**: Grouped and ranked books by year of publication.
B. **Weighted Average Rating Recommendations**
   * Used a weighted score formula to recommend books with high overall ratings.
C. **Collaborative Filtering**
   * Built a user-item matrix and used cosine similarity to recommend books.
D. **Correlation-Based Recommendations**
   * Computed a correlation matrix to find similar books.
E. **Nearest Neighbor Recommendations**
   * Trained a Nearest Neighbors model on sparse matrices of user-book ratings.
F. **Content-Based Recommendations**
   * Used TF-IDF feature vectors for unigrams and bigrams of book titles.
G. **Hybrid Recommendations**
   * Combined content-based and collaborative filtering methods for enhanced recommendations.

### Libraries Used
* **IPython Notebook**: For interactive coding.
* **scikit-learn**: For machine learning models.
* **NumPy** and **SciPy**: For numerical operations.
* **Pandas**: For data manipulation.
* **Matplotlib** and **Seaborn**: For data visualization.
