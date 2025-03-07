tags:
[[Python]]; [[Programming]]

``` python


```
tags:
[[Python – For and While]]

``` python
#list in reverse order  
starting = int(input("choose a starting number: "))  
ending = int(input("choose an ending number: "))  
  
for i in range(starting, ending+1):  
    for j in range(2, i):  
       if (i % j) == 0:  
          break  
    else:  
       print(i)

  
  
#first loop is needed to iterate through original numbers  
#the second loop is needed to iterate the chosen number i through all of the numbers within the given limit
```
