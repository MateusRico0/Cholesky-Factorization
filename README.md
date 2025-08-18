# Cholesky Decomposition Implementation

This repository contains a Python implementation of the Cholesky decomposition algorithm for positive definite matrices.

## Functions

### `Cholesky(A)`
Performs Cholesky decomposition on matrix A.

**Parameters:**
- `A`: Input matrix (must be symmetric positive definite)

**Returns:**
- `L`: Lower triangular matrix such that A = LLᵀ
- `p`: Flag indicating if matrix is positive definite (0 = yes, 1 = no)

### `Cholesky_validation(A)`
Validates the Cholesky decomposition by comparing with NumPy's built-in implementation.

### `definida_positiva(A)`
Checks if a matrix is positive definite using the Cholesky decomposition.

## Example Usage

```python
import numpy as np

# Define a positive definite matrix
A = np.array([[1, 1, 1], 
              [1, 2, 3], 
              [1, 3, 6]], dtype=np.float64)

# Perform Cholesky decomposition
L, p = Cholesky(A)

# Validate the result
Cholesky_validation(A)

# Check if matrix is positive definite
definida_positiva(A)