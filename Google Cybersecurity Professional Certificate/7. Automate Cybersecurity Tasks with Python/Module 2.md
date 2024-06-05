# Write effective Python **code**
## Python functions in cybersecurity
### Functions in cybersecurity

- A **function** is a section of code that can be reused in a program.
- Functions are important in Python because they allow you to automate repetitive parts of your code.
- In cybersecurity, you will likely adopt some processes that you will often repeat.
- When working with security logs, you will often encounter tasks that need to be repeated.
    - Example: Finding malicious login activity based on failed login attempts across multiple logs.
- Define a function to take a log as its input and return all potentially malicious logins.
    - Easy to apply this function to different logs.

### Defining a function

- In Python, you'll work with built-in functions and user-defined functions.
    - **Built-in functions**: Functions that exist within Python and can be called directly (e.g., `print()`).
    - **User-defined functions**: Functions that programmers design for their specific needs.

#### Function header

- The function header tells Python that you are starting to define a function.
- Example: Define a function that displays an "investigate activity" message.
    ```python
    def display_investigation_message():
    ```
    - `def` keyword is placed before a function name to define a function.
    - Name of the function in this case: `display_investigation_message`.
    - Parentheses follow the name of the function and a colon (:) ends the function header.

**Pro tip**: When naming a function, give it a name that indicates what it does. This will make it easier to remember when calling it later.

#### Function body

- The body of the function is an indented block of code after the function header that defines what the function does.
- Indentation separates the definition of a function from the rest of the code.
- Add a body to the `display_investigation_message()` function:
    ```python
    def display_investigation_message():
        print("investigate activity")
    ```

### Calling a function

- After defining a function, you can use it as many times as needed in your code.
- Using a function after defining it is referred to as calling a function.
- To call a function, write its name followed by parentheses:
    ```python
    display_investigation_message()
    ```
- Example: Calling the `display_investigation_message()` function as part of a larger section of code:
    ```python
    def display_investigation_message():
        print("investigate activity")

    application_status = "potential concern"
    email_status = "okay"

    if application_status == "potential concern":
        print("application_log:")
        display_investigation_message()

    if email_status == "potential concern":
        print("email log:")
        display_investigation_message()
    ```
    - The `display_investigation_message()` function is used twice within the code.
    - It will print "investigate activity" messages about two different logs when the specified conditions evaluate to True.
    - Only the first conditional statement evaluates to True, so the message prints once.

- **Note:** Calling a function inside the body of its function definition can create an infinite loop.
    - Example of infinite loop:
        ```python
        def func1():
            func1()
        ```

### Key takeaways

- Python’s functions are important when writing code.
- To define your own functions, you need the two essential components of the function header and the function body.
- After defining a function, you can call it when needed.

---
## Functions and variables
### Working with variables in functions
#### Parameters

- **Parameter**: Object included in a function definition.
- Defined in the function header.
- Used within the function body.
- **Example:**
	```python
	def remaining_login_attempts(maximum_attempts, total_attempts):
	    print(maximum_attempts - total_attempts)
	```

#### Arguments

- **Argument**: Data brought into a function when it's called.
- Passed to the function when calling it.
- **Example:**
	```python
	remaining_login_attempts(3, 2)
	```

#### Return statements

- Used to return output from a function.
- Precedes the value or expression to be returned.
- **Example:**
	```python
	def remaining_login_attempts(maximum_attempts, total_attempts):
	    return maximum_attempts - total_attempts
	```

### Global and local variables

#### Global variables

- Available throughout the entire program.
- Defined outside of a function.
- Accessible from anywhere in the code.
- **Example:**
	```python
	device_id = "7ad2130bd"
	```

#### Local variables

- Defined within a function's scope.
- Accessible only within the function.
- Created and destroyed during function execution.
- **Example:**
	```python
	def greet_employee(name):
	    total_string = "Welcome" + name
	    return total_string
	```

#### Best practices for global and local variables

- Use distinct variable names to avoid conflicts.
- Minimize the use of global variables.
- Avoid combining global and local variables within functions.
- **Example:**
	```python
	username = "elarson"
	
	def identify_user():
	    print(username)
	
	identify_user()
	```

	```python
	username = "elarson"
	print("1:" + username)
	
	def greet():
	    username = "bmoreno"
	    print("2:" + username)
	
	greet()
	print("3:" + username)
	```

### Key takeaways

- Understand parameters, arguments, and return statements in functions.
- Differentiate between global and local variables.
- Follow best practices to maintain clean and efficient code.

---
## Work with built-in functions

- **Built-in function:**
	- A function that exists within Python and can be called directly.

### print()

- `print()`: Outputs specified object to the screen. Takes multiple arguments separated by commas.

  ```python
	month = "September"
	print("Investigate failed login attempts during", month, "if more than", 100)
	```

### type()

- `type()`: Returns the data type of its argument.
	```python
	print(type("This is a string"))
	```
- When passing functions like `type()` to `print()`, the output of the inner function is passed as an argument to the outer function.
	```python
	print(type("This is a string"))
	```

### max() and min()

- `max()`: Returns the largest numeric input.    
- `min()`: Returns the smallest numeric input.
	```python
	time_list = [12, 2, 32, 19, 57, 22, 14]
	print(min(time_list))
	print(max(time_list))
	```

### sorted()

- `sorted()`: Sorts the components of a list or any iterable in ascending order.
	```python
	time_list = [12, 2, 32, 19, 57, 22, 14]
	print(sorted(time_list))
	```

