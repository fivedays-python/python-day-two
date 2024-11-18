### **Exercises**

#### **Exercise 1: Prime Number Checker**

**Objective:** Write a program that checks if a number entered by the user is a prime number.

**Instructions:**

1. Prompt the user to enter a positive integer.
2. Use a function to check if the number is prime.
3. Print whether the number is prime or not.

**Solution:**

```python
def is_prime(number):
    if number <= 1:
        return False
    for i in range(2, number):
        if number % i == 0:
            return False
    return True

num = int(input("Enter a positive integer: "))
if is_prime(num):
    print(f"{num} is a prime number.")
else:
    print(f"{num} is not a prime number.")
```

---

#### **Exercise 2: To-Do List Application**

**Objective:** Create a program that allows the user to add, view, and remove tasks from a to-do list.

**Instructions:**

1. Use a list to store tasks.
2. Implement functions for adding, viewing, and removing tasks.
3. Provide a menu for user interaction.

**Solution:**

```python
def display_menu():
    print("\nTo-Do List Menu:")
    print("1. View Tasks")
    print("2. Add Task")
    print("3. Remove Task")
    print("4. Exit")

def view_tasks(tasks):
    if not tasks:
        print("Your to-do list is empty.")
    else:
        print("\nYour To-Do List:")
        for idx, task in enumerate(tasks, 1):
            print(f"{idx}. {task}")

def add_task(tasks):
    task = input("Enter a new task: ")
    tasks.append(task)
    print(f"'{task}' added to your to-do list.")

def remove_task(tasks):
    view_tasks(tasks)
    if tasks:
        try:
            task_num = int(input("Enter the number of the task to remove: "))
            removed_task = tasks.pop(task_num - 1)
            print(f"'{removed_task}' has been removed.")
        except (IndexError, ValueError):
            print("Invalid task number.")

tasks = []

while True:
    display_menu()
    choice = input("Enter your choice (1-4): ")
    if choice == '1':
        view_tasks(tasks)
    elif choice == '2':
        add_task(tasks)
    elif choice == '3':
        remove_task(tasks)
    elif choice == '4':
        print("Goodbye!")
        break
    else:
        print("Invalid choice. Please select from 1 to 4.")
```

---

#### **Exercise 3: Word Frequency Counter**

**Objective:** Write a script that counts the frequency of each word in a given string.

**Instructions:**

1. Prompt the user to enter a string.
2. Remove punctuation and convert the string to lowercase.
3. Split the string into words.
4. Use a dictionary to count word frequencies.
5. Display the word frequencies.

**Solution:**

```python
import string

def count_word_frequency(text):
    # Remove punctuation and convert to lowercase
    text = text.lower()
    text = text.translate(str.maketrans('', '', string.punctuation))
    words = text.split()

    word_counts = {}
    for word in words:
        word_counts[word] = word_counts.get(word, 0) + 1

    return word_counts

input_text = input("Enter a string: ")
frequencies = count_word_frequency(input_text)

print("\nWord Frequencies:")
for word, count in frequencies.items():
    print(f"{word}: {count}")
```
