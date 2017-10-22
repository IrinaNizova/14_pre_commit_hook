# Quadratic Equations Solver

pre-commit hook deny perform commit when tests failed

# How to use

Copy file pre-commit in folder .git/hook

# Example of output

## Passed

```bash
git commit
....
----------------------------------------------------------------------
Ran 4 tests in 0.000s

OK
All tests passed
[master cf1552a] fix and add hook
 2 files changed, 2 insertions(+), 2 deletions(-)
 create mode 100644 pre-commit
```

## Failed
```bash
git commit
.E..
======================================================================
ERROR: test_returns_none_for_complex_solution (__main__.QuadraticEquationTestCase)
----------------------------------------------------------------------
Traceback (most recent call last):
  File "tests.py", line 22, in test_returns_none_for_complex_solution
    root1, root2 = get_roots(1, 2, 3)
  File "/home/ira/myfolder/14_pre_commit_hook/quadratic_equation.py", line 6, in get_roots
    root1 = (-b - sqrt(discriminant)) / (2 * a)
ValueError: math domain error

----------------------------------------------------------------------
Ran 4 tests in 0.001s

FAILED (errors=1)
Some tests failed

```

# Project Goals

The code is written for educational purposes. Training course for web-developers - [DEVMAN.org](https://devman.org)
