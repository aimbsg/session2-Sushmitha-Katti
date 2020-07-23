# Session 2- Object Mutability and Interning

## Code Structure 
* ### Classes
    * **Something**
        * *Something* is a class which inherits object class.
        * __init__ method initialises the variable 'something_new' to 'None'
        * __repr__ method returns 'Something' as a string. It is the representation of the Class.


    * **SomethingNew**
        * *SomethingNew* is a class which inherits object class.
        * __init__ method takes i preferably of type integer and something preferably of type 'Something' class instance. It initialises the variable i to argument i and  something to argument something
        * __repr__ method returns 'Something New' as a string. It is the representation of the Class.

* ### Functions
    * **add_something** : This function takes 2 arguments list and int. Creates a instance of class 'Something' and assigns its variable 'something_new' to point to class 'SomethingNew' which takes arguments i and something. Basically it creates a cyclic reference.


    * **reserved_funtion** : This is not implemented yet. It is reserved for future use.


    * **clear_memory** : This method clears the memory, basically list. For this to function properly list_name.clear() is used first and manually called garbage collector to clear cyclic references.


    * **critical_function** : This function creates a large list named collection, with the help of 'add_something' function and then clears it using 'clear_memory' function


    * **compare_strings_old** : This function compares the equality of two strings of given n times and check the membership of a letter in a string as well. But this is not a optimised method since it is letter to letter comparision and while cheching memberhip list(char_list) is used, this takes lot of find the element.


    * **compare_strings_new**: This function does same task as above method. But optimal solution for string comparision and membership testing. To solve this problem interning was used. First both the strings are manually interned and 'is' operater is used for comparision. Since it uses address for comparing. So it will be faster. 
    For membership test first string is converted to set(char_set) and then checked, since set takes 0(1) time to search a element. 


## Test Cases

*  **test_clear_memory** :  this test is used to check whether memory is cleared properly or not and if the cyclic references are released or not.


*  **test_memory_actually_increeded** :  This test will check whether we are actually increase the memory during running the function f

*  **test_performence** : This test check the performance of string comparison methods. 'compare_strings_new' function should be atlest 10 times speeder that 'compare_strings_old'.

*  **test_readme_exists** :  This test checks whether Readme file exists or not.
*  **test_readme_contents** : This test checks whether there are more words or not. There should be atleast 500 words.


*  **test_readme_proper_description** : This checks whether readme is properly documented or not. It checks some of the keywords('Something, clear_memory, sleep, critical_function etc....) are present or not.


*  **test_readme_file_for_formatting** : This checks whether readme is we well formated with headings or not. It checks for the number of '#'. It should be more than 10.


*  **test_class_repr** : It checks whether class has good representation or not and the word 'object at' should not be present in that.


*  **test_fourspace** : Checks whether indented spaces are multiple of four or not. 


* **test_function_name_had_cap_letter** : Checks whether any funtion has capital letter or not.
