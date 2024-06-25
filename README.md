

import random

class WordJumble:
    def __init__(self):
        self.words = ["python", "java", "ruby", "php", "perl", "scala", "swift", "go", "kotlin", "csharp"]
        self.score = 0

    def play(self):
        word = random.choice(self.words)
        jumbled_word = self.jumble(word)
        print("Jumbled word: " + jumbled_word)
        guess = input("Guess the word: ")
        if guess == word:
            print("Correct!")
            self.score += 1
        else:
            print("Incorrect. The word was: " + word)
        print("Score: " + str(self.score))

    def jumble(self, word):
        jumbled = list(word)
        random.shuffle(jumbled)
        return "".join(jumbled)

def main():
    game = WordJumble()
    choice = ""
    while choice != "exit":
        print("Welcome to Word Jumble!")
        print("1. Play")
        print("2. Score")
        print("3. Exit")
        choice = input("Enter your choice: ")
        if choice == "1":
            game.play()
        elif choice == "2":
            print("Your score is: " + str(game.score))
        elif choice == "3":
            print("Goodbye!")
            break
        else:
            print("Invalid choice.")

if __name__ == "__main__":
    main()

----


+*Out[ ]:*+
----
Welcome to Word Jumble!
1. Play
2. Score
3. Exit
----


