# Day 2: Control Structures and Data Collections

Welcome to Day 2 of our 5-day Python course! Today, we'll delve deeper into programming by exploring control structures and data collections. Understanding these concepts will allow you to write more complex and efficient programs that can make decisions and handle collections of data.

---

## Lecture Notes

### 1. Conditional Statements

Conditional statements allow your program to execute certain pieces of code based on specific conditions. They are fundamental to controlling the flow of your program.

#### Syntax

```python
if condition:
    # code block executed if condition is true
elif another_condition:
    # code block executed if the previous condition was false and this condition is true
else:
    # code block executed if all above conditions are false
```

#### Explanation

- **`if` Statement**: Checks a condition. If it's `True`, the indented code block under it executes.
- **`elif` (else if) Statement**: Checks another condition if the previous `if` condition was `False`.
- **`else` Statement**: Executes if none of the above conditions are `True`.

#### Example

```python
age = 18

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

#### Nested Conditions

You can place conditional statements inside other conditional statements.

```python
score = 85

if score >= 60:
    print("You passed!")
    if score >= 90:
        print("Excellent!")
    elif score >= 80:
        print("Very Good!")
    else:
        print("Good job!")
else:
    print("You failed.")
```

**Output:**

```
You passed!
Very Good!
```

#### Logical Operators in Conditions

- **`and`**: True if both conditions are true.
- **`or`**: True if at least one condition is true.
- **`not`**: Inverts the truth value.

**Example:**

```python
is_student = True
age = 20

if is_student and age < 25:
    print("You are eligible for a student discount.")
```

**Output:**

```
You are eligible for a student discount.
```

---

### 2. Loops

Loops are used to execute a block of code repeatedly.

#### `for` Loops

Used to iterate over a sequence (such as a list, tuple, string, or range).

##### Syntax

```python
for variable in sequence:
    # code block
```

##### Example 1: Iterating Over a Range

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

- **Note:** `range(5)` generates numbers from 0 to 4.

##### Example 2: Iterating Over a List

```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```

**Output:**

```
apple
banana
cherry
```

#### `while` Loops

Executes as long as a condition is true.

##### Syntax

```python
while condition:
    # code block
```

##### Example

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

- **Note:** Be careful to update the condition variable (`count += 1`) to avoid infinite loops.

---

### 3. Loop Control Statements

Control the execution of loops beyond their normal sequence.

#### `break` Statement

- Exits the loop immediately.

**Example:**

```python
for number in range(10):
    if number == 5:
        break
    print(number)
```

**Output:**

```
0
1
2
3
4
```

#### `continue` Statement

- Skips the current iteration and moves to the next one.

**Example:**

```python
for number in range(5):
    if number == 3:
        continue
    print(number)
```

**Output:**

```
0
1
2
4
```

- **Note:** Number `3` is skipped.

#### `pass` Statement

- Does nothing; it's a null operation.

**Example:**

```python
for letter in 'Python':
    if letter == 'h':
        pass  # Placeholder for future code
    print('Current Letter:', letter)
```

**Output:**

```
Current Letter: P
Current Letter: y
Current Letter: t
Current Letter: h
Current Letter: o
Current Letter: n
```

---

### 4. Data Collections

Python provides several built-in data structures to store collections of data.

#### 4.1 Lists

- Ordered, mutable collections of items.
- Items can be of different data types.

##### Creating a List

```python
fruits = ["apple", "banana", "cherry"]
```

##### Accessing Items

```python
print(fruits[0])      # Outputs: apple
print(fruits[-1])     # Outputs: cherry
```

##### List Methods

- **`append(item)`**: Adds an item to the end.

  ```python
  fruits.append("orange")
  print(fruits)  # ['apple', 'banana', 'cherry', 'orange']
  ```

- **`remove(item)`**: Removes the first occurrence of an item.

  ```python
  fruits.remove("banana")
  print(fruits)  # ['apple', 'cherry', 'orange']
  ```

- **`pop(index)`**: Removes and returns item at index. Defaults to the last item.

  ```python
  item = fruits.pop()
  print(item)    # orange
  print(fruits)  # ['apple', 'cherry']
  ```

- **`sort()`**: Sorts the list in ascending order.

  ```python
  numbers = [3, 1, 4, 1, 5]
  numbers.sort()
  print(numbers)  # [1, 1, 3, 4, 5]
  ```

##### Slicing Lists

```python
print(fruits[0:2])  # Outputs: ['apple', 'cherry']
```

---

#### 4.2 Tuples

- Ordered, immutable collections.
- Defined using parentheses `()`.

##### Creating a Tuple

```python
coordinates = (10, 20)
```

##### Accessing Items

```python
print(coordinates[0])  # Outputs: 10
```

##### Tuple Packing and Unpacking

```python
# Packing
person = ("Alice", 25)

