import random
# Step 1: Get user choice
def get_user_choice():
    choice = input("Enter your choice (rock, paper, or scissors): ").lower()
    while choice not in ['rock', 'paper', 'scissors']:
        print("Invalid input. Try again.")
        choice = input("Enter your choice (rock, paper, or scissors): ").lower()
    return choice

# Step 2: Get computer choice
def get_computer_choice():
    return random.choice(['rock', 'paper', 'scissors'])

# Step 3: Determine the winner
def determine_winner(user, computer):
    if user == computer:
        return "It's a tie!"
    elif (user == 'rock' and computer == 'scissors') or \
         (user == 'paper' and computer == 'rock') or \
         (user == 'scissors' and computer == 'paper'):
        return "You win!"
    else:
        return "Computer wins!"

# Step 4: Play the game
def play():
    user = get_user_choice()
    computer = get_computer_choice()
    
    print(f"\nYou chose: {user}")
    print(f"Computer chose: {computer}")
    
    result = determine_winner(user, computer)
    print(f"Result: {result}")

# Run the game
play()
