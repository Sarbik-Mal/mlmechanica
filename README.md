# MLMechanica

[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue)]()
[![License](https://img.shields.io/badge/license-MIT-green)]()
[![Status](https://img.shields.io/badge/status-active-success)]()

**Machine Learning, Unveiled.**

`mlmechanica` is a custom Machine Learning library built from scratch in Python.  
Unlike traditional libraries that treat models as "black boxes," MLMechanica is designed to be a **Glass Box**—offering complete transparency into mathematical operations, internal states, and iterative steps of every algorithm.

It is strictly educational, optimized for clarity and understanding rather than production speed.

---

## 🚀 Key Features

- **Transparency First**  
  Enable `calculation=True` to see every matrix multiplication, gradient update, and intermediate derivation logged to the console in real time.

- **Pure Python & NumPy**  
  Uses only NumPy for linear algebra, avoiding high-level abstractions so the math is fully visible.

- **Self-Documenting Models**  
  Every class exposes a `model_analysis()` method that returns the mathematical derivation and theory behind the algorithm.

- **Instant Demos**  
  Built-in static `demo()` methods let you run smoke tests and view results without writing setup code.

---

## 📦 Installation

Install directly from PyPI:

```bash
pip install mlmechanica
```

---

## ⚡ Quick Start

### 1. Run a Quick Demo

```python
from mlmechanica.regression.linear import SimpleLinearRegression

SimpleLinearRegression.demo()
```

---

### 2. Custom Usage with Calculation Mode

```python
import numpy as np
from mlmechanica.regression.linear import MultipleLinearRegression

X = np.array([[1, 2], [2, 3], [3, 4], [4, 5]])
y = np.array([2, 3, 4, 5])

model = MultipleLinearRegression(calculation=True)
model.fit(X, y)

pred = model.predict(np.array([[5, 6]]))
print(f"Prediction: {pred}")
```

---

## 📚 Supported Models

| Module | Class | Description |
|------|------|-------------|
| **Simple Linear** | `SimpleLinearRegression` | Univariate regression using closed-form OLS derivation |
| **Multiple Linear** | `MultipleLinearRegression` | Multivariate regression using the Normal Equation |
| **Lasso** | `LassoRegression` | L1 regularization via coordinate descent |
| **Ridge** | `RidgeRegression` | L2 regularization with multiple solvers |

---

## 🧠 Model Analysis

```python
from mlmechanica.regression.linear import SimpleLinearRegression

model = SimpleLinearRegression()
print(model.model_analysis("derivation"))
```

---

## 🤝 Contributing

1. Fork the project  
2. Create a feature branch  
3. Commit your changes  
4. Push to the branch  
5. Open a Pull Request  

---

## 📄 License

MIT License. See `LICENSE` for details.
