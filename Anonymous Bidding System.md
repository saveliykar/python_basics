tags:
[[Python]]; [[Programming]]; [[Python - Dictionaries]]

``` python
  
def clear_output():  
    print("\n" * 100)  
  
bids = {}  
  
def bid_process():  
    bidder_name = input("Enter your name: \n")  
    bid = int(input("Enter your bid (in USD): \n"))  
    bids[bidder_name] = bid  
  
def main():  
    print(  
       "Hello! This is an anonymous bidding system. Input your name, your bid, and pass the computer to the next person.")  
    while True:  
       bid_process()  
       answer = input("Any other bidders? If so, print 'yes'. If no, print 'no': \n").lower()  
       clear_output()  
       if answer == "no":  
          break  
    winning_bid = max(bids, key=bids.get)  
    print(f"The winner of the bidding process is {winning_bid} with a bid of ${bids[winning_bid]}!")  
  
  
main()
```
