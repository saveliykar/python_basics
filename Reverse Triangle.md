tags:
[[Python]]; [[Programming]]

``` python


```
tags:
[[Python – For and While]]

``` python
def numbers_before():  
    n = int(input('Up to which number should I print the numbers: '))  
    for i in range (n, 0, -1):  
       for j in range(i, 0, -1):  
          print(j, end=' ')  
       print('')  
  
  
  
numbers_before()

```
