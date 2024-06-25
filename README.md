Project Name: Word Jumble
Description
"Word Jumble" is a web-based application designed to challenge and improve your word-forming skills. The game presents a jumbled set of letters, and the player must rearrange them to form a valid word. This engaging and educational tool is perfect for both casual players looking to pass time and individuals aiming to enhance their vocabulary and spelling skills.

Features
Interactive Gameplay: Users can drag and drop letters to form words.
Real-Time Feedback: Immediate validation of the formed word, notifying if it is correct or not.
User-Friendly Interface: A clean and intuitive design that enhances the gaming experience.
Responsive Design: Optimized for various screen sizes, ensuring accessibility on both desktop and mobile devices.
How to Play
1-Start the game by pressing the "Start" button.
2-A set of jumbled letters will appear on the screen.
3-Drag and drop the letters to rearrange them into a valid word.
4-Submit your word to see if it's correct.
5-Continue to the next jumble or retry the current one if necessary.

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


