# Formula of power sum 
**This algorithm helps to generate the sum equation of the power function x^n (with n >= 0)**

## Usage
python sum_eng.py\
Sum formula of x^n (n >= 0): <Enter degree of function (n)>
## Example
```python
python sum_eng.py
Sum formula of x^n (n >= 0): 6
Sum formula of x^ 6 is:  +1/42*x^1+0*x^2-1/6*x^3+0*x^4+1/2*x^5+1/2*x^6+1/7*x^7

Matrix triagle is:

         1      2     3     4    5    6    7

  0      1
  1    1/2    1/2
  2    1/6    1/2   1/3
  3      0    1/4   1/2   1/4
  4  -1/30      0   1/3   1/2  1/5
  5      0  -1/12     0  5/12  1/2  1/6
  6   1/42      0  -1/6     0  1/2  1/2  1/7
```


## The principle of the algorithm
The algorithm works by forming a triangular matrix with each value of the matrix being a coefficient of the sum equation. The coefficients of the equation of degree n are the values of the n-th row of the matrix.

