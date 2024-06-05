# Python in practice
## Essential Python Components for Automation
### Automating tasks in Python

- **Definition**: **Automation** reduces manual effort by using technology to perform repetitive tasks. In cybersecurity, Python is commonly used for automation.

### Variables

- **Definition**: A container that stores data.
- **Importance**: Avoids the need to rewrite values for each action.
- **Example:**
	```python
	login_attempts = ['user1', 'user2', 'flagged_user', 'user3']
	flagged_user = 'flagged_user'
	```

### Conditional Statements

- **Definition**: Evaluates code to determine if it meets specified conditions.
- **Importance**: Checks conditions before performing actions, increasing efficiency.
- **Example**:
	```python
	if flagged_user in login_attempts:
	    print("Flagged user has logged in.")
	```

### Iterative Statements

- **Definition**: Executes a set of instructions repeatedly.
- **Types**: `for` loops and `while` loops.
- **Example**:
	```python
	for user in login_attempts:
	    if user == flagged_user:
	        print("Flagged user login detected.")
	```

### Functions

- **Definition**: A reusable section of code.
- **Importance**: Reduces redundancy and improves readability.
- **Example**:
	```python
	def count_logins(logins, user):
	    count = 0
	    for login in logins:
	        if login == user:
	            count += 1
	    return count
	
	login_count = count_logins(login_attempts, flagged_user)
	print(f"Flagged user logged in {login_count} times.")
	```

### Techniques for Working with Strings

- **Importance**: String data is common in cybersecurity tasks.
- **Examples**:
	```python
	log_entry = "2024-05-31 12:00:00, flagged_user logged in"
	username = log_entry.split(",")[1].strip()
	print(username)  # Output: flagged_user logged in
	```

### Techniques for Working with Lists

- **Importance**: Lists store multiple items in a single variable.
- **Examples:**
	```python
	login_attempts.append('new_user')
	print(login_attempts)
	```

### Working with Files in Python
#### Log Files and Their Formats

- **Importance**: Logs are essential for tracking events in cybersecurity.
- **Common Formats**: `.txt` and `.csv`.

#### Reading from Files

- **Example: Reading a .txt file**
	```python
	with open('logfile.txt', 'r') as file:
	    logs = file.readlines()
	    for log in logs:
	        print(log.strip())
	```
- **Example: Reading a .csv file**
	```python
	import csv
	
	with open('logfile.csv', 'r') as file:
	    reader = csv.reader(file)
	    for row in reader:
	        print(row)
	```

#### Writing to Files

- **Example: Writing to a .txt file**
	```python
	with open('output.txt', 'w') as file:
	    file.write("Flagged user logged in 5 times.\n")
	```
- **Example: Writing to a .csv file**
	```python
	with open('output.csv', 'w', newline='') as file:
	    writer = csv.writer(file)
	    writer.writerow(['Username', 'Logins'])
	    writer.writerow(['flagged_user', 5])
	```

## Key Takeaways

- **Essential Components for Automation**:
    
    - Variables
    - Conditional Statements
    - Iterative Statements
    - Functions
    - Techniques for Working with Strings and Lists
    - File Handling Skills
- **Purpose**: Streamline and automate cybersecurity tasks, improving productivity and accuracy.

---
## Import Files into Python
### Working with files in cybersecurity

- **Log**: A record of events occurring within an organization's systems.
    - Example: Logs of login attempts or software application issues.

### Opening files in Python

- **Syntax**:
	```python
	with open("update_log.txt", "r") as file:
	    # file operations here
	```
	- **with**: Manages resources and handles errors; ensures the file is closed after exiting the block.
    - **open()**: Opens a file.
        - **Parameters**:
            - File name or file path.
            - Mode: "r" (read), "w" (write), "a" (append).
    - **as**: Assigns a variable to reference the opened file.
- **Example**:
	```python
	with open("update_log.txt", "r") as file:
	    content = file.read()
	    print(content)
	```

### Reading files in Python

- **.read()**: Converts the file content into a string.
    - Example:
		```python
		with open("update_log.txt", "r") as file:
		    updates = file.read()
		print(updates)
		```

- After reading, you can use string operations on the file content:
    - **.index()**: Find the index of a substring.
    - **len()**: Get the length of the string.

### Writing files in Python

- **Modes**:
    - "w": Write (replaces existing content or creates a new file).
    - "a": Append (adds new information to the end of an existing file).

- **.write()**: Writes string data to a file.
    - Example (writing):
		```python
		with open("update_log2.txt", "w") as file:
		    file.write("New log entry\n")
		```
	- Example (appending):
		```python
		line = "jrafael,192.168.243.140,4:56:27,True"
		with open("access_log.txt", "a") as file:
		    file.write(line)
		```

