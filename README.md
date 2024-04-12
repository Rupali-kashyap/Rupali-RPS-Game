# Rock Paper Scissors Game

import random   #genrate random variable

print("--------------------------------")
print("Welcome to Rock, Paper, Scissors")
print("--------------------------------")
player_win = 0
computer_win = 0

while True:
    player = input("Enter a choice (rock, paper, scissors): ")
    choices = ["rock", "paper", "scissors"]
    computer = random.choice(choices)
    print(f"\nYou choose {player}, computer choose {computer}.")
    if player == computer: 
        print(f"Both players selected {player}. \nIt's a tie!")        
    elif player == "rock":
        if computer == "scissors":
            print("Rock smashes scissors. \nYou win!")
            player_win+=1
        else:
            print("Paper covers rock. \nYou lose.")
            computer_win+=1
    elif player == "paper": 
        if computer == "rock":
            print("Paper covers rock. \nYou win!")
            player_win+=1
        else:
            print("Scissors cuts paper. \nYou lose.")
            computer_win+=1
    elif player == "scissors":   
        if computer == "paper":
            print("Scissors cuts paper. \nYou win!")
            player_win+=1
        else:
            print("Rock smashes scissors. \nYou lose.")
            computer_win+=1
    print("You have "+str(player_win)+" wins")
    print("The computer has "+str(computer_win)+" wins")
    repeat   = input("\nPlay again? (yes/no): ")
    if repeat.lower() != "yes": # lower method returns the lowercase string from given string
        print("Thanks for playing!")
        break  
        
