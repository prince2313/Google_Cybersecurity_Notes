# **Work with strings and lists**
## Strings and the Security Analyst
### String data in a security setting

- **String data**: Ordered sequence of characters.
- Common in cybersecurity: IP addresses, usernames, URLs, employee IDs.
- Used for storing information that doesn't require mathematical manipulation.

### Definitions
#### Immutable

- **Immutable**: An object whose state cannot be modified after it is created. Strings in Python are immutable, meaning once a string is created, its characters cannot be changed.

#### Method

- **Method**: A function that belongs to an object and is accessed using the dot notation. Methods can operate on data contained within the object.

#### String Concatenation

- **String concatenation**: The process of joining two or more strings end-to-end to form a single string. In Python, this can be done using the `+` operator.
  ```python
  string1 = "Hello"
  string2 = "World"
  result = string1 + " " + string2  # Output: 'Hello World'
	```

### Working with indices in strings
#### Indices

- **Index**: Number indicating the position of each character in a string.
- Indices start at 0.
- Example: `"h32rb17"`

|Character|Index|
|---|---|
|h|0|
|3|1|
|2|2|
|r|3|
|b|4|
|1|5|
|7|6|

- Negative indices count from the end of the string.

|Character|Index|
|---|---|
|h|-7|
|3|-6|
|2|-5|
|r|-4|
|b|-3|
|1|-2|
|7|-1|

#### Bracket notation

- Used to extract parts of a string using indices.
- Example:
	```python
	device_id = "h32rb17"
	print(device_id[0])  # Output: 'h'
	print(device_id[-1]) # Output: '7'
	print(device_id[0:3]) # Output: 'h32'
	```

### String functions and methods
#### str() and len()

- **str()**: Converts input to a string.
	```python
	string_id = str(19329302)
	print(string_id)  # Output: '19329302'
	```
- **len()**: Returns the number of characters in a string.
	```python
	device_id_length = len("h32rb17")
	if device_id_length == 7:
	    print("The device ID has 7 characters.")  # Output: The device ID has 7 characters.
	```

#### .upper() and .lower()

- **.upper()**: Converts all characters in a string to uppercase.
	```python
	department = "Information Technology"
	print(department.upper())  # Output: 'INFORMATION TECHNOLOGY'
	```
- **.lower()**: Converts all characters in a string to lowercase
	```python
	department = "Information Technology"
	print(department.lower())  # Output: 'information technology'
	```

#### .index()

- **.index()**: Returns the index of the first occurrence of a character or substring.
	```python
	device_id = "h32rb17"
	print(device_id.index("r"))  # Output: 3
	```
- Raises `ValueError` if the character/substring is not found.
- Finding substrings:
	```python
	users = "tsnow, tshah, bmoreno - updated"
	print(users.index("tshah"))  # Output: 7
	```

### Practical Applications in Cybersecurity

1. **IP Address Manipulation**: Extracting segments of IP addresses.
	```python
	ip_address = "192.168.1.1"
	first_octet = ip_address.split('.')[0]
	print(first_octet)  # Output: '192'
	```
2. **Username Validation**: Ensuring usernames meet criteria.
	```python
	username = "adminUser1"
	if username[0].islower():
	    print("Username must start with an uppercase letter.")
	```
3. **URL Handling**: Extracting domain names or paths from URLs.
	```python
	url = "https://example.com/path"
	domain = url.split('//')[1].split('/')[0]
	print(domain)  # Output: 'example.com'
	```
4. **Log Analysis**: Searching for specific entries in log files.
	```python
	log_entry = "User tshah logged in at 10:00 AM"
	if "tshah" in log_entry:
	    print("tshah found in log entry.")
	```

---
## Lists and the Security Analyst
### List data in a security setting
- **List data**: A data structure consisting of a collection of data in sequential form.
- Can store multiple elements in a single variable and can contain multiple data types.
- Used to store usernames, IP addresses, URLs, device IDs, and other data in a cybersecurity context.
- Allows performing actions on multiple items, e.g., iterating through a list of device IDs.

### Working with indices in lists
#### Indices
- Indices start at 0 and are assigned to each element in the list.
- Example list: `["elarson", "fgarcia", "tshah", "sgilmore"]`

| **Element** | **Index** |
|-------------|-----------|
| "elarson"   | 0         |
| "fgarcia"   | 1         |
| "tshah"     | 2         |
| "sgilmore"  | 3         |

### Bracket notation
- Used to extract elements or slices in a list using indices.
- Example:
  ```python
  username_list = ["elarson", "fgarcia", "tshah", "sgilmore"]
  print(username_list[2])  # Output: 'tshah'
	```
#### Extracting a slice from a list

- Extracting a slice results in another list (sublist).
- Example:
	```python
	username_list = ["elarson", "fgarcia", "tshah", "sgilmore"]
	print(username_list[0:2])  # Output: ['elarson', 'fgarcia']
	```

### Changing the elements in a list

- Lists are mutable and can be changed after creation.
- Example:
	```python
	username_list = ["elarson", "fgarcia", "tshah", "sgilmore"]
	username_list[1] = "bmoreno"
	print(username_list)  # Output: ['elarson', 'bmoreno', 'tshah', 'sgilmore']
	```

### List methods

- Functions specific to the list data type.

#### .insert()

- Adds an element at a specific position.
- Example:
	```python
	username_list = ["elarson", "bmoreno", "tshah", "sgilmore"]
	username_list.insert(2, "wjaffrey")
	print(username_list)  # Output: ['elarson', 'bmoreno', 'wjaffrey', 'tshah', 'sgilmore']
	```

