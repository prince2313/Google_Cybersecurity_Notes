# Introduction to Python
## Get to Know Python
### How Programming Works

- **Programming**: Process of creating a specific set of instructions for a computer to execute tasks.
- Programs are everywhere: computers, cell phones, electronic devices.
- Multiple programming languages exist; Python is one of them.
- Programming languages are converted to binary numbers (0s and 1s) for the CPU to perform operations.
- Using binary directly is time-consuming for humans; programming languages like Python simplify this.

### Using Python to Program

- **Python**: General-purpose programming language for solving various problems (e.g., building websites, data analysis, automating tasks).
- Python code is converted by an **interpreter** into runnable instructions line by line.

#### Python Versions

- Multiple versions of Python exist; this course uses Python 3.
- Important to track the version used due to syntax differences.
- **Syntax**: Rules that determine what is correctly structured in a computing language.

### Python in Cybersecurity

- Python is especially useful for **automation** in cybersecurity.
- **Automation**: Reduces human and manual effort for repetitive tasks.
- Specific areas in cybersecurity where Python can be used:
  - **Log Analysis**: Automating the examination of log files for patterns, anomalies, or breaches.
  - **Malware Analysis**: Writing scripts to analyze malicious software.
  - **Access Control List Management**: Automating creation and management of access control lists.
  - **Intrusion Detection**: Developing systems to detect unauthorized access or breaches.
  - **Compliance Checks**: Automating the process of checking systems against compliance standards.
  - **Network Scanning**: Writing scripts to scan networks for vulnerabilities or unauthorized devices.

### Advantages of Python

- **Readability and Simplicity**: Python has a clean and straightforward syntax that makes it easy to read and write.
- **Versatility**: Can be used for web development, data analysis, artificial intelligence, scientific computing, automation, and more.
- **Large Standard Library**: Extensive library of modules and packages for various tasks.
- **Community Support**: Large and active community providing resources, libraries, and frameworks.
- **Cross-Platform Compatibility**: Runs on various operating systems, including Windows, macOS, and Linux.
- **Integration**: Easily integrates with other languages and technologies (e.g., C/C++, Java, .NET).
- **Rapid Development**: Allows for quick prototyping and iterative development due to its simplicity and versatility.

### Key Takeaways

- Python is used to create instructions for computers to complete tasks.
- Programming languages are converted to binary for machine understanding.
- Multiple Python versions exist with different syntax rules.
- Python is valuable in cybersecurity for automating repetitive tasks.

---
## Create a basic Python script

- **Comment:**
	- A note programmers make about the intention behind their code.

- **print():**
	- Output a specified object to the screen.

- **Syntax:**
	- The rules that determine what is correctly structured in a computing language.

---
## Python Environments
### Notebooks

- **Notebook**: An online interface for writing, storing, and running code. Allows documentation of information about the code.
- In this course, interaction with Python will be through notebooks.
- Notebook content appears in either a code cell or markdown cell.

#### Code Cells

- Meant for writing and running code.
- Notebooks provide a mechanism for running these code cells, often a play button within the cell.
- Output appears after the code when run.

#### Markdown Cells

- Meant for describing the code.
- Allows formatting of text using markdown language.
- Markdown is used for formatting plain text in text editors and code editors (e.g., headers).

#### Common Notebook Environments

