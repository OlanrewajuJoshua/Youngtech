# Youngtech
import random

secret_number = random.randint(1, 10)  # generate a random integer between 1 and 10
guess_limit = 5
guesses_left = guess_limit

while guesses_left > 0:
    print(f"You have {guesses_left} guesses left.")
    guess = int(input("Guess the secret number between 1 and 10: "))
    
    if guess == secret_number:
        print("Congratulations! You guessed the secret number!")
        break  # exit the loop
        
    else:
        print("Sorry, that's not the secret number.")
        guesses_left -= 1  # decrease the number of guesses left
        
        if guesses_left == 0:
            print(f"You have no more guesses left. The secret number was {secret_number}.")
            break  # exit the loop
            
        else:
            hint1 = secret_number
            hint2 = random.randint(1, 10)
            print(f"Here's a hint: pick between {hint1} and {hint2}")
            choice = int(input("Which number do you choose? "))
            if choice == secret_number:
                print("You got it! The secret number was", secret_number)
                break
            else:
                print("Sorry, that's not the secret number.")
            
print("Thanks for playing!")