# Unpacking
name, age = person
print(name)  # Alice
print(age)   # 25
```

---

#### 4.3 Dictionaries

- Unordered collections of key-value pairs.
- Keys must be unique and immutable.

##### Creating a Dictionary

```python
student = {"name": "Alice", "age": 25}
```

##### Accessing Values

```python
print(student["name"])  # Outputs: Alice
```

##### Adding and Updating Items

```python
student["grade"] = "A"  # Adds a new key-value pair
student["age"] = 26     # Updates the value of an existing key
```

##### Removing Items

```python
del student["age"]      # Removes the key-value pair for 'age'
```

##### Iterating Over Dictionaries

```python
for key, value in student.items():
    print(f"{key}: {value}")
```

**Output:**

```
name: Alice
grade: A
```

---

#### 4.4 Sets

- Unordered collections of unique elements.
- Defined using curly braces `{}` or the `set()` function.

##### Creating a Set

```python
unique_numbers = {1, 2, 3, 2, 1}
print(unique_numbers)  # Outputs: {1, 2, 3}
```

##### Set Operations

- **Union (`|`):**

  ```python
  set_a = {1, 2, 3}
  set_b = {3, 4, 5}
  print(set_a | set_b)  # Outputs: {1, 2, 3, 4, 5}
  ```

- **Intersection (`&`):**

  ```python
  print(set_a & set_b)  # Outputs: {3}
  ```

- **Difference (`-`):**

  ```python
  print(set_a - set_b)  # Outputs: {1, 2}
  ```

---

### 5. Exercises

#### Exercise 1: Prime Number Checker

**Task:** Write a program to check if a number is prime.

**Solution:**

```python
# Prime Number Checker

num = int(input("Enter a number: "))

# Prime numbers are greater than 1
if num > 1:
    # Check for factors
    for i in range(2, num):
        if (num % i) == 0:
            print(f"{num} is not a prime number.")
            print(f"It is divisible by {i}.")
            break
    else:
        print(f"{num} is a prime number.")
else:
    print(f"{num} is not a prime number.")
```

**Sample Interaction:**

```
Enter a number: 13
13 is a prime number.
```

---

#### Exercise 2: To-Do List Application

**Task:** Create a program that allows the user to add, view, and remove tasks from a to-do list.

**Solution:**

```python
# Simple To-Do List Application

to_do_list = []

def display_menu():
    print("\nTo-Do List Menu:")
    print("1. View To-Do List")
    print("2. Add Task")
    print("3. Remove Task")
    print("4. Exit")

def view_list():
    if not to_do_list:
        print("Your to-do list is empty.")
    else:
        print("\nYour To-Do List:")
        for idx, task in enumerate(to_do_list, 1):
            print(f"{idx}. {task}")

def add_task():
    task = input("Enter the task: ")
    to_do_list.append(task)
    print(f"'{task}' has been added to your to-do list.")

def remove_task():
    view_list()
    if to_do_list:
        try:
            task_num = int(input("Enter the task number to remove: "))
            removed_task = to_do_list.pop(task_num - 1)
            print(f"'{removed_task}' has been removed from your to-do list.")
        except (IndexError, ValueError):
            print("Invalid task number.")

while True:
    display_menu()
    choice = input("Enter your choice (1-4): ")
    if choice == '1':
        view_list()
    elif choice == '2':
        add_task()
    elif choice == '3':
        remove_task()
    elif choice == '4':
        print("Goodbye!")
        break
    else:
        print("Invalid choice. Please select from 1 to 4.")
```

**Sample Interaction:**

```
To-Do List Menu:
1. View To-Do List
2. Add Task
3. Remove Task
4. Exit
Enter your choice (1-4): 2
Enter the task: Finish homework
'Finish homework' has been added to your to-do list.

