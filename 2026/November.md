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
- Saves records inside a JSON file.
- Reads stored records from the file.
- Handles a missing JSON file gracefully.

### Key Takeaway
File handling allows Python applications to preserve data beyond a single program execution.

**Today's Progress:** Practiced JSON serialization, deserialization, and persistent data storage.