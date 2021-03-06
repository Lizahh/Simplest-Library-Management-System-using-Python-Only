# Simplest-Library-Management-System-using-Python-Only

This is a simple Library-Management-System designed purely in Python. It is written using python 3.10 (which is latest version at the time of making this repository) and it can work for any Python version 3.x. The system provides following 8 main functionalities:
* Creating a new book
* Saving books locally
* Loading books from the disk
* Issuing book
* Returning a book
* Updated a book
* Showing all books
* Showing specific book

## 1-Creating a new book:
This module asks the user to create new book by entering its information about book ID,book name, book description,book ISBN,book's page count, if it is issued or not, and its year of publication. The book is displayed immediately in the form of dictionary. This module is based on the class 'Book' which is written in 'book.py' module. 

![Create a book](https://user-images.githubusercontent.com/44564025/173081429-4af886d1-2524-4001-aac5-26f521155c06.png)

## 2-Saving books locally:
The next step is to save the book. It leads to saving book in 'books.dat' file locally on machine. The gathered data from the user in first module (creating the book) is sent to the Book class which converts that information in dictinary. The save_books function accesses that dictionary, dumps that dictionary using json function 'json.dumps()'. Later, this json object is stored in the books.dat data file.

![Saving the book](https://user-images.githubusercontent.com/44564025/173081512-27134982-7743-4db3-b143-2bebe42cc298.png)

## 3-Loading books from the disk:
It will load the books from the disk. It loads the json data from books.dat, convert them to dictionary using class Book, save it to the list books and return it at the calling place. This function will load all the books from the disk. Once you save the books, next time you use the application, you are just supposed to load all the books using this function.

![Loading all books](https://user-images.githubusercontent.com/44564025/173081549-da895b27-117d-457b-977e-41fed5576e88.png)

## 4-Issuing book:
This function serves the basic purpose of library management system. If a student/user comes to issue a book, he will be asked to input the ID of the book. That ID will be searched thoroughly in the books.dat file using find_book function. Then, the book will be issued to the student and the 'issue status' of book will be replaced from False to True in the books.dat file, immediately. Later a message is displayed that the book is issued, successfully.
* Nota bene: You must need to call the save book function after issuing book, to update the information in data file.

![Issuing the Book](https://user-images.githubusercontent.com/44564025/173081598-13b98a7b-9b19-450a-b21b-420c72ffd37f.png)

## 5-Returning a book
This function works almost the same like issuing book function. It asks the student/user come to return a book, it checks if the book is issued from this library by confirming if its issued_status is True. If so, then the issued_status is set to False and a message is displayed that the book is returned, successfully.
* Nota bene: You must need to call the save book function after getting the returned book, to update the information in data file.

![Returning the book](https://user-images.githubusercontent.com/44564025/173081666-fc82026d-9ceb-428d-81b3-add9ec490822.png)

## 6-Updated a book
This function is used if the user want to update the information about a book in the data file. It asks the user to enter the ID of the book and checks if the book exists in the library. If yes, then it call the create book function to re-enter the information about the book and then update it.

![Updating a book](https://user-images.githubusercontent.com/44564025/173082022-95e15c2d-dd88-4ca2-92f3-3780944f43ca.png)

## 7-Showing all books
This function is solely based on showing all books, of which information is available in the data file.

![Showing all books](https://user-images.githubusercontent.com/44564025/173082071-c46ce04b-6750-4281-ba04-a254b2095460.png)

## 8-Showing specific book
It asks the user to enter the ID of the book, of which information they want to see. It check if the book exist using find_book function. It it does, then it shows the information of that book, respectively.

![Showing Specific book](https://user-images.githubusercontent.com/44564025/173082147-15307776-27e6-49da-8f94-e3175786072d.png)


