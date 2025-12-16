import random

word_bank= ["cat", "dog", "deer", "spaghetti", "rahmenbedigungen"]
word = random.choice(word_bank)

guessedWord = ["_"] * len(word)
attempts = 10
guessed_letters = []

print("Welcome to the Word Guessing Game!")

while attempts > 0:
    print("\nWord: " + " ".join(guessedWord))
    print(f"Remaining entitlement: {attempts}")

    guess = input("Guess a letter: ").lower()

    if not guess.isalpha() or len(guess) != 1:
        print("Please enter only one letter.")
        continue

    if guess in guessed_letters:
        print(f"You already guessed this letter: {guess}")
        continue

    guessed_letters.append(guess)

    if guess in word:
        print("Correct!")
        
        for i in range(len(word)):
            if word[i] == guess:
                guessedWord[i] = guess
    
    else:
        attempts -= 1
        print(f"Incorrect! You have {attempts} left.")
    
    if "_" not in guessedWord:
        print(f"Congratulations! You guessed it right: {word}")
        break

if attempts == 0 and "_" in guessedWord:
    print(f"Time's up. Answer: {word}")
