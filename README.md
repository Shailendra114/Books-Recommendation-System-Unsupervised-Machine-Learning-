# Books-Recommendation-System-Unsupervised-Machine-Learning-
The purpose of this project is to built  a recommender system (RS) for books.![image](https://user-images.githubusercontent.com/88799249/154325914-620e6434-edc3-4ace-b6a1-22d3408cd07a.png)
# Objective:

![image](https://user-images.githubusercontent.com/88799249/155769464-4ae168f7-90b3-402f-bfad-9a8fe1cea43d.png)

Recommender systems have become a part of daily life for users of Amazon and Netflix and even social media. While some sites might use these systems to improve the customer experience (if you liked movie A, you might like movie B) or increase sales (customers who bought product C also bought product D), others are focused on customized advertising and suggestive marketing. As a book lover and former book store manager, I have always wondered where I can find good book recommendations that are both personalized to my interests and also capable of introducing me to new authors and genres. The purpose of this project is to create just such a recommender system (RS).
# Dataset link�
![image](https://user-images.githubusercontent.com/88799249/155766744-518f69c1-4ef6-490f-82a7-4cafe73fa8ce.png)

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

![image](https://user-images.githubusercontent.com/88799249/155765751-59d2d5ad-2476-4755-8dc9-d20b10daa6dc.png)

* Collaborative Filtering Recommendation

Collaborative Filtering Recommendation System works by considering user ratings and finds cosine similarities in ratings by several users to recommend books. To implement this, we took only those books' data that have at least 50 ratings in all.

# Tools Used:
1. Python
2. Pandas
3. Numpy
4. Sklearn
5. Flask
7. Pickle
8. HTML
9. Heroku
# Deployment:-

![image](https://github.com/KasumiL5x/book-recommendation-system/blob/master/screenshots/hhgttg.gif?raw=true)
