tags:
[[Python]]; [[Programming]]

``` python

def add(n1, n2):  
    return n1 + n2  
def subtract(n1, n2):  
    return n1 - n2  
def multiply(n1, n2):  
    return n1 * n2  
def divide(n1, n2):  
    return n1 / n2  
  
operations = {  
    '+': add,  
    '-': subtract,  
    '*': multiply,  
    '/': divide  
}  
  
def calc_main():  
    n1 = float(input("enter your first number: \n"))  
    while True:  
       for symbol in operations:  
          print(symbol)  
       operation_symbol = input(("choose one of the above operation symbols or 'exit' to quit: \n"))  
       if operation_symbol == "exit".lower():  
          print("goodbye!")  
          break  
       if operation_symbol not in operations:  
          print("Wrong operation! try again: \n")  
          continue  
       n2 = float(input("enter your second number: \n"))  
       result = (operations[operation_symbol](n1, n2))  
       print(f"{n1} {operation_symbol} {n2} = {result}")  
       result_decision = input("Do you want to reuse the result? 'y' for yes, 'n' for no: \n").lower()  
       if result_decision == "y":  
          n1 = result  
       elif result_decision == 'n':  
          return calc_main()  
       else:  
          print("wrong input! choose yes or no:\n")  
          continue  
  
calc_main()
```
