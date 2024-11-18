#### **1. Conditional Statements**

Conditional statements allow your program to execute certain pieces of code based on specific conditions.

**Syntax:**

```python
if condition:
    # code block executed if condition is true
elif another_condition:
    # code block executed if previous conditions are false and this condition is true
else:
    # code block executed if all above conditions are false
```

**Example:**

```python
age = 20

if age < 13:
    print("You are a child.")
elif age < 18:
    print("You are a teenager.")
else:
    print("You are an adult.")
```

**Output:**

```
You are an adult.
```

**Logical Operators:**

- `and`: True if both conditions are true.
- `or`: True if at least one condition is true.
- `not`: Inverts the truth value.

**Example:**

```python
is_member = True
age = 17

if is_member and age >= 18:
    print("Access granted.")
else:
    print("Access denied.")
```

**Output:**

```
Access denied.
```

---

#### **2. Loops**

Loops are used to execute a block of code repeatedly.

##### **`for` Loops**

Used to iterate over a sequence.

**Syntax:**

```python
for variable in sequence:
    # code block
```

**Example:**

```python
for i in range(5):
    print(i)
```

**Output:**

```
0
1
2
3
4
```

##### **`while` Loops**

Executes as long as a condition is true.

**Syntax:**

```python
while condition:
    # code block
```

**Example:**

```python
count = 0
while count < 5:
    print(count)
    count += 1
```

**Output:**

```
0
1
2
3
4
```

##### **Loop Control Statements**

- **`break`**: Exits the loop immediately.
- **`continue`**: Skips to the next iteration.
- **`pass`**: Does nothing; placeholder.

**Example using `break`:**

```python
for num in range(10):
    if num == 5:
        break
    print(num)
```

**Output:**

```
0
1
2
3
4
```

---

#### **3. Functions**

Functions allow you to encapsulate code into reusable blocks.

**Defining Functions:**

```python
def function_name(parameters):
    # code block
    return value
```

**Example:**

```python
def greet(name):
    return f"Hello, {name}!"

print(greet("Alice"))
```

**Output:**

```
Hello, Alice!
```

**Parameters and Arguments:**

- **Parameters** are variables in the function definition.
- **Arguments** are values passed when calling the function.

**Example:**

```python
def add(a, b):
    return a + b

result = add(5, 3)
print(result)
```

**Output:**

```
8
```

**Variable Scope:**

- **Local Variables**: Defined within a function.
- **Global Variables**: Defined outside all functions.

**Example:**

```python
x = 10  # Global variable

def my_function():
    x = 5  # Local variable
    print("Inside function:", x)

my_function()
print("Outside function:", x)
```

**Output:**

```
Inside function: 5
Outside function: 10
```

---

#### **4. Data Collections**

##### **Lists**

Ordered, mutable collections.

**Example:**

```python
fruits = ["apple", "banana", "cherry"]
fruits.append("orange")
print(fruits)
```

**Output:**

```
['apple', 'banana', 'cherry', 'orange']
```

**Common List Methods:**

- `append()`
- `remove()`
- `pop()`
- `sort()`

##### **Tuples**

Ordered, immutable collections.

**Example:**

```python
coordinates = (10, 20)
print(coordinates)
```

**Output:**

```
(10, 20)
```

##### **Dictionaries**

Unordered collections of key-value pairs.

**Example:**

```python
student = {"name": "Alice", "age": 25}
print(student["name"])
```

**Output:**

```
Alice
```

##### **Sets**

Unordered collections of unique elements.

**Example:**

```python
unique_numbers = {1, 2, 3, 2, 1}
print(unique_numbers)
```

**Output:**

```
{1, 2, 3}
```
