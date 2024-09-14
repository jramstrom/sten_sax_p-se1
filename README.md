# sten_sax_påse1
import random

def play_game():
    choices = ["rock", "paper", "scissors"]
    player_choice = input("rock, paper or scissors? ").lower()
    computer_choice = random.choice(choices)

    print(f"Player: {player_choice}")
    print(f"Computer: {computer_choice}")

    if player_choice == computer_choice:
        print("It's a tie!")
    elif player_choice == "rock":
        if computer_choice == "scissors":
            print("Player wins!")
        else:
            print("Computer wins!")
    elif player_choice == "paper":
        if computer_choice == "rock":
            print("Player wins!")
        else:
            print("Computer wins!")
    elif player_choice == "scissors":
        if computer_choice == "paper":
            print("Player wins!")
        else:
            print("Computer wins!")
    else:
        print("Invalid choice!")

while True:
    play_game()
    play_again = input("Play again? (yes/no) ").lower()
    if play_again != "yes":
        print("Game over!")
        break