#### .remove()

- Removes the first occurrence of a specific element.
- Example:
	```python
	username_list = ["elarson", "bmoreno", "wjaffrey", "tshah", "sgilmore"]
	username_list.remove("elarson")
	print(username_list)  # Output: ['bmoreno', 'wjaffrey', 'tshah', 'sgilmore']
	```

#### .append()

- Adds an element to the end of a list.
- Example:
	```python
	username_list = ["bmoreno", "wjaffrey", "tshah", "sgilmore"]
	username_list.append("btang")
	print(username_list)  # Output: ['bmoreno', 'wjaffrey', 'tshah', 'sgilmore', 'btang']
	```
- Using .append() with a for loop:
	```python
	numbers_list = []
	for i in range(10):
	    numbers_list.append(i)
	print(numbers_list)  # Output: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
	```

### .index()

- Finds the first occurrence of an element and returns its index.
- Example:
	```python
	username_list = ["bmoreno", "wjaffrey", "tshah", "sgilmore", "btang"]
	username_index = username_list.index("tshah")
	print(username_index)  # Output: 2
	```

### List Concatenation

- **List concatenation**: The process of combining two or more lists into one.
- Achieved using the `+` operator.
- Example:
	```python
	list1 = [1, 2, 3]
	list2 = [4, 5, 6]
	combined_list = list1 + list2
	print(combined_list)  # Output: [1, 2, 3, 4, 5, 6]
	```

### Algorithm

- **Algorithm**: A step-by-step procedure or formula for solving a problem.
- In programming, it refers to a set of instructions designed to perform a specific task.
- Example: Sorting a list of numbers, searching for an item in a list.

### Key takeaways

- Python offers various ways to work with lists.
- Bracket notation can extract and alter elements and slices.
- List methods (e.g., .insert(), .remove(), .append(), .index()) provide additional functionality for manipulating lists.
- List concatenation allows combining multiple lists into one.
- Algorithms are fundamental to problem-solving in programming and cybersecurity.

---
## Regular Expressions in Python
### What is a Regular Expression?
- A **regular expression (regex)** is a sequence of characters that define a search pattern.
- Used for text processing tasks such as searching logs, extracting data, and validating inputs.

### Using the `re` Module in Python
```python
import re
```

### Basic Functions of `re`
#### `re.findall()`

- Returns a list of all non-overlapping matches of a pattern in a string.
- **Example:**
	```python
	import re
	matches = re.findall("ts", "tsnow, tshah, bmoreno")
	print(matches)  # Output: ['ts', 'ts']
	```
### Regular Expression Symbols
#### Character Type Symbols

- `\w`: Matches any alphanumeric character (letters, digits, and underscores).
- `\d`: Matches any single digit (0-9).
- `\s`: Matches any whitespace character (spaces, tabs, etc.).
- `.`: Matches any character except a newline.
- `\\.`: Matches a literal period (dot) character.
- **Example:**
	```python
	import re
	matches = re.findall("\d+", "h32rb17")
	print(matches)  # Output: ['32', '17']
	
	matches = re.findall("\d*", "h32rb17")
	print(matches)  # Output: ['', '32', '', '', '', '17', '']
	
	matches = re.findall("\d{2}", "h32rb17 k825t0m c2994eh")
	print(matches)  # Output: ['32', '17', '82', '29', '94']
	
	matches = re.findall("\d{1,3}", "h32rb17 k825t0m c2994eh")
	print(matches)  # Output: ['32', '17', '825', '0', '299', '4']
	```

### Constructing Complex Patterns

- To extract specific parts of a string, break down the pattern into components and use regular expression symbols to represent these components.
- **Example:** Given a string with employee information:
	```python
	employee_logins_string = "1001 bmoreno: 12 Marketing 1002 tshah: 7 Human Resources 1003 sgilmore: 5 Finance"
	```
- You want to extract usernames and login attempts:
	```python
	import re
	pattern = r"\w+:\s\d+"
	matches = re.findall(pattern, employee_logins_string)
	print(matches)  # Output: ['bmoreno: 12', 'tshah: 7', 'sgilmore: 5']
	```

### Best Practices

1. **Test Your Patterns**: Regular expressions can be tricky and might match more or less than intended. Always test your patterns with various inputs.
2. **Use Raw Strings**: In Python, use raw string notation (prefix the pattern with `r`) to avoid conflicts with Python's escape sequences.

### Key Takeaways

- Regular expressions are powerful for pattern matching and text processing.
- Use the `re` module in Python to work with regular expressions.
- Combine characters and special symbols to form complex patterns.
- Quantifiers allow you to specify how many times a character or group should repeat.
- Always test your regular expressions to ensure they match the intended patterns.

### References

- Python `re` module documentation: [Python re Module](https://docs.python.org/3/library/re.html)

---
## **Cybersecurity Terms and Concepts**

|Term|Definition|
|---|---|
|Algorithm|A set of rules that solve a problem.|
|Bracket notation|The indices placed in square brackets.|
|Debugging|The practice of identifying and fixing errors in code.|
|Immutable|An object that cannot be changed after it is created and assigned a value.|
|Index|A number assigned to every element in a sequence that indicates its position.|
|List concatenation|The concept of combining two lists into one by placing the elements of the second list directly after the elements of the first list.|
|List data|Data structure that consists of a collection of data in sequential form.|
|Method|A function that belongs to a specific data type.|
|Regular expression (regex)|A sequence of characters that forms a pattern.|
|String concatenation|The process of joining two strings together.|
|String data|Data consisting of an ordered sequence of characters.|
|Substring|A continuous sequence of characters within a string.|

---