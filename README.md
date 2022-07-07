# Formula of power sum 
**This algorithm helps to generate the sum equation of the power function:** 

![](https://latex.codecogs.com/svg.image?\inline&space;\huge&space;\color{white}f(x)=\sum\limits_{x&space;=&space;1}^x&space;{{x^n}}&space;&space;,\left&space;(&space;n\geq&space;0&space;,\in&space;\mathbb{N}&space;\right&space;))

![](https://latex.codecogs.com/png.image?\inline&space;\huge&space;\dpi{80}\color{white}&space;f(x):&space;\textrm{the&space;power&space;function&space;of&space;n&space;degree}&space;&space;)

![](https://latex.codecogs.com/png.image?\inline&space;\huge&space;\dpi{80}\color{white}&space;n:&space;\textrm{degree&space;of&space;function}&space;&space;)
## Usage
If we want to know the equation of the sum function of the nth power, we run the python script and enter the degree n of the sum function.
```python
python sum_eng.py
Sum formula of x^n (n >= 0): <Enter degree of function (n)>
```
## Example
For example, when we want to find the sum function of the power of 6, we run the command and enter the degree of the function as 6.
```python
#input
python sum_eng.py
Sum formula of x^n (n >= 0): 6

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

<a href="url"><img src="https://latex.codecogs.com/png.image?\inline&space;\huge&space;\dpi{200}\color{white}&space;\left\{&space;\begin{array}{l}{a_{ij}}&space;=&space;\frac{j}{i}&space;\times&space;{a_{(i&space;-&space;1)(j&space;-&space;1)}}\\{a_{10}}&space;=&space;1\\\sum\limits_{k&space;=&space;1}^i&space;{{a_{kj}}{\rm{&space;=&space;&space;1&space;&space;,}}\forall&space;{\rm{i,j}}}&space;\end{array}&space;\right.\" align="center" height="180" width="300" ></a>


