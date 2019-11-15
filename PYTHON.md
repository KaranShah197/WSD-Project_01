# Python

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