- **Jupyter Notebook**: [Jupyter](https://jupyter.org/about)
- **Google Colaboratory (Google Colab)**: [Google Colab](https://colab.sandbox.google.com/)
- Both allow running several programming languages, including Python.

### Integrated Development Environments (IDEs)

- **IDE**: Software application for writing code that provides editing assistance and error correction tools.
- IDEs include a graphical user interface (GUI) offering customization and building options for programs.

### Command Line

- **Command-line interface (CLI)**: Text-based user interface using commands to interact with the computer.
- Allows running Python programs, accessing files and directories, and opening file editors to create new Python files.

### Key Takeaways

- Security analysts can access Python through various environments:
  - Notebooks
  - Integrated development environments (IDEs)
  - Command line
- In this course, notebooks will be used:
  - Notebooks contain code cells for writing and running code.
  - Markdown cells for plain text descriptions.

---
## More about data types

### Definition

- **Data type:**
	- A category for a particular type of data item.

### Data types

#### String

- **Definition**: An ordered sequence of characters.
- **Examples**: 
  - `"updates needed"`
  - `"20%"`
  - `"5.0"`
  - `"35"`
  - `"**/**/**"`
  - `""`
- **Note**: The last item ("") is an empty string.
- **Usage**: Represent text data.

#### List

- **Definition**: A collection of items in sequential form.
- **Examples**: 
  - `[12, 36, 54, 1, 7]`
  - `["eraab", "arusso", "drosas"]`
  - `[True, False, True, True]`
  - `[15, "approved", True, 45.5, False]`
  - `[]`
- **Note**: The last item [] is an empty list.
- **Usage**: Store multiple values in a single variable.

#### Integer

- **Definition**: A whole number without a decimal point.
- **Examples**:
  - `-100`
  - `-12`
  - `-1`
  - `0`
  - `1`
  - `20`
  - `500`
- **Usage**: Represent numerical data without fractions.

#### Float

- **Definition**: A number with a decimal point.
- **Examples**:
  - `-2.2`
  - `-1.34`
  - `0.0`
  - `0.34`
- **Usage**: Represent numerical data with fractions.

#### Boolean 

- **Definition**: Data with two possible values: True or False.
- **Examples**:
  - `True`
  - `False`
- **Usage**: Represent logical values in conditions and comparisons.

### Additional data types

In this course, you will work with the string, list, integer, float, and Boolean data types, but there are other data types. These additional data types include tuple data, dictionary data, and set data.

#### Tuple

- **Definition**: A collection of data that cannot be changed.
- **Examples**:
  - `("wjaffrey", "arutley", "dkot")`
  - `(46, 2, 13, 2, 8, 0, 0)`
  - `(True, False, True, True)`
  - `("wjaffrey", 13, True)`
- **Pro tip**: Tuples are more memory efficient than lists.
- **Usage**: Store fixed collections of items.

#### Dictionary

- **Definition**: Data consisting of key-value pairs.
- **Examples**:
  - `{1: "East", 2: "West", 3: "North", 4: "South"}`
- **Usage**: Store structured data with unique keys.

#### Set

- **Definition**: An unordered collection of unique values.
- **Examples**:
  - `{"jlanksy", "drosas", "nmason"}`
- **Usage**: Store collections of distinct items.

### Key takeaways

- Familiarity with various Python data types is crucial for security analysts.
- Data types include string, list, integer, float, and Boolean.
- Additional data types include tuple, dictionary, and set.

---
## Variables in Python
### What are variables?

- **Definition**: Containers that store data in a programming language.
- **Properties**: Named storage location, can hold values of different data types.
- **Mutability**: Values stored in variables can change.

### Working with variables
#### Assigning and reassigning variables

- Syntax: `variable_name = value`
- Reassigning: Giving a new value to an existing variable.
- Example:
  ```python
	username = "nzhao"
	username = "zhao2"
	```
#### Assigning variables to variables

- Syntax: `variable1 = variable2`
- Example:
	```python
	username = "nzhao"
	old_username = username
	```

#### Putting it together

- Demonstrates updating a username:
	```python
	username = "nzhao"
	old_username = username
	username = "zhao2"
	```

### `type()` function

- **Definition**: Returns the data type of an object.
- **Syntax**: `type(object)`
- **Example**:
	```python
	x = 5
	print(type(x))  # Output: <class 'int'>
	```

### Type Error

- **Definition**: An error that results from using the wrong data type.
- **Example**:
	```python
	x = "Hello"
	y = 5
	print(x + y)  # Raises TypeError: can only concatenate str (not "int") to str
	```

### Best practices for naming variables

- **Syntax rules**:
    - Use letters, numbers, and underscores.
    - Start with a letter or underscore, not a number.
    - Case-sensitive.
    - Avoid using Python keywords.
- **Stylistic guidelines**:
    - Separate words with underscores or capitalize each word except the first.
    - Avoid similar names causing confusion.
    - Keep names descriptive but concise.

### Key takeaways

- Variables store and manipulate data in Python.
- Understanding assignment and reassignment is crucial.
- Following naming conventions improves code readability.

---
## More on conditionals in Python

### How conditional statements work

- **Conditional statement**: Evaluates code based on specific conditions, resulting in either True or False.
- Common comparison operators for numerical values:

| Operator | Use                        |
|----------|----------------------------|
| >        | greater than               |
| <        | less than                  |
| >=       | greater than or equal to   |
| <=       | less than or equal to      |
| ==       | equal to                   |
| !=       | not equal to               |

#### `if` statements

- Keyword `if` starts a conditional statement.
- Syntax: 
  ```python
	if condition:
		# Body
	```

- The body executes if the condition evaluates to True.

##### `if` statement components

- **Header**: Starts with `if` followed by a condition and ends with a colon.
- **Body**: Code block indented under the header, executed if the condition is True.

### Continuing conditionals with `else` and `elif`

- **`else` statements**:
    - Executes when all preceding conditions in the `if` statement evaluate to False.
    - Syntax:
		```python
		else:
		    # Body
		```

- **`elif` statements**:
	- Used for additional conditions if preceding conditions are False.
	- Syntax:
		```python
		elif condition:
		    # Body
		```

### Logical operators for multiple conditions

- **`and`**: Requires both conditions to be True.
- **`or`**: Requires at least one condition to be True.
- **`not`**: Negates the condition (True becomes False, and vice versa).

#### Examples

- **`and`**:
	```python
	if status > 200 and status < 226:
	    print("successful response")
	```

- **`or`**:
	```python
	if status == 100 or status == 102:
	    print("informational response")
	```

- **`not`**:
	```python
	if not (status >= 200 and status <= 226):
	    print("check status")
	```

### Key takeaways

- Conditional statements are crucial for automating tasks.
- Use `if`, `else`, and `elif` to handle different conditions.
- Logical operators (`and`, `or`, `not`) enhance conditionals' flexibility.#

---
## More on loops in Python
### How conditional statements work

- **Iterative statement**: Repeatedly executes a set of instructions based on certain criteria.
- Iterative statements include for loops and while loops.

#### for loops

- Used to iterate through a specified sequence.
- Syntax:
	```python
	for i in sequence:
	    # Body
	```
- `i` is the loop variable, and `sequence` is the sequence to iterate through.

##### Looping through a list

- Easily iterate through lists using for loops.
- Example:
	```python
	computer_assets = ["laptop1", "desktop20", "smartphone03"]
	for asset in computer_assets:
	    print(asset)
	```

##### Using range()

- Generate a sequence of numbers for iterating through a for loop.
- Syntax: `range(start, stop, step)`
- Example:
	```python
	for i in range(0, 5, 1):
	    print(i)
	```

#### while loops

- Used to iterate based on a condition.
- Syntax:
	```python
	while condition:
	    # Body
	```
- Iterates as long as the condition is True.

##### Integers in the loop condition

- Loop condition based on integer values.
- Example:
	```python
	login_attempts = 0
	while login_attempts < 5:
	    print("Login attempts:", login_attempts)
	    login_attempts = login_attempts + 1
	```

##### Boolean values in the loop condition

- Loop condition based on Boolean values.
- Example:
	```python
	count = 0
	login_status = True
	while login_status == True:
	    print("Try again.")
	    count = count + 1
	    if count == 4:
	        login_status = False
	```

### Managing loops
#### break

- Exits a loop based on a condition.
- Example:
	```python
	computer_assets = ["laptop1", "desktop20", "smartphone03"]
	for asset in computer_assets:
	    if asset == "desktop20":
	        break
	    print(asset)
	```

#### continue

- Skips an iteration based on a condition.
- Example:
	```python
	computer_assets = ["laptop1", "desktop20", "smartphone03"]
	for asset in computer_assets:
	    if asset == "desktop20":
	        continue
	    print(asset)
	```

### Infinite loops

- Loops that do not exit.
- Terminate with CTRL-C or CTRL-Z.
- Common in services like web servers.

### Key takeaways

- Security analysts use iterative statements for various tasks.
- for loops iterate through lists or sequences.
- while loops iterate based on conditions.
- break and continue keywords control loop execution.

---
## **Cybersecurity Terms and Concepts**

| Term                                          | Definition                                                                                                         |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| Automation                                   | The use of technology to reduce human and manual effort to perform common and repetitive tasks                     |
| Boolean data                                 | Data that can only be one of two values: either True or False                                                     |
| Command-line interface                       | A text-based user interface that uses commands to interact with the computer                                       |
| Comment                                      | A note programmers make about the intention behind their code                                                     |
| Conditional statement                        | A statement that evaluates code to determine if it meets a specified set of conditions                              |
| Data type                                    | A category for a particular type of data item                                                                      |
| Dictionary data                              | Data that consists of one or more key-value pairs                                                                  |
| Float data                                   | Data consisting of a number with a decimal point                                                                   |
| Integer data                                 | Data consisting of a number that does not include a decimal point                                                   |
| Integrated development environment (IDE)     | A software application for writing code that provides editing assistance and error correction tools                 |
| Interpreter                                  | A computer program that translates Python code into runnable instructions line by line                               |
| Iterative statement                          | Code that repeatedly executes a set of instructions                                                                |
| List data                                    | Data structure that consists of a collection of data in sequential form                                             |
| Loop variable                                | A variable that is used to control the iterations of a loop                                                        |
| Notebook                                    | An online interface for writing, storing, and running code                                                         |
| Programming                                 | A process that can be used to create a specific set of instructions for a computer to execute tasks                 |
| Set data                                    | Data that consists of an unordered collection of unique values                                                     |
| String data                                  | Data consisting of an ordered sequence of characters                                                              |
| Syntax                                      | The rules that determine what is correctly structured in a computing language                                       |
| Tuple data                                  | Data structure that consists of a collection of data that cannot be changed                                         |
| Type error                                  | An error that results from using the wrong data type                                                               |
| Variable                                    | A container that stores data                                                                                      |

---