# Rock, Paper, Scissors game by Gbughul Lubem 

# Define the options
choices = ["rock", "paper", "scissors"]

# Print a welcome message
print("=== Welcome to Rock, Paper, Scissors Game ===")
print("Rules: Rock beats Scissors, Scissors beats Paper, Paper beats Rock")
print("You will play against the computer. Good luck!\n")

# Get user's choice
user_choice = input("Enter your choice (rock, paper, or scissors): ").lower()

# Check if input is valid
if user_choice not in choices:
    print("Oops! That's not a valid choice. Please run the program again.")
else:
    #  Simulate the computer 'thinking'
    print("\nComputer is making a choice...")
    time.sleep(1.5)

    #  Computer randomly selects
    computer_choice = random.choice(choices)
    print(f"Computer chose: {computer_choice}")

    #  Decide the winner
    if user_choice == computer_choice:
        result = "It's a tie!"
    elif (user_choice == "rock" and computer_choice == "scissors") or \
         (user_choice == "paper" and computer_choice == "rock") or \
         (user_choice == "scissors" and computer_choice == "paper"):
        result = "You win! "
    else:
        result = "Computer wins! "

    # Display result
    print(result)

print("\nThanks for playing! ")
