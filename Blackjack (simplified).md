tags:
[[Python]]; [[Programming]]; [[Python - Functions]]

``` python
import random  
import math  
  
cards = [11, 2, 3, 4, 5, 6, 7, 8, 9, 10, 10, 10, 10]  
  
def draw_card(player_hand):  
    player_hand.append(random.choice(cards))  
    return player_hand  
  
def comp_hand_calculation(comp_hand):  
    while sum(comp_hand) < 16:  
        comp_hand.append(random.choice(cards))  
    return comp_hand  
  
def value_calculation(hand):  
    total = sum(hand)  
    while total > 21 and 11 in hand:  
        hand[hand.index(11)] = 1  # Change Ace from 11 to 1  
        total = sum(hand)  # Recalculate total after change  
    return total  
  
def get_card_player_decision():  
    while True:  
       card_player_decision = input("do you want another card? y for yes, n for no and getting the results: \n").lower()  
       if card_player_decision in ("y", "n"):  
          return card_player_decision  
       else:  
          print("invalid input. Try again: \n")  
  
  
def result (player_hand, comp_hand):  
    if sum(player_hand) > 21:  
        return "Bust!"  
    elif sum(player_hand) == 21:  
        return "Blackjack!"  
    elif sum(player_hand) > sum(comp_hand) or sum(comp_hand) > 21:  
        return "You win!"  
    else:  
        return "You lose!"  
  
def print_values_regular(player_hand, comp_hand):  
    print(f"your hand is {player_hand}, the sum is {sum(player_hand)}")  
    print(f"the computer's first card is {comp_hand[0]}")  
  
  
  
  
def main():  
    while True:  
       player_hand = [random.choice(cards), random.choice(cards)]  
       comp_hand = [random.choice(cards), random.choice(cards)]  
       comp_hand = comp_hand_calculation(comp_hand)  
  
       print_values_regular(player_hand, comp_hand)  
       while True:  
          card_decision = get_card_player_decision()  
          if card_decision == "y":  
             player_hand = draw_card(player_hand)  
             print_values_regular(player_hand, comp_hand)  
             if sum(player_hand) > 21:  
                print("You bust!")  
                break  
             if sum(player_hand) == 21:  
                print("Blackjack! You win.")  
                break  
          elif card_decision == "n":  
             print(result(player_hand, comp_hand))  
             print(f"your hand is {player_hand}, the sum is {sum(player_hand)}")  
             print(f"the dealer's hand is {comp_hand}, and the sum is {sum(comp_hand)}")  
             break  
  
  
       play_again = input("do you want to play again? y/n \n").lower()  
       if play_again == "n":  
          break  
       else:  
          continue  
  
main()

```