To-Do List Menu:
1. View To-Do List
2. Add Task
3. Remove Task
4. Exit
Enter your choice (1-4): 1

Your To-Do List:
1. Finish homework

To-Do List Menu:
1. View To-Do List
2. Add Task
3. Remove Task
4. Exit
Enter your choice (1-4): 4
Goodbye!
```

---

#### Exercise 3: Word Frequency Counter

**Task:** Write a script that counts the frequency of each word in a given string.

**Solution:**

```python
# Word Frequency Counter

text = input("Enter a string: ")

# Convert to lowercase to make counting case-insensitive
text = text.lower()

# Remove punctuation (optional)
import string
for char in string.punctuation:
    text = text.replace(char, "")

words = text.split()

word_count = {}

for word in words:
    word_count[word] = word_count.get(word, 0) + 1

# Display word frequencies
print("\nWord Frequencies:")
for word, count in word_count.items():
    print(f"{word}: {count}")
```

**Sample Interaction:**

```
Enter a string: This is a test. This test is only a test.

Word Frequencies:
this: 3
is: 2
a: 2
test: 3
only: 1
```

---

## Additional Examples and Tips

### Using `elif` Statements

You can have multiple `elif` statements to check various conditions.

```python
score = 75

if score >= 90:
    grade = 'A'
elif score >= 80:
    grade = 'B'
elif score >= 70:
    grade = 'C'
elif score >= 60:
    grade = 'D'
else:
    grade = 'F'

print(f"Your grade is {grade}.")
```

**Output:**

```
Your grade is C.
```

---

### Nested Loops

Loops inside loops can be used for iterating over multi-dimensional data structures.

```python
# Multiplication table

for i in range(1, 6):
    for j in range(1, 6):
        product = i * j
        print(f"{product}\t", end="")
    print()  # Newline after each row
```

**Output:**

```
1	2	3	4	5	
2	4	6	8	10	
3	6	9	12	15	
4	8	12	16	20	
5	10	15	20	25	
```

---

### List Comprehensions (Advanced)

A concise way to create lists.

```python
# Create a list of squares from 1 to 10
squares = [x ** 2 for x in range(1, 11)]
print(squares)
```

**Output:**

```
[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```

---

### Common Mistakes and How to Avoid Them

1. **Forgetting to Initialize Loop Variables:**

   ```python
   count = 0  # Ensure count is initialized before the loop
   ```

2. **Infinite Loops:**

   Ensure that the loop condition will eventually become `False`.

   ```python
   while True:
       # Without a break or a condition that becomes False, this is infinite
   ```

3. **Modifying a List While Iterating Over It:**

   This can lead to unexpected behavior.

   **Incorrect:**

   ```python
   numbers = [1, 2, 3, 4, 5]
   for num in numbers:
       if num % 2 == 0:
           numbers.remove(num)
   print(numbers)  # Outputs: [1, 3, 5]
   ```

   **Correct Approach:**

   ```python
   numbers = [1, 2, 3, 4, 5]
   numbers = [num for num in numbers if num % 2 != 0]
   print(numbers)  # Outputs: [1, 3, 5]
   ```

4. **KeyError in Dictionaries:**

   Accessing a key that doesn't exist.

   ```python
   student = {"name": "Alice"}
   print(student["age"])  # KeyError: 'age'
   ```

   **Solution:** Use `get()` method with a default value.

   ```python
   print(student.get("age", "Unknown"))  # Outputs: Unknown
   ```

---

## Wrap-Up and Q&A

- **Recap:**

  - Learned about conditional statements to make decisions.
  - Explored loops to repeat code efficiently.
  - Understood loop control statements to fine-tune loop execution.
  - Worked with data collections to store and manipulate groups of data.
  - Practiced with exercises to apply the concepts.

- **Questions to Consider:**

  - How can you use loops to process data in a list or dictionary?
  - What are some real-world scenarios where conditional statements are useful?
  - How do data collections enhance the way you store and access data?

---

## Next Steps

- **Practice:** Try modifying the exercises or creating your own programs using these concepts.
- **Preview of Day 3:** We'll explore functions and modules, which will help you write reusable and organized code.

---

Looking forward to continuing our Python journey together!
