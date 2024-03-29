# Formula of power sum 
**This algorithm helps to generate the sum equation of the power function:** 

![](https://latex.codecogs.com/svg.image?\LARGE&space;\color{White}f(x)=\sum\limits_{x&space;=&space;1}^x&space;{{x^n}}=1^n&plus;2^n&plus;3^n&plus;\cdots&space;&plus;x^n&space;&space;,\left&space;(&space;n\geq&space;0&space;,\in&space;\mathbb{N}&space;\right&space;))

![](https://latex.codecogs.com/png.image?\inline&space;\huge&space;\dpi{80}\color{white}&space;f(x):&space;\textrm{the&space;power&space;function&space;of&space;n&space;degree}&space;&space;)

![](https://latex.codecogs.com/png.image?\inline&space;\huge&space;\dpi{80}\color{white}&space;n:&space;\textrm{degree&space;of&space;function}&space;&space;)
## Usage
```python
usage: posum.py [-h] [-d DEGREE] [-v] [-s SHOW]

optional arguments:
  -h, --help            show this help message and exit
  -d DEGREE, --degree DEGREE
  -v, --version         show version
  -s SHOW, --show SHOW  only showing the formula (f), triagle matrix (m) or both (b)[default]?
```

If we want to know the equation of the sum function of the nth power, we run the python script and enter the degree n of the sum function. 
```python
python posum.py -d <the degree n>
```
The result consists of the power sum formula of n degree and the triangle matrix. Besides, wanting to show either. Let's use the argument -s

## Example
Need help to use
```python
python posum.py -h
```

To show version of algorithm.
```python
python posum.py -v
```
For example, when we want to find the sum function of the power of 6, we run the command and enter the degree of the function as 6.
```python
#input
python posum.py -d 6

#output
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
So the equation sum of the power of the sixth power has the form:

![](https://latex.codecogs.com/svg.image?\color{White}f(x)=\sum_{x=1}^{x}x^6=\frac{1}{42}.x^{1}-\frac{1}{6}.x^{3}&plus;\frac{1}{2}.x^{5}&plus;\frac{1}{2}.x^{6}&plus;\frac{1}{7}.x^{7})

## The principle of the algorithm
The algorithm works by forming a triangular matrix with each value of the matrix being a coefficient of the sum equation. The coefficients of the equation of degree n are the values of the n-th row of the matrix.
Values of the matrix is calculated according to the system of equations:

$$\left\{ \begin{array}{l}
{a_{01}} = 1\\
{a_{ij}} = \frac{i}{j} \times {a_{_{(i - 1)(j - 1)}}} {\rm{  ,}}\forall i\ge 1,\forall j\ge 2\\
\sum\limits_{k = 1}^j {{a_{ik}} = 1{\rm{  ,}}\forall i,j} 
\end{array} \right.$$

## Application

- [Create sum formula of polinomial functions](https://github.com/Truongphi20/sumfor) 
