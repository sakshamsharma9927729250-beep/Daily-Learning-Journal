## 📅 November 1, 2026 — Python Unit Testing with unittest

### 🎯 Today's Objective
Learn how to write automated tests in Python to verify program behaviour and catch errors early.

### 💻 Key Concepts

- **Unit Testing:** Testing individual functions or components independently.
- **Test Case:** A specific scenario used to verify expected behaviour.
- **Assertion:** A check that compares actual output with expected output.
- **Test Suite:** A collection of test cases.
- **Test Runner:** A tool that executes tests and reports results.

### 🛠️ Practical Implementation

```python
import unittest

def calculate_total(price, quantity):
    return price * quantity

class TestCalculator(unittest.TestCase):

    def test_total(self):
        self.assertEqual(calculate_total(100, 3), 300)

    def test_zero_quantity(self):
        self.assertEqual(calculate_total(100, 0), 0)

if __name__ == "__main__":
    unittest.main()
```

### 🧠 Key Learning
Automated testing improves code reliability and makes future modifications safer. Instead of manually checking every result, developers can run test cases repeatedly.

### 🚀 Next Steps
- Explore pytest.
- Practise testing invalid inputs.
- Add unit tests to existing Python projects.
- Learn test-driven development fundamentals.

**Skills:** Python, Unit Testing, unittest, Software Quality Assurance  
**Contribution Type:** Technical Learning & Code Practice  
**Date:** November 1, 2026

## 📅 November 3, 2026 — Python Context Managers & File Handling

### 🎯 Today's Objective
Understand Python context managers and how they help manage resources safely while working with files.

### 💻 Key Concepts

- **Context Manager:** An object that manages resource setup and cleanup automatically.
- **`with` Statement:** Provides a clean way to work with resources.
- **`__enter__()`:** Runs when entering a context.
- **`__exit__()`:** Runs when leaving a context.
- **Automatic Cleanup:** Ensures resources such as files are properly closed.

### 🛠️ Practical Implementation

```python
from pathlib import Path

file_path = Path("learning_notes.txt")

with file_path.open("w", encoding="utf-8") as file:
    file.write("Learning Python Context Managers")

with file_path.open("r", encoding="utf-8") as file:
    content = file.read()

print(content)
```

### 🧠 Key Learning
The `with` statement makes resource management safer and cleaner. It automatically handles file closure, even if an exception occurs inside the context.

### 🚀 Practical Tasks
- Create a text file using `pathlib`.
- Write and read data using a context manager.
- Handle file-related exceptions.
- Explore custom context managers.

**Skills:** Python, File Handling, Context Managers, pathlib  
**Contribution Type:** Python Technical Learning & Practice  
**Date:** November 3, 2026

## 📅 November 5, 2026 — Python Generators & Yield

### 🎯 Today's Objective
Understand Python generators and how they produce values one at a time instead of storing an entire sequence in memory.

### 💻 Key Concepts

- **Generator:** A special iterator that produces values lazily.
- **`yield`:** Returns a value while preserving the function's execution state.
- **`next()`:** Retrieves the next value from an iterator.
- **Lazy Evaluation:** Values are generated only when requested.
- **`StopIteration`:** Indicates that an iterator has no more values.

### 🛠️ Practical Implementation

```python
def number_generator(limit):
    number = 1

    while number <= limit:
        yield number
        number += 1

numbers = number_generator(5)

for value in numbers:
    print(value)
```

### Expected Output

```text
1
2
3
4
5
```

### 🧠 Key Learning
Generators are useful when working with large datasets or streams of information because they produce values on demand rather than building the complete sequence in memory.

### 🚀 Practice Tasks
1. Create a generator for even numbers.
2. Generate a multiplication table using `yield`.
3. Create a Fibonacci number generator.
4. Compare a normal function returning a list with a generator function.

**Skills:** Python, Generators, Iterators, Lazy Evaluation  
**Contribution Type:** Python Technical Learning & Practice  
**Date:** November 5, 2026

## November 6, 2026 — Python Exception Handling

### Today's Focus
Practiced Python exception handling and learned how to make user input more reliable.

### Key Learnings
- Understood the purpose of `try` and `except`.
- Used `ValueError` to handle invalid numeric input.
- Applied input validation to reject non-positive numbers.
- Used a loop to allow users to retry invalid input.
- Improved the reliability of a simple command-line program.

### Practical Implementation
Created a positive-number input program that:
- Accepts valid numeric input.
- Handles invalid text without crashing.
- Rejects zero and negative values.
- Repeats the input process until valid data is received.

### Key Takeaway
Reliable programs should handle unexpected input gracefully instead of crashing.

**Today's Progress:** Practiced exception handling, input validation, and writing more robust Python code.

## November 7, 2026 — Python JSON File Handling

### Today's Focus
Practiced storing and retrieving structured data using Python's JSON module.

