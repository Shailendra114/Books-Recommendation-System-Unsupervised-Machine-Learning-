# Books-Recommendation-System-Unsupervised-Machine-Learning-
The main aim of this project is to built a good recommender system (RS) for books.![image](https://user-images.githubusercontent.com/88799249/154325914-620e6434-edc3-4ace-b6a1-22d3408cd07a.png)
# Objective:

![image](https://user-images.githubusercontent.com/88799249/155769464-4ae168f7-90b3-402f-bfad-9a8fe1cea43d.png)

Recommender systems have become a part of daily life for users of Amazon and Netflix and even social media. While some sites might use these systems to improve the customer experience (if you liked movie A, you might like movie B) or increase sales (customers who bought product C also bought product D), others are focused on customized advertising and suggestive marketing. As a book lover and former book store manager, I have always wondered where I can find good book recommendations that are both personalized to my interests and also capable of introducing me to new authors and genres. The purpose of this project is to create just such a recommender system (RS).
# Dataset link�
The dataset link can be downloaded from the following link---![image](https://user-images.githubusercontent.com/88799249/155766744-518f69c1-4ef6-490f-82a7-4cafe73fa8ce.png)

https://drive.google.com/drive/u/0/folders/1LQZRVw0qnoAoSsIa3vgHMX2nD0oj1fel
# Data Cleaning and Pre-Processing:-
![image](https://user-images.githubusercontent.com/88799249/155766150-2821ace4-030c-4c2c-9dab-dd943ba4e23c.png)


The dataset consists of three tables; Books, Users, and Ratings. Data from all three tables are cleaned and preprocessed separately as defined below briefly:

For Books Table:


![image](https://user-images.githubusercontent.com/88799249/155894733-7ff5900c-d369-4029-b102-94afff54d390.png)


* Drop all three Image URL features.
* Check for the number of null values in each column. There comes only 3 null values in the table. Replace these three empty cells with ‘Other’.
* Check for the unique years of publications. Two values in the year column are publishers. Also, for three tuples name of the author of the book was merged with the title of the book. Manually set the values for these three above obtained tuples for each of their features using the ISBN of the book.
* Convert the type of the years of publications feature to the integer.
* By keeping the range of valid years as less than 2022 and not 0, replace all invalid years with the mode of the publications that is 2002.
* Upper-casing all the alphabets present in the ISBN column and removal of duplicate rows from the table.


For Users Table:


 ![image](https://user-images.githubusercontent.com/88799249/155894836-9167ebea-4cec-43d7-ad92-689ee90227aa.png)


* Check for null values in the table. The Age column has more than 1 lakh null values.
* Check for unique values present in the Age column. There are many invalid ages present like 0 or 244.
* By keeping the valid age range of readers as 10 to 80 replace null values and invalid ages in the Age column with the mean of valid ages.
* The location column has 3 values city, state, and country. These are split into 3 different columns named; City, State, and Country respectively. In the case of null value, ‘other’ has been assigned as the entity value.
* Removal of duplicate entries from the table.


For Ratings Table:

![image](https://user-images.githubusercontent.com/88799249/155894867-656a879c-9d55-46b5-9650-2d23097aadd7.png)


* Check for null values in the table.
* Check for Rating column and User-ID column to be an integer.
* Removal of punctuation from ISBN column values and if that resulting ISBN is available in the book dataset only then considering else drop that entity.
* Upper-casing all the alphabets present in the ISBN column.
* Removal of duplicate entries from the table.

#  Algorithms Implemented:- 
The different algorithms that we used in this project are as follows-

 ![image](https://user-images.githubusercontent.com/88799249/156038176-6dd56841-4a97-426d-982a-bb1b53f316ef.png)


* Collaborative Filtering Recommendation

Collaborative Filtering Recommendation System works by considering user ratings and finds cosine similarities in ratings by several users to recommend books. To implement this, we took only those books' data that have at least 50 ratings in all.

# Tools Used:
The different tools that we have used in this project are as follows--

![image](https://user-images.githubusercontent.com/88799249/155894943-6c80d776-5281-4cd3-a3b0-1f985608cf4b.png)

1. Python
2. Pandas
3. Numpy
4. Seaborn
5. Plotly
5. Matplotlib
6. Sklearn
7. Flask
8. Pickle
9. HTML
10. Heroku
# Deployment:-

![image](https://github.com/KasumiL5x/book-recommendation-system/blob/master/screenshots/hhgttg.gif?raw=true)

# Conclusions:-
 ![image](https://user-images.githubusercontent.com/88799249/157096139-bf2dafe9-4dde-4d6b-9632-8c76a6e8c6a5.png)

*  In EDA, the Top-10 most rated books were essentially novels. Books like The Lovely Bone and The Secret Life of Bees were very well perceived.
*  Majority of the readers were of the age bracket 20–35 and most of them came from North American and European countries namely USA, Canada, UK, Germany and Spain.
*  If we look at the ratings distribution, most of the books have high ratings with maximum books being rated 8. Ratings below 5 are few in number.
*  Author with the most books was Agatha Christie, William Shakespeare and Stephen King.
*  For modelling, it was observed that for model based collaborative filtering SVD technique worked way better than NMF with lower Mean Absolute Error (MAE) .
*  Amongst the memory based approach, item-item CF performed better than user-user CF because of lower computation requirements .

# CHALLENGES:-
 ![image](https://user-images.githubusercontent.com/88799249/157095932-7a9983ee-dd0e-41ee-a958-65f8b1bbca39.png)


* Handling of sparsity was a major challenge as well since the user interactions were not present for the majority of the books.
* Understanding the metric for evaluation was a challenge as well.
* Since the data consisted of text data, data cleaning was a major challenge in features like Location etc..
* Decision making on missing value imputations and outlier treatment was quite challenging as well.

# FUTURE SCOPE:-
![image](https://user-images.githubusercontent.com/88799249/157096691-83a727b5-981a-4f18-8443-96b250e11a20.png)

* Given more information regarding the books dataset, namely features like Genre, Description etc., we could implement a content-filtering based recommendation system and compare the results with the existing collaborative-filtering based system.
* We would like to explore various clustering approaches for clustering the users based on Age, Location etc., and then implement voting algorithms to recommend items to the user depending on the cluster into which it belongs.









