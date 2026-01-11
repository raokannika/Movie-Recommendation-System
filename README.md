# 🎬 Movie Recommendation System

## Project Overview
This project is a **Content-Based Movie Recommendation System** that suggests movies similar to a user-selected movie.
The recommendation is based on **movie content** such as genres, keywords, and descriptions rather than user ratings.

The system uses **TF-IDF Vectorization** to convert text data into numerical form and **Cosine Similarity** to find movies that are most similar to each other.

This type of recommendation system is commonly used by platforms like Netflix and Amazon Prime Video.

---

## Dataset Description
The dataset contains information about movies, including:

- Movie Title  
- Genre(s)  
- Overview / Description  
- Keywords / Tags  

Only relevant columns required for generating recommendations are used.
Text-based features are combined and processed to represent each movie uniquely.

The dataset helps the system understand *what a movie is about* and recommend similar movies based on content similarity.

---

## Project Workflow

1. **Data Loading**
   - Load the movie dataset.
   - Select relevant columns required for recommendations.

2. **Data Preprocessing**
   - Handle missing values.
   - Clean and combine important text fields into a single feature.

3. **Feature Extraction**
   - Convert text data into numerical vectors using **TF-IDF Vectorizer**.

4. **Similarity Calculation**
   - Compute similarity between movies using **Cosine Similarity**.

5. **User Input**
   - User provides a movie name.

6. **Recommendation Generation**
   - The system finds movies with the highest similarity scores.
   - Top similar movies are recommended.

7. **Output**
   - A list of recommended movies is displayed to the user.

---

## TF-IDF Vectorizer

**TF-IDF** stands for **Term Frequency – Inverse Document Frequency**.

### Why TF-IDF is used?
Not all words in a movie description are equally important. Common words like *“the”, “is”, “and”* appear everywhere and do not help differentiate movies.

TF-IDF gives:
- Higher weight to **important and unique words**
- Lower weight to **common and less meaningful words**

### How it works:
- **Term Frequency (TF):** Measures how often a word appears in a movie description.
- **Inverse Document Frequency (IDF):** Reduces the importance of words that appear in many movies.

After applying TF-IDF:
- Each movie is converted into a **numerical vector**
- These vectors represent the movie’s content in mathematical form

This makes it possible to compare movies using similarity measures.

---

##  Cosine Similarity

**Cosine Similarity** measures the **angle between two vectors** instead of their distance.

### Why Cosine Similarity?
- Text data creates **high-dimensional vectors**
- Magnitude (length) is less important than **direction**
- Cosine similarity focuses on how similar the content is

### Cosine Similarity Values:
- **1** → Movies are very similar  
- **0** → Movies are not similar  
- **-1** → Completely opposite (rare in text data)

### In this project:
- Each movie vector is compared with all other movie vectors
- Movies with the **highest cosine similarity scores** are recommended

Cosine similarity works very well for **text-based recommendation systems**.

---

## 🛠️ Technologies Used

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Jupyter Notebook  

---

## How to Run the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/raokannika/movie-recommendation-system.git
````

2. Install required libraries:

   ```bash
   pip install pandas numpy scikit-learn
   ```

3. Open the Jupyter Notebook:

   ```bash
   jupyter notebook movie-recommemdation-system.ipynb
   ```

4. Run all cells and provide a movie name as input.

---

## Example

**Input:**

```
Avatar
```

**Output:**

```
Recommended Movies:
- Guardians of the Galaxy
- John Carter
- Star Wars
- Interstellar
```

---

## Conclusion

This project demonstrates how machine learning techniques like **TF-IDF Vectorization** and **Cosine Similarity** can be used to build an effective movie recommendation system.
It is beginner-friendly and helps understand real-world recommender systems.

---
