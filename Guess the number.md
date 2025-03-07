tags:
[[Python]]; [[Programming]]; [[Python - Functions]]

``` python
import random  
  
def guess_number(random_number, max_tries):  
    user_guess_counter = 0  
    print(f"You have {max_tries} tries.")  
    while user_guess_counter < max_tries:  
        try:  
            user_guess = int(input("enter your guess: \n"))  
        except ValueError:  
            print("invalid input. enter a number.")  
            continue  
        user_guess_counter += 1  
        if user_guess > random_number:  
            print("too high. try again.")  
        elif user_guess < random_number:  
            print("too low. try again.")  
        else:  
            print("you won! nice bro")  
            return  
    print("you lost! no tries left.")  
  
def main():  
    while True:  
        random_number = random.randint(1, 100)  
        print(random_number)  
        while True:  
            dif_choice = input("welcome to the number guessing game!\n"  
                               "the computer guessed a random number from 1 to 100.\n"  
                               "choose easy (10 tries) or hard (5 tries) (e/h): \n ").lower()  
            if dif_choice in ("e", "h"):  
                break  
            print("enter a valid argument: \n")  
  
        max_tries = 10 if dif_choice == "e" else 5  
        guess_number(random_number, max_tries)  
        play_again = input("do you want to play again? (y/n): ").lower()  
        if play_again == "n":  
            break  
  
main()

```
