tags:
[[Python]]; [[Programming]]

``` python


```
tags:
[[Python – For and While]]

``` python
n = int(input('reverse a number: '))  
reverse_n = 0  
while n > 0:  
    reminder = n % 10  
    reverse_n = reverse_n*10 + reminder  
    n = n // 10  
  
print(reverse_n)

```
