# Python

### 1. How Python uses Indentation to control Flow

Python uses a different principle. Python programs get structured through indentation, i.e. code blocks are defined by their indentation. In the case of Python it's a language requirement not a matter of style.

While the concepts of function definitions, loops, and conditional statements are shared across the majority of modern programming languages, the languages often differ in their syntax for delimiting the _bodies_ of these constructs. For example, where C++ uses “curly braces” as delimiters. 

Python  **uses whitespace (i.e. indentation) to delimit scope**:
```python
# example showing that Python uses whitespace to delimit scope
x = 1
if x > 10:
    # we are inside the if-block; this line starts with four blank spaces
    x = x + 1
# we are outside of the if-block; there are no leading whitespace characters
x = x + 3
```

Python’s syntax is quite flexible in terms of what it defines as a whitespace delimiter. Its rules are that:

-   One or more whitespace characters (spaces or tabs) is sufficient to serve as indentation.
-   A given indented block must use a uniform level of indentation. E.g. if the first line of an indented block has two leading spaces, all subsequent lines in that block must lead with exactly two white spaces.

While Python’s syntax is relatively forgiving, I am not: the  [standard style](https://www.python.org/dev/peps/pep-0008/#indentation)  for indenting in Python is to  **use four space characters**  for each level of indentation. It is strongly advised that you adhere to this standard. Most IDEs and consoles (including Jupyter notebooks) will automatically add a four-space indentation for you when you enter into the body of one of the aforementioned constructs.

### 2. Don't Repeat Yourself

**Don't repeat yourself** (**DRY**, or sometimes **do not repeat yourself**) is a principle of "Software development process"  aimed at reducing repetition of software patterns, replacing it with abstractions or using "Data normalization" to avoid redundancy.

The DRY principle is stated as "Every piece of knowledge must have a single, unambiguous, authoritative representation within a system". The principle has been formulated by Andy Hunt Dave Thomas in their book  The Pragmatic Programmer. They apply it quite broadly to include "Database schema", "Test plan", the "Software build" system, even "Software documentation". 

When the DRY principle is applied successfully, a modification of any single element of a system does not require a change in other logically unrelated elements. Additionally, elements that are logically related all change predictably and uniformly, and are thus kept in Synchronization. 

**This code sample from the lesson illustrates how to apply DRY:**
```python
name = 'Mahdi'
people_i_like = ['Mahdi', 'John', 'Linda']
if name in people_i_like:
    print 'yay!'
```
    
### 3. Design Patterns from Gang of Four

Patterns can be divided into three different categories depending on their level of abstraction and implementation language independency: architectural patterns, design patterns and idioms. Design patterns are described in what is known as the GANG  OF  FOUR  book (GOF for short). The overall architecture of the system and related design decisions can be explained by giving a set of patterns used. While new patterns do emerge the GOF still remains as the definite reference on design patterns. For this reason it is important to introduce these patterns, the notions and the theory behind them and their applicability to Python community.

GOF is divided into three parts and each part describes the patterns related to the theme of the part. The themes describe the purpose of the patterns. Creational patterns address object instantiation issues. Structural patterns concentrate on object composition and their relations in the runtime object structures. Whereas the structural patterns describe the layout of the object system, the behavioral patterns focus on the internal dynamics and object interaction in the system.

Design patterns are a common way of solving well known problems. Two main principles are in the bases of the design patterns defined by the GOF:

	1. Program to an interface not an implementation.
	2. Favor object composition over inheritance.

- ### Behavioral Patterns

	Behavioural Patterns involve communication between objects, how objects interact and fulfil a given task. According to GOF principles, there are a total of 11 behavioral patterns in Python: _Chain of responsibility, Command, Interpreter, Iterator, Mediator, Memento, Observer, State, Strategy, Template, Visitor._

- ### Structural Patterns
	This may very well be the most famous Python design pattern. It includes _FACADE, ADAPTER, DECORATOR_

- ### Creational Patterns
	Creational patterns are not commonly used in Python. Why? Because of the dynamic nature of the language.

**You can find more details explanation of Design pattern in Python [here](https://www.toptal.com/python/python-design-patterns).

### 4. Class

Python is an _“object-oriented programming language”_. This means that almost all the code is implemented using a special construct called classes. Programmers use classes to keep related things together. This is done using the keyword _“class”_, which is a grouping of object-oriented constructs. A Class is like an object constructor, or a "blueprint" for creating objects.

Classes provide a means of bundling data and functionality together. Creating a new class creates a new _type_ of object, allowing new _instances_ of that type to be made. Each class instance can have attributes attached to it for maintaining its state. Class instances can also have methods (defined by its class) for modifying its state.

- ### What is a class?
	
	A class is a code template for creating objects. Objects have member variables and have behaviour associated with them. In python a class is created by the keyword  `class`.

- ### How to create a class
	
	The simplest class can be created using the class keyword. For example, let's create a simple, empty class with no functionalities.
	```python
		>>> class Snake:
		...     pass
		... 
		>>> snake = Snake()
		>>> print(snake)
		<__main__.Snake object at 0x7f315c573550>
	```
- ### Attributes and Methods in class:

	A class by itself is of no use unless there is some functionality associated with it. Functionalities are defined by setting attributes, which act as containers for data and functions related to those attributes. Those functions are called methods.
	
	- ### Attributes:

	You can define the following class with the name Snake. This class will have an attribute  `name`.
	```python
		>>> class Snake:
		...     name = "python" # set an attribute `name` of the class
		...
	```
	- ### Methods

	Once there are attributes that “belong” to the class, you can define functions that will access the class attribute. These functions are called methods. When you define methods, you will need to always provide the first argument to the method with a self keyword.

	For example, you can define a class  `Snake`, which has one attribute  `name`  and one method  `change_name`. The method change name will take in an argument  `new_name`  along with the keyword  `self`.

	```python
		>>> class Snake:
		...     name = "python"
		...     
		...     def change_name(self, new_name): # note that the first argument is self
		...         self.name = new_name # access the class attribute with the self keyword
		...
	```

### 5. Object

An object is created using the constructor of the class. This object will then be called the  `instance`  of the class. In Python we create instances in the following manner

```python
	Instance = class(arguments)
```

We can instantiate class  `Snake`  defined above in class description with a variable  `snake`  and then change the name with the method  `change_name`.

```python
	>>> # instantiate the class
	>>> snake = Snake()

	>>> # print the current object name 
	>>> print(snake.name)
	python

	>>> # change the name using the change_name method
	>>> snake.change_name("anaconda")
	>>> print(snake.name)
	anaconda
```

- ### Instance attributes in python and the init method

	You can also provide the values for the attributes at runtime. This is done by defining the attributes inside the init method. The following example illustrates this.

	```python
		class Snake:

		    def __init__(self, name):
		        self.name = name

		    def change_name(self, new_name):
		        self.name = new_name
	```

	Now we can directly define separate attribute values for separate objects. For example,

	```python
		>>> # two variables are instantiated
		>>> python = Snake("python")
		>>> anaconda = Snake("anaconda")

		>>> # print the names of the two variables
		>>> print(python.name)
		python
		>>> print(anaconda.name)
		anaconda
	```

### 9. Exception
An exception is an error that happens during execution of a program. When that
error occurs, python generate an exception that can be handled, which avoids your program to crash. A Python program terminates as soon as it encounters an error.
- Exceptions are convenient in many ways for handling errors and special conditions in a program. When you think that you have a code which can produce an error then you can use exception handling. 
- You can raise an exception in your own program by using the raise exception statement. Raising an exception breaks current code execution and returns the exception back until it is handled.

**Exception Errors**
Below are some common *exception errors* used in python:

| Error | Explanation |
| ------ | ------ |
| IOError | If the file cannot be opened |
| ImportError | If python cannot find the module |
| ValueError | Raised when a built-in operation or function receives an argument that has the right type but an inappropriate value |
| KeyboardInterrupt |Raised when the user hits the interrupt key (normally Control-C or Delete) |
| EOFError | Raised when one of the built-in functions (input() or raw_input()) hits an end-of-file condition (EOF) without reading any data |

For more information on exception, visit [https://www.pythonforbeginners.com/error-handling/exception-handling-in-python](https://www.pythonforbeginners.com/error-handling/exception-handling-in-python).

### 10. Unit Test
Unit Testing in Python is done to identify bugs early in the development stage of the application when bugs are less recurrent and less expensive to fix. A unit test is a scripted code level test designed in Python to verify a small "unit" of functionality. Unit test is an object oriented framework based around test fixtures.

The standard workflow for Unit Test is as follow:
- You define your own class derived from unittest.TestCase.
- Then you fill it with functions that start with ‘`test_`’.
- You run the tests by placing `unittest.main()` in your file, usually at the bottom.

Here's a test **example** code to test ‘multiply’ function.

```python
import unittest
from unnecessary_math import multiply
 
class TestUM(unittest.TestCase):
 
    def setUp(self):
        pass
 
    def test_numbers_3_4(self):
        self.assertEqual( multiply(3,4), 12)
 
    def test_strings_a_3(self):
        self.assertEqual( multiply('a',3), 'aaa')
 
if __name__ == '__main__':
    unittest.main()
```

For more information on Unit Test, visit [https://www.guru99.com/python-unit-testing-guide.html](https://www.guru99.com/python-unit-testing-guide.html).

### 11. Constructor
Constructors are generally used for instantiating an object. The task of constructors is to initialize(assign values) to the data members of the class when an object of class is created. In Python the `__init__()` method is called the constructor and is always called when an object is created.

There are two types of constructors:
- **Default constructor**: The default constructor is simple constructor which doesn’t accept any arguments. It’s definition has only one argument which is a reference to the instance being constructed.
- **Parameterized constructor**: Constructor with parameters is known as parameterized constructor. The parameterized constructor take its first argument as a reference to the instance being constructed known as self and the rest of the arguments are provided by the programmer.

**Syntax of constructor declaration**
```
def __init__(self):
# body of the constructor
```

For more information on constructor, visit [https://www.geeksforgeeks.org/constructors-in-python/](https://www.geeksforgeeks.org/constructors-in-python/).

### 12. Factory
Factory is an ambiguous term that stands for a function, method or class that supposed to be producing something. Most commonly, factories produce objects. But they may also produce files, records in databases, etc.

For instance, any of these things may be casually referenced as a *“factory”*:

- a function or method that creates a program’s GUI;
- a class that creates users;
- static method that calls a class constructor in a certain way;
- one of the creational design patterns.

Here's an example of factory method:

```
class UserFactory {
    public static function create($type) {
        switch ($type) {
            case 'user': return new User();
            case 'customer': return new Customer();
            case 'admin': return new Admin();
            default:
                throw new Exception('Wrong user type passed.');
        }
    }
}
```

For more information on factory, visit [https://refactoring.guru/design-patterns/factory-comparison](https://refactoring.guru/design-patterns/factory-comparison).

### 13. Decorator
Decorators are very powerful and useful tool in Python since it allows programmers to modify the behavior of function or class. Decorators allow us to wrap another function in order to extend the behavior of wrapped function, without permanently modifying it.

In Decorators, functions are taken as the argument into another function and then called inside the wrapper function.

**Syntax for Decorator**:
```
def hello_decorator(): 
    print("Gfg") 
      
hello_decorator = gfg_decorator(hello_decorator)
```

For more information on Decorator, visit [https://www.geeksforgeeks.org/decorators-in-python/](https://www.geeksforgeeks.org/decorators-in-python/).

### 14. Extend Class
Extend class is also known as inheritance. It is the mechanism of deriving new classes from existing ones. By doing this we get a hierarchy of classes. In most class-based object-oriented languages, an object created through inheritance (a *"child object"*) acquires all, - though there are exceptions in some programming languages, - of the properties and behaviors of the parent object.

**Syntax for Extend Class**:
```
class DerivedClassName(BaseClassName):
    pass
```

For more information on extend class, visit [https://www.python-course.eu/python3_inheritance.php](https://www.python-course.eu/python3_inheritance.php).

### 15. CSV Files
Data in the form of tables is also called CSV (comma separated values) - literally "comma-separated values." This is a text format intended for the presentation of tabular data. Each line of the file is one line of the table. The values of individual columns are separated by a separator symbol - a comma `(,)`, a semicolon `(;)` or another symbol. CSV can be easily read and processed by Python.

Python provides a CSV module to handle CSV files. To read/write data, you need to loop through rows of the CSV. You need to use the split method to get data from specified columns.

To read data from CSV files, you must use the reader function to generate a reader object.

**CSV Reader Module Example**
```
import necessary modules
import csv
with open('X:\data.csv','rt')as f:
  data = csv.reader(f)
  for row in data:
        print(row)
```

For more information on CSV Files, visit [https://www.guru99.com/python-csv.html](https://www.guru99.com/python-csv.html).

### 16. Reading Files
Python provides inbuilt functions for reading files. There are two types of files that can be handled in python, normal text files and binary files.
- **Text files**: In this type of file, Each line of text is terminated with a special character called EOL (End of Line), which is the new line character (‘\n’) in python by default.
- **Binary files**: In this type of file, there is no terminator for a line and the data is stored after converting it into machine understandable binary language.

There are three ways to read data from a text file.
1. `read()` : Returns the read bytes in form of a string. Reads n bytes, if no n specified, reads the entire file.
    ```
    File_object.read([n])
    ```
2. `readline()` : Reads a line of the file and returns in form of a string.For specified n, reads at most n bytes. However, does not reads more than one line, even if n exceeds the length of the line.
    ```
    File_object.readline([n])
    ```
3. `readlines()` : Reads all the lines and return them as each line a string element in a list.
    ```
    File_object.readlines()
    ```
    
For more information on reading files, visit [https://www.geeksforgeeks.org/reading-writing-text-files-python/](https://www.geeksforgeeks.org/reading-writing-text-files-python/).
