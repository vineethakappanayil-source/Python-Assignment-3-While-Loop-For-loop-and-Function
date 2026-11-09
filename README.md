# Python Assignment 3

Three beginner Python programs practicing while loops, for loops, control statements, and functions.

## Requirements

- Python 3

## Programs

### Number guessing game

```bash
import random

secret_number = random.randint(1, 10)
attempts = 3

while attempts > 0:
    guess = int(input("Guess the number (between 1 and 10): "))

    if guess < 1 or guess > 10:
        print("Your guess is out of range. Please guess a number between 1 and 10.")
        continue

    attempts -= 1

    if guess == secret_number:
        print("Congratulations! You guessed the correct number.")
        break
    elif guess < secret_number:
        print("Too low. Try again.")
    else:
        print("Too high. Try again.")

    if attempts > 0:
        print(f"You have {attempts} attempt(s) left.")

else:
    print(f"Better luck next time! The number was {secret_number}.")
```

Guess a random number from 1 to 10. You get three valid guesses. Out-of-range guesses do not use an attempt.

### Multiplication table

```bash
number = int(input("Enter a number for the multiplication table: "))

for i in range(1, 11):
    result = number * i
    print(f"{number} x {i} = {result}")
```

Enter a number to print its multiplication table from 1 to 10.

### BMI calculator

```bash
def calculate_bmi(weight, height):
    return weight / (height ** 2)


weight = float(input("Enter your weight in kg: "))
height = float(input("Enter your height in meters: "))

bmi = calculate_bmi(weight, height)
print(f"Your BMI is: {bmi:.2f}")
```

Enter your weight in kilograms and height in meters to calculate BMI.
