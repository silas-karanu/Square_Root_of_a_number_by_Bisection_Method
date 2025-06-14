# Square_Root_of_a_number_by_Bisection_Method
Exploring the numerical method of bisection to find the square root of a number by iteratively narrowing down the possible range of values that contain the square root.

# 📐 Square Root Bisection Method (Python)

This project implements a numerical method to approximate the square root of a number using the **bisection algorithm**. It avoids built-in math functions and instead demonstrates an iterative approach with customizable precision and iteration limits.

---

## ✅ Features

- Calculates square roots of non-negative real numbers
- Uses the **bisection method** for fast convergence
- Supports custom tolerance and iteration limit
- Handles special cases like `0` and `1` directly
- Raises meaningful errors for invalid input (e.g., negative numbers)

---

## 🧠 How It Works

1. **For square_target 0 or 1**, the result is returned immediately.
2. **For all other non-negative values**, the function uses the **bisection method**:
   - It starts with a search interval `[0, max(1, square_target)]`
   - Repeatedly halves the interval
   - Stops when the square of the midpoint is within a small tolerance of the target

---

## 📌 Function Signature

```python
def square_root_bisection(square_target, tolerance=1e-7, max_iterations=100):
```

---
## Parameters:
- `square_target` (float): The number to find the square root of

- `tolerance` (float, optional): The precision of the approximation (default: 1e-7)

- `max_iterations` (int, optional): Max iterations before exiting (default: 100)

---

## 🧪 Example Usage
```python

>>> square_root_bisection(25)
The square root of 25 is approximately 5.000000000000001

>>> square_root_bisection(2)
The square root of 2 is approximately 1.4142135679721832
```
---

## ❗ Error Handling
- Raises `ValueError` if the input number is negative:
```python
>>> square_root_bisection(-4)
ValueError: Square root of negative number is not defined in real numbers
```
---

## 🛠 Suggested Improvements
- Add `verbose=False` flag to control printing

- Return more detailed info (`root`, `iterations`, `converged`)

- Refactor to separate logic from I/O

- Use `math.isclose()` for more robust float comparison

- Support small and large float inputs with dynamic tolerance

---

## 📄 License
MIT License. Free to use and modify.
