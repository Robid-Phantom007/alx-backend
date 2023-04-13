# 0x00. Pagination

## General :house:
* How to paginate a dataset with simple page and page_size parameters
* How to paginate a dataset with hypermedia metadata
* How to paginate in a deletion-resilient manner

## Requirements :page_with_curl:
* All your files will be interpreted/compiled on Ubuntu 18.04 LTS using python3 (version 3.7)
* All your files should end with a new line
* The first line of all your files should be exactly #!/usr/bin/env python3
* A README.md file, at the root of the folder of the project, is mandatory
* Your code should use the pycodestyle style (version 2.5.*)
* The length of your files will be tested using wc
* All your modules should have a documentation (python3 -c 'print(__import__("my_module").__doc__)')
* All your functions should have a documentation (python3 -c 'print(__import__("my_module").my_function.__doc__)'
* A documentation is not a simple word, it’s a real sentence explaining what’s the purpose of the module, class or method (the length of it will be verified)
* All your functions and coroutines must be type-annotated.

## Tasks and Files :heavy_check_mark:
* 0. Simple helper function
	* Write a function named index_range that takes two integer arguments page and page_size.
The function should return a tuple of size two containing a start index and an end index corresponding to the range of indexes to return in a list for those particular pagination parameters.
Page numbers are 1-indexed, i.e. the first page is page 1.

* 1. Simple pagination
	* Copy index_range from the previous task and the following class into your code

* 2. Hypermedia pagination
	* Replicate code from the previous task.
Implement a get_hyper method that takes the same arguments (and defaults) as get_page and returns a dictionary containing the following key-value pairs:
	* page_size: the length of the returned dataset page
	* page: the current page number
	* data: the dataset page (equivalent to return from previous task)
	* next_page: number of the next page, None if no next page
	* nprev_page: number of the previous page, None if no previous page
	* total_pages: the total number of pages in the dataset as an integer

* 3. Deletion-resilient hypermedia pagination
	* The goal here is that if between two queries, certain rows are removed from the dataset, the user does not miss items from dataset when changing page.
