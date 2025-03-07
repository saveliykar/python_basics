tags:
[[Python]]; [[Programming]]; [[Python – For and While]]

``` python
import random  
  
word_list = ['cigarette', 'baboon', 'drugs', 'python']  
chosen_word = random.choice(word_list)  
  
  
display = ['_'] * len(chosen_word)  
mistake_counter = 5  
  
# Game loop  
while mistake_counter > 0 and '_' in display:  
    print(f"{' '.join(display)}")  
    print(f"You have {mistake_counter} mistakes remaining.")  
  
    guess = input('Guess a letter: ').lower()  
  
    if guess in chosen_word:  
        for index, letter in enumerate(chosen_word):  
            if letter == guess:  
                display[index] = guess  
        print("Correct guess!")  
    else:  
        mistake_counter -= 1  
        print("Wrong guess!")  
  
if '_' not in display:  
    print(f"Congratulations! You guessed the word: {chosen_word}")  
else:  
    print(f"Game over! The word was: {chosen_word}")

```
