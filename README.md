# QR Factorization

This project implements QR factorization using Householder reflections and compares the results with NumPy's built-in `np.linalg.qr` function.

## Features

- **QR Factorization**: Custom implementation using Householder reflections
- **Matrix Comparison**: Function to compare matrices with numerical tolerance
- **Pascal Matrix Generator**: Creates Pascal matrices for testing
- **Verification**: Compares custom implementation with NumPy's implementation

## Code Structure

### Main Functions

#### `qr(A):` Performs QR factorization.

#### `compare_matrices_with_tolerance(A, B, tolerance=1e-10):` Compares two matrices with a specified tolerance.

#### `pascal_matrix(n):` Generates an n x n Pascal matrix.


## Example Usage

```python
# Generate a 6x6 Pascal matrix
A = pascal_matrix(6)

# Perform QR factorization
Q, R = qr(A)

# Compare with NumPy's implementation
Q_numpy, R_numpy = np.linalg.qr(A)
compare_matrices_with_tolerance(Q, Q_numpy)
compare_matrices_with_tolerance(R, R_numpy)

# Reconstruct original matrix
A_reconstructed = Q @ R