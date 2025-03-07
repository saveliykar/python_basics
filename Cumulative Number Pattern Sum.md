tags:
[[Python]]; [[Programming]]
 [[Python – For and While]]

``` python
num = int(input('choose the base number for our terms (for example, if you choose 3 - sum of 3, 33, 333, etc): '))  
terms = int(input('choose the terms(if you choose 2 - sum of 3, 33): '))  
sum = 0  
counter = 0  
next_num = 0  
while counter < terms:  
    next_num = next_num*10+num  
    sum = sum + next_num  
    counter += 1  
  
print(sum)

```
