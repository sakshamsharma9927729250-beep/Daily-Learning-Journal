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