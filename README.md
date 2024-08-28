1.Project Overview

This project is a straightforward mechanism for recommending films based on how similar their genres are. It employs cosine similarity on the genre and type data to determine how similar two films are by utilising a cleaned version of the Netflix Shows dataset.

2.Prerequisites

Make sure you have the following installed:

a.Python 

b.Pandas

c.NumPy

d.Scikit-learn

e.Matplotlib

f.Seaborn

3.Dataset

A Netflix movie dataset is used in the study. Make sure the dataset file is in the project directory, or change the code to point to the right location.


4.How It Works

Following is the implementation of the recommendation system:

a.Preprocessing of Data:

A pandas DataFrame has the dataset loaded into it.Combining the listed_in and type columns yields a new feature called feature_summary. The genre and type information for every show is compiled in this section.

b.Vectorisation of text:
With CountVectorizer, the feature_summary column is tokenised and vectorised. To ensure that each genre or category is handled as a distinct token, the text is divided on commas (,) using a bespoke tokeniser.
A sparse matrix of token counts is the end product, with each row representing a show and each column representing a genre or category.

c.Computing Cosine Similarity:

The resemblance between various shows is determined by computing the cosine similarity between the rows of the feature matrix. This yields a similarity matrix, in which the similarity between shows I and J is represented by each entry (i, j).

d.Logic:

The method searches the cosine similarity matrix for the row that corresponds to a given movie title in order to determine which shows are the most comparable.Using cosine similarity scores, the method returns the top n most comparable movies.

e.Visualisation:

A scatter plot is used to display the suggested movies, with similarity scores on the y-axis and movie names on the x-axis.

5.Usage

a.Input: A movie title input box is displayed to the user.
b.Output: A scatter plot with the list of suggested films that are comparable to the input movie is produced by the system.

6.Conclusion

This project shows how to use text vectorisation and cosine similarity to create a simple recommendation system. It offers a simple, yet powerful, method for making movie recommendations based on similarity in genre.





