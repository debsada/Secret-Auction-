# Silent-Auction-
A programme that allows users to input their name and bidding price into a dictionary which is then iterated through to find the highest bid and announce the winning bidder. 


from replit import clear
from art import logo

print(logo) 

print("Welcome to the secret auction!")


auction_dict = {
  
}  #empty dictionary to store each user's bid 

new_bidders = True 

while new_bidders == True: #computer will continue to update the dictionary with new bids until there are no more bidders 
  name = (input("What is your name? "))
  auction_dict[name] = int(input("What is your bid? "))
  should_continue = (input("do you want to add another bid? Y or N "))
  if should_continue != "Y":
    new_bidders = False
  else:
    clear() #if there are more bidders wanting to add bid then computer will clear terminal to allow for next user to enter their bid - hence secret auction


highest_number = 0 
highest_bidder = ""

for key in auction_dict: #will iterate through all the values of the keys until it finds the highest bidder 
  if auction_dict[key] > highest_number:
    highest_number = auction_dict[key]
    highest_bidder = key #name of bidder with the highest bid 

print(f"the winning bidder is {highest_bidder}") #announces the winning bidder 
