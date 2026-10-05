

## 📌 Overview

A **function** is a reusable block of Python code that performs a specific task.

Instead of writing the same code again and again, we can put it inside a function and call the function whenever we need it.

Functions are very important in:

- Python programming
- Automation
- Cloud/DevOps scripts
- AWS automation
- API development
- Data processing

---

# 1. Why Do We Need Functions?

Suppose we want to print a welcome message three times.

Without a function:

```python
print("Welcome to Python")
print("Welcome to Python")
print("Welcome to Python")
```

This repeats the same code.

With a function:

```python
def welcome():
    print("Welcome to Python")

welcome()
welcome()
welcome()
```

Now we write the code only once and reuse it.

---

# 2. Creating a Function

We use the `def` keyword to create a function.

### Syntax

```python
def function_name():
    # code
```

### Example

```python
def greet():
    print("Hello, Adi")
```

Here:

- `def` → keyword used to create a function
- `greet` → function name
- `()` → parentheses
- `:` → starts the function body
- Indented code → function body

---

# 3. Calling a Function

Creating a function does not execute it.

We need to **call** the function.

```python
def greet():
    print("Hello, Adi")

greet()
```

Output:

```text
Hello, Adi
```

The function runs when we write:

```python
greet()
```

---

# 4. Function Flow

A simple function works like this:

```text
Create Function
      ↓
   def greet()
      ↓
Call Function
      ↓
   greet()
      ↓
Function Executes
```

---

# 5. Simple Function Example

```python
def start_server():
    print("Server started")

start_server()
```

Output:

```text
Server started
```

This is a simple example of how functions can be used for automation tasks.

---

# 6. Function with Multiple Statements

A function can contain multiple lines of code.

```python
def server_info():
    print("Server Name: Web Server")
    print("Status: Running")
    print("Port: 80")

server_info()
```

Output:

```text
Server Name: Web Server
Status: Running
Port: 80
```

---

# 7. Calling a Function Multiple Times

One of the main advantages of functions is **reusability**.

```python
def welcome():
    print("Welcome to Cloud Computing")

welcome()
welcome()
welcome()
```

Output:

```text
Welcome to Cloud Computing
Welcome to Cloud Computing
Welcome to Cloud Computing
```

We created the code once but used it three times.

---

# 8. Functions with Parameters

Sometimes we want to give information to a function.

This is where **parameters** are useful.

```python
def greet(name):
    print("Hello", name)

greet("Adi")
```

Output:

```text
Hello Adi
```

Here:

```text
name
```

is the parameter.

```text
"Adi"
```

is the value passed to the function.

---

# 9. Parameter vs Argument

These two terms are important.

### Parameter

The variable written inside the function definition.

```python
def greet(name):
```

Here `name` is a **parameter**.

### Argument

The actual value passed when calling the function.

```python
greet("Adi")
```

Here `"Adi"` is an **argument**.

### Simple Difference

```text
Parameter → Variable in function definition
Argument  → Actual value passed to function
```

---

# 10. Function with Two Parameters

A function can have multiple parameters.

```python
def add(a, b):
    print(a + b)

add(10, 20)
```

Output:

```text
30
```

Here:

- `a` → parameter
- `b` → parameter
- `10` → argument
- `20` → argument

---

# 11. Function with Three Parameters

```python
def student_info(name, age, course):
    print("Name:", name)
    print("Age:", age)
    print("Course:", course)

student_info("Adi", 21, "CSE")
```

Output:

```text
Name: Adi
Age: 21
Course: CSE
```

---

# 12. Function to Check Server Status

We can use functions for Cloud/DevOps-related tasks.

```python
def check_server():
    status = "running"

    if status == "running":
        print("Server is running")
    else:
        print("Server is stopped")

check_server()
```

Output:

```text
Server is running
```

---

# 13. Function with a Server Name

```python
def check_server(server_name):
    print("Checking server:", server_name)

check_server("web-server")
```

Output:

```text
Checking server: web-server
```

We can reuse the same function for different servers:

```python
check_server("web-server")
check_server("database-server")
check_server("app-server")
```

---

# 14. Function with a List

Functions can also work with lists.

```python
def show_servers(servers):
    for server in servers:
        print(server)

servers = ["web-server", "app-server", "database-server"]

show_servers(servers)
```

Output:

```text
web-server
app-server
database-server
```

---

# 15. Function with a Dictionary

Functions can also receive dictionaries.

```python
def show_server(server):
    print("Name:", server["name"])
    print("Status:", server["status"])

server = {
    "name": "web-server",
    "status": "running"
}

show_server(server)
```

Output:

```text
Name: web-server
Status: running
```

This is useful when working with structured Cloud/DevOps data.

---

# 16. Returning a Value

