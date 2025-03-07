tags:
[[Python]]; [[Programming]]; [[Python – For and While]]; [[Python - Functions]]

``` python
name_1 = input('enter the first name: ')  
name_2 = input('enter the second name: ')  
  
  
def love_calculator(name_1, name_2):  
  
    counts = {'t': 0, 'r': 0, 'u': 0, 'e': 0, 'l': 0, 'o': 0, 'v': 0}  
    for letter in (name_1 + name_2).lower():  
       if letter in counts:  
          counts[letter] += 1  
       for letter in 'true':  
          print(f'letter {letter} occurs {counts[letter]} times')  
       for letter in 'love':  
          print(f'letter {letter} occurs {counts[letter]} times')  
    total_true = sum(counts[letter] for letter in 'true')  
    total_love = sum(counts[letter] for letter in 'love')  
    final_total = (str(total_true) + str(total_love))  
    print('total love counter for these two names is equal to ', final_total)  
  
love_calculator(name_1, name_2)

```