### Key Takeaways

- **Importing Files**: Use the `with` keyword, `open()` function, and `as` keyword.
- **Reading Files**: Use `.read()` method.
- **Writing Files**: Use `.write()` method with appropriate mode ("r", "w", "a").

---
# Work with Files in Python
### Parsing

- **Parsing**: Converting data into a more readable format for both Python and programmers.

#### .split()

- **The basics of .split()**:
    - Converts a string into a list based on a specified character.
    - **Example**:
		```python
		approved_users = "elarson,bmoreno,tshah,sgilmore,eraab"
		print("before .split():", approved_users)
		approved_users = approved_users.split(",")
		print("after .split():", approved_users)
		```
	- Without arguments, .split() separates the string at each whitespace.
	- Example:
		```python
		removed_users = "wjaffrey jsoto abernard jhill awilliam"
		print("before .split():", removed_users)
		removed_users = removed_users.split()
		print("after .split():", removed_users)
		```
	
- **Applying .split() to files**:
	- Converts file content to a list after reading it as a string.
	- Example:
		```python
		with open("update_log.txt", "r") as file:
		    updates = file.read()
		updates = updates.split()
		```

#### .join()

- **The basics of .join()**:
    - Converts a list into a string, separating elements with a specified character.
    - **Example:**
		```python
		approved_users = ["elarson", "bmoreno", "tshah", "sgilmore", "eraab"]
		print("before .join():", approved_users)
		approved_users = ",".join(approved_users)
		print("after .join():", approved_users)
		```
	- Newline character "\n" can be used to separate elements by new lines.

- **Applying .join() to files**:
	- Converts list back into a string for writing to a file.
	- **Example:**
		```python
		updates = " ".join(updates)
		with open("update_log.txt", "w") as file:
		    file.write(updates)
		```

### Key Takeaways

- **Parsing**: Essential for making file data readable.
- **.split()**: Converts a string into a list.
- **.join()**: Converts a list into a string.

---
## Debugging Techniques
### Definition of Debugging

- **Debugging**: Process of identifying and resolving errors or bugs in a computer program.

### Types of Errors
#### Syntax Errors

- **Definition**: Invalid usage of the programming language.
- **Examples**: Missing punctuation marks, such as closing brackets or colons.
- **Identification**: Error messages indicating location and nature of syntax errors.

#### Logic Errors

- **Definition**: Occur when code logic produces unintended results.
- **Examples**: Using wrong logical operator, assigning incorrect values in conditions.
- **Identification**: Examining program output and comparing with expected results.

#### Exceptions

- **Definition**: Errors that involve code unable to execute despite being syntactically correct.
- **Examples**: Name errors, index errors, type errors, file not found errors.
- **Identification**: Specific error messages like "NameError", "IndexError", "TypeError", "FileNotFoundError".

### Debugging Strategies

#### Debuggers

- **Definition**: Software tools to locate source of errors in a program.
- **Usage**: Step through code execution, set breakpoints, inspect variable values.

#### Use Print Statements

- **Definition**: Insert print statements strategically to identify source of errors.
- **Usage**: Display variable values, confirm execution flow, identify unexpected behavior.

### Key Takeaways

- Debugging involves identifying and resolving errors in a program.
- Syntax errors involve invalid language usage, logic errors result in unintended behavior, and exceptions indicate exceptional conditions.
- Debugging strategies include using debuggers for step-by-step inspection and print statements for real-time debugging.

---
## **Cybersecurity Terms and Concepts**

|Term|Definition|
|---|---|
|Automation|The use of technology to reduce human and manual effort to perform common and repetitive tasks|
|Conditional Statement|A statement that evaluates code to determine if it meets a specified set of conditions|
|Debugger|A software tool that helps to locate the source of an error and assess its causes|
|Debugging|The practice of identifying and fixing errors in code|
|Exception|An error that involves code that cannot be executed even though it is syntactically correct|
|File Path|The location of a file or directory|
|Function|A section of code that can be reused in a program|
|Integrated Development Environment (IDE)|A software application for writing code that provides editing assistance and error correction tools|
|Iterative Statement|Code that repeatedly executes a set of instructions|
|Log|A record of events that occur within an organization's systems|
|Logic Error|An error that results when the logic used in code produces unintended results|
|Parsing|The process of converting data into a more readable format|
|Syntax Error|An error that involves invalid usage of a programming language|
|Variable|A container that stores data|

---