A function can **return** a result using the `return` keyword.

Example:

```python
def add(a, b):
    return a + b

result = add(10, 20)

print(result)
```

Output:

```text
30
```

Here the function calculates:

```text
10 + 20 = 30
```

and sends `30` back to the caller.

---

# 17. `print()` vs `return`

This is an important concept.

### Using `print()`

```python
def add(a, b):
    print(a + b)

add(10, 20)
```

The result is displayed.

### Using `return`

```python
def add(a, b):
    return a + b

result = add(10, 20)

print(result)
```

The result can be stored in a variable and used later.

### Simple Difference

```text
print()  → Displays the result
return   → Sends the result back
```

---

# 18. Using the Returned Value

A returned value can be used in another calculation.

```python
def add(a, b):
    return a + b

result = add(10, 20)

print(result * 2)
```

Output:

```text
60
```

Because:

```text
10 + 20 = 30
30 × 2 = 60
```

---

# 19. Function Returning a String

```python
def get_message():
    return "Server is running"

message = get_message()

print(message)
```

Output:

```text
Server is running
```

---

# 20. Function Returning Boolean

Functions can return `True` or `False`.

```python
def is_server_running(status):
    if status == "running":
        return True
    else:
        return False

result = is_server_running("running")

print(result)
```

Output:

```text
True
```

We can simplify this:

```python
def is_server_running(status):
    return status == "running"

print(is_server_running("running"))
```

---

# 21. Function with No Parameters

A function does not always need parameters.

```python
def show_message():
    print("Python is easy to learn")

show_message()
```

---

# 22. Function with One Parameter

```python
def greet(name):
    print("Hello", name)

greet("Adi")
```

---

# 23. Function with Multiple Parameters

```python
def student(name, age, course):
    print(name)
    print(age)
    print(course)

student("Adi", 21, "CSE")
```

So functions can have:

```text
No parameters
     ↓
One parameter
     ↓
Multiple parameters
```

---

# 24. Default Parameter

A parameter can have a default value.

```python
def greet(name="User"):
    print("Hello", name)

greet()
```

Output:

```text
Hello User
```

If we provide a value:

```python
greet("Adi")
```

Output:

```text
Hello Adi
```

The provided value replaces the default value.

---

# 25. Simple Calculator Using Functions

We can create separate functions for mathematical operations.

```python
def add(a, b):
    return a + b


def subtract(a, b):
    return a - b


def multiply(a, b):
    return a * b


print(add(10, 5))
print(subtract(10, 5))
print(multiply(10, 5))
```

Output:

```text
15
5
50
```

This is better than writing all the calculations repeatedly.

---

# 26. Function Calling Another Function

One function can call another function.

```python
def greet():
    print("Hello")

def start():
    greet()
    print("Program started")

start()
```

Output:

```text
Hello
Program started
```

---

# 27. Function with Conditions

A function can contain `if`, `elif`, and `else`.

```python
def check_number(number):
    if number > 0:
        print("Positive")
    elif number < 0:
        print("Negative")
    else:
        print("Zero")

check_number(10)
```

Output:

```text
Positive
```

---

# 28. Function with a Loop

A function can also contain loops.

```python
def show_numbers():
    for i in range(1, 6):
        print(i)

show_numbers()
```

Output:

```text
1
2
3
4
5
```

---

# 29. Practical Cloud/DevOps Example

Suppose we have multiple servers.

```python
def check_status(server, status):
    if status == "running":
        print(server, "is running")
    else:
        print(server, "is stopped")


check_status("web-server", "running")
check_status("database-server", "stopped")
check_status("app-server", "running")
```

Output:

```text
web-server is running
database-server is stopped
app-server is running
```

The same function can be reused for many servers.

---

# 30. Function for AWS Region

```python
def show_region(region):
    print("AWS Region:", region)

show_region("ap-south-1")
```

Output:

```text
AWS Region: ap-south-1
```

---

# 31. Function to Check an AWS Instance

```python
def check_instance(instance_id, status):
    if status == "running":
        return instance_id + " is running"
    else:
        return instance_id + " is stopped"


result = check_instance("i-123456", "running")

print(result)
```

Output:

```text
i-123456 is running
```

This is a simple example of how functions can later be used in AWS automation scripts.

---

# 32. Variable Scope — Basic Introduction

**Scope** means where a variable can be accessed.

For now, understand two basic types:

- Local variable
- Global variable

### Local Variable

A variable created inside a function is normally available only inside that function.

```python
def test():
    message = "Hello"
    print(message)

test()
```

Here `message` is a local variable.

---

# 33. Global Variable

A variable created outside a function is a global variable.

```python
message = "Hello Python"

def show_message():
    print(message)

show_message()
```

Output:

```text
Hello Python
```

