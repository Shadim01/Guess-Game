import random

print("\nYou are going to play guess game!\nRules are as follows\n\tComputer guess and you too!"
      "\nIf your guess equals to computer guess,You wins!\n"
      "Maximum guess allowed are 3.\n\t\tGame is starting........")

guess_allowed = 3
print(f"{guess_allowed},guesses left")
print("Guess the number between 1 to 10")

while True:
    guess = int(input("Guess Number :"))
    computer_guess = random.randint(1,10)
    print(f"You guess {guess}\nComputer guess {computer_guess}")

    if guess>10:
        print("Eror!Please guess between 1 to 10!")

    if guess>0<11 and guess == int(computer_guess):
        print("Hurrey! You Wins")
        break

    elif guess_allowed == 1:
        print("No guesses left\nYou loss\tGame over!!")
        break


    else:
        print("Guess again please!")
        guess_allowed = guess_allowed - 1

        print(f"{guess_allowed} guesses left")
        print("Guess the number between 1 to 10")