### Key takeaways

- Built-in functions are powerful tools in Python.
- `print()` outputs to the screen.
- `type()` returns data type.
- `min()` and `max()` find the smallest and largest values.
- `sorted()` sorts iterables.

### Resources for more information

- [The Python Standard Library documentation](https://docs.python.org/3/library/functions.html)

---
## Notes on Importing Modules and Libraries
### The Python Standard Library

- Extensive collection of Python code that comes packaged with Python
- Includes various modules for different tasks:
  - `re`: Searching for patterns in log files
  - `csv`: Working with .csv files
  - `glob` and `os`: Interacting with the command line
  - `time` and `datetime`: Working with timestamps
  - `statistics`: Calculating statistics related to numeric data

#### How to Import Modules
##### Importing an Entire Module

- Use the `import` keyword followed by the module name
- Example:
  ```python
	import statistics
	```

##### Importing Specific Functions

- Use the `from` keyword followed by the module name and function(s) to import
- Example:
	```python
	from statistics import mean, median
	```

### External Libraries

- Can be downloaded and incorporated into Python code
- Examples:
    - **Beautiful Soup (bs4)**: Parsing HTML files
    - **NumPy (numpy)**: Arrays and mathematical computations

#### Installing External Libraries

- Before use, libraries need to be installed
- Example for installing NumPy.
	```python
	pip install numpy
	```

#### Importing External Libraries

- Use the `import` keyword followed by the library name
- Example:
	```python
	import numpy
	```

### Key Takeaways

- Python Standard Library offers many modules for various tasks
- Syntax differs based on whether importing entire modules or specific functions
- External libraries can extend Python's functionality but require installation before use.

---
## Ensure proper syntax and readability in Python
### Comments

- **Comment:** A note programmers make about the intentions behind their code.

    - Single-line comments in Python begin with the `#` symbol. It's best practice to keep all lines under 79 characters, including comments.
    
        ```python
        # Print elements of 'computer_assets' list
        computer_assets = ["laptop1", "desktop20", "smartphone03"]
        
        for asset in computer_assets:
            print(asset)
        ```
    
    - Multi-line comments are used when a single comment exceeds 79 characters. They can be written using `#` over multiple lines or triple quotes `""" """`.
    
        ```python
        # remaining_login_attempts() function takes two integer parameters,
        # the maximum login attempts allowed and the total attempts made,
        # and it returns an integer representing remaining login attempts
        def remaining_login_attempts(maximum_attempts, total_attempts):
            return maximum_attempts - total_attempts
        ```

### Correct indentation

- **Indentation:** Space added at the beginning of a line of code.

    - In Python, indentation is crucial for code interpretation and readability. It's recommended to use four spaces for each level of indentation.

        ```python
        count = 0
        login_status = True
        
        while login_status == True:
            print("Try again.")
            count = count + 1
            if count == 4:
                login_status = False
        ```

### Maintaining correct syntax

- Syntax errors involve invalid usage of the Python language. Common errors include mistakes with data types or in the headers of conditional or iterative statements or function definitions.

#### Data types

- Correct syntax varies depending on data type:
    - Strings: Place string data in quotation marks.
    - Integers, floats, Booleans: No quotation marks.
    - Lists: Brackets for elements, commas for separation.

        ```python
        username = "bmoreno"
        login_attempts = 5
        percentage_successful = .8
        login_status = True
        username_list = ["bmoreno", "tshah"]
        ```

#### Colons in headers

- Headers of conditional, iterative statements, or function definitions must end with a colon.

    ```python
    def remaining_login_attempts(maximum_attempts, total_attempts):
        return maximum_attempts - total_attempts
    ```

### Key takeaways

- **PEP 8 style guide:** A resource that provides stylistic guidelines for programmers working in Python.
- **Style guide:** A manual that informs the writing, formatting, and design of documents.
- **Comment:** A note programmers make about the intention behind their code.
- **Indentation:** Space added at the beginning of a line of code.

- Follow PEP 8 for clean Python code.
- Use comments for clarity, following conventions for single or multi-line comments.
- Maintain correct indentation for readability.
- Ensure syntax correctness by observing data types and headers.

### Resources for more information

- [PEP 8 - Style Guide for Python Code](https://peps.python.org/pep-0008/)

---
## **Cybersecurity Terms and Concepts**

| Term                     | Definition                                                                                   |
|--------------------------|----------------------------------------------------------------------------------------------|
| Argument (Python)        | The data brought into a function when it is called                                           |
| Built-in function        | A function that exists within Python and can be called directly                              |
| Comment                  | A note programmers make about the intention behind their code                                 |
| Function                 | A section of code that can be reused in a program                                             |
| Global variable          | A variable that is available through the entire program                                       |
| Indentation              | Space added at the beginning of a line of code                                                |
| Library                  | A collection of modules that provide code users can access in their programs                  |
| Local variable           | A variable assigned within a function                                                        |
| Module                   | A Python file that contains additional functions, variables, classes, and any kind of runnable code |
| Parameter (Python)       | An object that is included in a function definition for use in that function                  |
| PEP 8 style guide        | A resource that provides stylistic guidelines for programmers working in Python              |
| Python Standard Library  | An extensive collection of Python code that often comes packaged with Python                  |
| Return statement         | A Python statement that executes inside a function and sends information back to the function call |
| Style guide              | A manual that informs the writing, formatting, and design of documents                        |
| User-defined function    | A function that programmers design for their specific needs                                   |

---