### Key Learnings
- Understood JSON data format.
- Practiced `json.dump()` to write Python data into a JSON file.
- Used `json.load()` to retrieve stored data.
- Learned how to handle missing files using `FileNotFoundError`.
- Explored basic data persistence in Python.

### Practical Implementation
Created a student record storage program that:
- Stores student names and marks.
- Saves records inside a JSON file.## November 9, 2026 — Python CSV File Handling

### Today's Focus
Practiced reading and writing structured tabular data using Python's CSV module.

### Key Learnings
- Understood the purpose of CSV files.
- Practiced using Python's `csv` module.
- Used `csv.DictWriter()` to write records.
- Used `writeheader()` and `writerows()` to store structured data.
- Used `csv.DictReader()` to read records.
- Explored how CSV files can be used for simple data storage.

### Practical Implementation
Created a student record management script that:
- Stores student names and marks.
- Writes records into a CSV file.
- Reads saved records from the file.
- Displays each student's information.

### Key Takeaway
CSV handling is useful when working with structured tabular data and exchanging data between applications.

**Today's Progress:** Practiced CSV reading, writing, and structured data management.
- Reads stored records from the file.
- Handles a missing JSON file gracefully.

### Key Takeaway
File handling allows Python applications to preserve data beyond a single program execution.

**Today's Progress:** Practiced JSON serialization, deserialization, and persistent data storage.

## November 9, 2026 — Python CSV File Handling

### Today's Focus
Practiced reading and writing structured tabular data using Python's CSV module.

### Key Learnings
- Understood the purpose of CSV files.
- Practiced using Python's `csv` module.
- Used `csv.DictWriter()` to write records.
- Used `writeheader()` and `writerows()` to store structured data.
- Used `csv.DictReader()` to read records.
- Explored how CSV files can be used for simple data storage.

### Practical Implementation
Created a student record management script that:
- Stores student names and marks.
- Writes records into a CSV file.
- Reads saved records from the file.
- Displays each student's information.

### Key Takeaway
CSV handling is useful when working with structured tabular data and exchanging data between applications.

**Today's Progress:** Practiced CSV reading, writing, and structured data management.

📚 Learning: Idempotency

Idempotency is a property where executing the same operation multiple times produces the same final result as executing it once.

It is important in APIs, payment systems, database operations, and retry mechanisms to prevent duplicate actions.

Example: Updating a user's status to "active" multiple times should not create multiple users or duplicate records.

📚 Learning: Race Conditions

A race condition occurs when multiple processes or threads access or modify shared resources simultaneously, causing unpredictable results.

It can lead to incorrect counters, inconsistent data, and unexpected application behavior.

Solutions include locks, synchronization, atomic operations, and transaction management.

📚 Learning: Caching

Caching stores frequently accessed data temporarily to reduce response time and unnecessary database queries.

Cache invalidation is the process of updating or removing stale cached data when the original data changes.

A cache improves performance but requires proper consistency management.

📚 Learning: Time Complexity

Time complexity describes how an algorithm's execution time grows as the input size increases.

Common complexities:
O(1) — Constant
O(log n) — Logarithmic
O(n) — Linear
O(n log n) — Linearithmic
O(n²) — Quadratic

Understanding Big O helps developers select scalable and efficient algorithms.

# Daily Learning Journal — 23 November 2026

## Topic: C Programming – Conditional Logic

### Today's Learning
- Studied conditional statements in C programming.
- Practiced `if`, `if-else`, `else-if` ladder, and nested `if`.
- Understood how conditions control program execution.
- Practiced relational and logical operators.
- Analyzed decision-making flow in programs.

### Technical Concepts
- Conditional branching
- Boolean evaluation
- Relational operators
- Logical operators (`&&`, `||`, `!`)
- Nested decision structures

### Practical Implementation
Implemented conditional programs to:
- Identify even and odd numbers.
- Evaluate conditions using relational operators.
- Categorize marks into grades.
- Apply multiple conditions using nested `if`.

### Key Takeaway
Conditional statements enable programs to make decisions dynamically based on input and logical conditions, forming the foundation of intelligent program flow.

### Progress
Continuing to strengthen C programming fundamentals through logic building, practical implementation, and structured coding practice.

# Day 6 — C Programming Learning Log
**Date:** 24 November 2026

### Topics Covered
- Introduction to functions in C
- Library functions and user-defined functions
- Function declaration, definition and calling
- Parameters and arguments
- Return types and return values
- Code reusability and modular programming

### Practical Work
- Created a user-defined addition function.
- Passed two integer arguments to a function.
- Returned the calculated result to `main()`.
- Practiced breaking program logic into reusable functions.

### Key Learning
Functions make programs modular, reusable, easier to debug and maintain. Instead of writing the same logic repeatedly, we can create a function and call it whenever required.

### Learning Status
Completed today's C programming practice and strengthened my understanding of modular programming and function-based logic.

#C #Programming #LearningJourney #Functions #GitHub #CodeDaily

