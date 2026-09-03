# NumPy Linear Algebra Lab 1

> **Course project** — Applied Linear Algebra, Ferdowsi University of Mashhad, Fall 2024

A Jupyter notebook implementing core linear algebra algorithms from scratch with NumPy,
then applying them to image and video manipulation.

## Contents

- **NumPy fundamentals** — array creation, arithmetic, slicing, and the standard dtypes.
- **Gaussian elimination from scratch** — row-swap, row-sum, and row-scale implemented as
  left-multiplications by elementary matrices, composed into a full `gaussian_elimination`
  routine, row-echelon form (`to_ref`), and back substitution to solve `Ax = b`.
- **Matrix inverse** — computed via Gauss-Jordan elimination on an augmented `[A | I]` matrix.
- **LU decomposition with partial pivoting** — decomposes `A` into `PA = LU`, used to compute
  a determinant in `O(n)` from the triangular factors instead of cofactor expansion.
- **Color grading** — 3×3 matrices applied to every pixel's `(r, g, b)` vector to isolate
  channels, swap channels, and convert to grayscale (average and luminosity-weighted) and
  sepia.
- **Video motion tracking** — frame differencing (against the first frame, and against the
  previous frame) and absolute differencing to highlight motion between video frames using
  OpenCV.
- **3D linear transformations** — rotation, scaling, and translation (via homogeneous
  coordinates) applied to a cube's vertices, with an interactive `ipywidgets` slider demo.

## Tech stack

Python, NumPy, Matplotlib, OpenCV (`cv2`), ipywidgets.

## Running it

Requires a local `images/` folder (with a sample image) and `videos/` folder (with a sample
clip) alongside the notebook, since a few cells load `images/bear.jpg` and
`videos/walking.mp4` — these sample assets aren't included here. Open `lab1.ipynb` in
Jupyter and run top to bottom.
