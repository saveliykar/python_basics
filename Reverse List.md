tags:
[[Python]]; [[Programming]]

``` python


```
tags:
[[Python – For and While]]

``` python

#list in reverse order  
n = int(input("Enter the number of elements: "))  
number_list = []  
  
for i in range(n):  
    element = int(input("Enter element {}: ".format(i + 1)))  
    number_list.append(element)  
  
number_list.reverse()  
  
def main():  
    for number in number_list:  
       print(number)  
  
  
number_list.reverse()  
  
main()
```
