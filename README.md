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
   ![heatmap](https://github.com/Ittismita/Book-Recommender/blob/main/images/heatmap.png)

   From the heatmap it was observed that:
   1. "subtitle" column had the most missing values and were mostly random.
   2. Same was the case for the columns : categories, thumbnail, description.
   3. While observations in the columns - average_rating, num_pages, ratings_count - were missing with a pttern i.e. observation missing from one of these columns were also missing from the other two columns. This could indicate these columns were part of some other dataset and were hence merged in this larger dataset, hence a space for bias.

- For our NLP task what we need is the column : description. So we find correlation of this column with the above mentioned columns with missing entries - average_rating, num_pages, and a newly engineered column called age(using the column "year" from the dataset). This was done to highlight any bias if present like if those books which were young had missing entries or those books which were rated the most had missing entries.

- But from the corr matrix it was found out that no such relation had existed between these columns. After this the number of rows that had missing entries were found out to be 303(roughly 4.5% of the entire data), so were removed entirely.

- 
   

    
   

