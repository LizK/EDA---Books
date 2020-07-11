## Cleaning Process
![Data](https://storage.ning.com/topology/rest/1.0/file/get/2808308206?profile=original)
**Source:**https://storage.ning.com/topology/rest/1.0/file/get/2808308206?profile=original


### Initial Inspection

1. The Datasets contains 11123 rows and 12 columns.
2. Upon inspecting the columns in the dataset, there seems to be two ISBN number which are slightly different.
3. Author name is not consistent in the dataset
4. There are a total of 6639 authors in the dataset
5. Majority of the books are in the english language


### Initial Actions
This are the steps I undertook with the datasets:
1. Fixed Author name to make it consistent 
2. It turns out that both ISBN numbers are unique. The ISBN number is unique to the edition and publisher of the book while ISBN13 is the the new format implemented in 2007.
3. I thought of dropping the columns "BookID", "isbn" and "isbn13" but the code df.drop(['bookID','isbn','isbn13'],axis = 1,inplace=True) continued to output an error. Still trying to work it out....
3. Fixed number of pages columns title
4. A number of books do not have total number of pages stated. Replaced all the zero values with average total page of all books.
5. There are no duplicate in the dataset


## EDA Process
Findings

1. Book ratings based on language shows English books being highly rated but that is not surprising given that majority of the books are in that language.
2. The top highest rated books shows a liking to fiction.
3. Readers dont seem to shy away from high volume books.
4. The Lliad tops the list of most occuring books. It is interesting to note that oldies reoccured in the list, meaning oldies have not been forgotten.
5. The top twenty publishers
6. The number of books per author in the dataset
6. There is a positivr correlation between ratings and review counts.
7. Recommendation of top rated books with less than 200 pages
   - Animal Farm
   - Lord of the files
   - Of mice and Men
   - The Alchemist
   - Charlotte's Web
   - Charlie and Chocolate Factory
   - The Firm
   - The five people you meet in heaven
   - Coraline
   - Alice in Wonderland
   
8. Recommendation of top rated books with less than 1000 pages
   - Gone with the Wind
   - The Count of Monte Cristo
   - Altas  Shrugged
   - War and Peace
   - Don Quixote
   - The Shadow Rising
   - The Fiery Cross
   - Lord of Chaos
   - Lord of the Rings
   - Anne of Green Gables
   
### Future Work
The dataset was an overall good one although there are some factors that could help in having a great analysis. Some of the limitations and questions that I thought of:
1. How recent is the dataset: I was not able to determine the date when the data was acquired, the concern is if it old then the analysis does not potrait the current situation.
2. Should the reviews include mandatory data collection to ensure consistency of the data? For example:
   - The total number of pages in a book
   - The Author names to be chosen from a library to avoid spelling mistakes or interchanging first and last names.
3. I would like to see genre of books column included in the dataset. It would not only offer better analysis but book recommendations would be made easier as people prefer deferent genres.
4. The dataset does not include reviewers location. Might be interesting data to acquire for future predictions of say, sales but also an understanding of the people.
5. The dataset seems a bit bias as far as language is concerned. Could it be non-english book readers dont review the books they read? Maybe the website should be available in other languages? 