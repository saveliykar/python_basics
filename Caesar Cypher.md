tags:
[[Python]]; [[Programming]]; [[Python – For and While]]; [[Python - Functions]]


``` python
import string  
alphabet = list(string.ascii_lowercase)  
result = []  
def encrypt(message, shift):  
    for letter in message:  
       if letter in alphabet:  
          shift_index = (alphabet.index(letter) + shift) % len(alphabet)  
          result.append(alphabet[shift_index])  
       else:  
          result.append(letter)  
    final_encrypt = ''.join(result)  
    print(final_encrypt)  
def decrypt(message, shift):  
    return encrypt(message, -shift)  
  
  
def main():  
    message = input('enter your original message: \n').lower()  
    shift = int(input('what shift do you want to encrypt / decrypt? \n'))  
    while True:  
       user_choice = input('enter encrypt, decrypt or break (lowercase): ')  
       if user_choice == 'encrypt':  
          encrypt(message, shift)  
       elif user_choice == 'decrypt':  
          decrypt(message, shift)  
       elif user_choice == 'break':  
          break  
       else:  
          print("invalid choice.  enter 'encrypt', 'decrypt', or 'break'.")  
  
  
main()

```
