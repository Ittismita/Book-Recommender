# Semantic Book Recommender
A guided project to explore the application of LLMs and use some cutting edge technology like Python, Gradio and LangChain.
This project helped apply what learnt theoretically in LLMs and give a kickstart to build more such applications.

Dataset : https://www.kaggle.com/datasets/dylanjcastillo/7k-books-with-metadata

1. Data Exploration - EDA
   
   - Rows - 6810
   - Columns - 12

   ``` data.info() ```
   
   - Numeric columns - 5 - isbn13, published_year, average_rating, num_pages, ratings_count
   - Categorical columns - 7 - title, subtitle, authors, categories, thumbnail, description, isbn10

   With missing values found in columns: 
   1. subtitle(65% missing values)
   2. thumbnail(~5% missing values)
   3. description(~4% missing values)
   4. categories(1.45% missing values)
   5. authors(1.05% missing values)
   6. average_rating, num_pages, ratings_count (0.6% missing values)
   7. published_year(0.088% missing values)
  
   Using heatmaps, showed the pattern in missing values:
   

    
   