We will study **scope in more detail on Day 10**.

---

# 34. Docstrings

A docstring is a description written inside a function.

```python
def greet():
    """This function prints a greeting message."""
    print("Hello")

greet()
```

Docstrings help explain what a function does.

---

# 35. Built-in Functions vs User-defined Functions

Python already provides many functions.

These are called **built-in functions**.

Examples:

```python
print()
len()
type()
input()
sum()
max()
min()
```

Example:

```python
numbers = [10, 20, 30]

print(len(numbers))
print(sum(numbers))
```

We can also create our own functions.

These are called **user-defined functions**.

```python
def greet():
    print("Hello")

greet()
```

---

# 36. Why Functions Are Important

Functions provide several benefits.

### 1. Reusability

Write code once and use it many times.

### 2. Less Code

Avoid repeating the same code.

### 3. Organization

Divide a large program into smaller parts.

### 4. Easy Maintenance

Changing the function changes the behavior wherever it is used.

### 5. Automation

Functions are heavily used in Cloud and DevOps scripts.

---

# 37. Function Structure

Remember this basic structure:

```python
def function_name(parameters):
    # function code
    return result
```

Example:

```python
def add(a, b):
    result = a + b
    return result
```

Calling the function:

```python
answer = add(10, 20)

print(answer)
```

---

# 38. Complete Example

Here is a small program combining several concepts:

```python
def check_server(server_name, status):
    if status == "running":
        return server_name + " is running"
    else:
        return server_name + " is stopped"


servers = [
    ("web-server", "running"),
    ("database-server", "stopped"),
    ("app-server", "running")
]

for server_name, status in servers:
    result = check_server(server_name, status)
    print(result)
```

Output:

```text
web-server is running
database-server is stopped
app-server is running
```

This example combines:

- Function
- Parameters
- `return`
- `if/else`
- List
- Loop
- Cloud/DevOps-style server data

---

# 39. Common Beginner Mistakes

## Mistake 1 — Forgetting to call the function

```python
def greet():
    print("Hello")
```

Nothing happens until we call:

```python
greet()
```

---

## Mistake 2 — Incorrect indentation

Incorrect:

```python
def greet():
print("Hello")
```

Correct:

```python
def greet():
    print("Hello")
```

Python uses indentation to identify the function body.

---

## Mistake 3 — Forgetting the colon

Incorrect:

```python
def greet()
```

Correct:

```python
def greet():
```

---

## Mistake 4 — Using a variable before returning it

Make sure the value exists before returning it.

Correct:

```python
def add(a, b):
    result = a + b
    return result
```

---

# 40. Practice Questions

### Practice 1 — Greeting Function

Create a function called `greet()` that prints:

```text
Hello, Welcome to Python
```

---

### Practice 2 — Name Function

Create a function that accepts a name and prints:

```text
Hello Adi
```

---

### Practice 3 — Addition

Create a function that accepts two numbers and returns their sum.

Example:

```python
add(10, 20)
```

Expected result:

```text
30
```

---

### Practice 4 — Even or Odd

Create a function that accepts a number and checks whether it is even or odd.

---

### Practice 5 — Server Status

Create a function:

```python
check_server(server_name, status)
```

If the status is `"running"`, print:

```text
Server is running
```

Otherwise print:

```text
Server is stopped
```

---

### Practice 6 — AWS Region

Create a function that accepts an AWS region and prints it.

Example:

```python
show_region("ap-south-1")
```

---

# 41. Day 9 Key Points

Remember these concepts:

```text
def        → Creates a function
()         → Function parameters
:          → Starts function body
call       → Executes the function
parameter  → Variable in function definition
argument   → Value passed to function
return     → Sends a value back
```

Example:

```python
def add(a, b):
    return a + b

result = add(10, 20)

print(result)
```

---

# ✅ Day 9 Checklist

- [ ] I understand what a function is
- [ ] I understand why functions are useful
- [ ] I can create a function using `def`
- [ ] I can call a function
- [ ] I understand parameters
- [ ] I understand arguments
- [ ] I can use one or more parameters
- [ ] I understand `return`
- [ ] I know the difference between `print()` and `return`
- [ ] I can use conditions inside functions
- [ ] I can use loops inside functions
- [ ] I understand default parameters
- [ ] I understand the basic idea of local and global scope
- [ ] I can create simple Cloud/DevOps functions

---

# 🚀 Next — Day 10

## Function Arguments, Return Values and Scope

On Day 10, we will go deeper into:

- Positional arguments
- Keyword arguments
- Default arguments
- Multiple arguments
- `*args`
- `**kwargs`
- Return values
- Multiple return values
- Local scope
- Global scope
- Practical examples

These concepts will make your functions much more powerful and useful for Python automation.

