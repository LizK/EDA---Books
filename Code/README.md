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
This are the steps I undertook with the datasets
1. Fixed Author name to make it consistent 
2. It turns out that both ISBN numbers are unique. The ISBN number is unique to the edition and publisher of the book while ISBN13 is the the new format implemented in 2007.
3. I thought of dropping the columns "BookID", "isbn" and "isbn13" but the code df.drop(['bookID','isbn','isbn13'],axis = 1,inplace=True) continued to output an error. Still trying to work it out....
3. Fixed number of pages columns title
4. A number of books do not have total number of pages stated. Replaced all the zero values with average total page of all books.
5.There are no duplicate in the dataset


## EDA Process
Findings
