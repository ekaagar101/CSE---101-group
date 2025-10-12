import random
#imports random module for predefined random function
print("Let's play hangman!")

randwords = ['Ostrich', 'Lacrosse', 'Samosa', 'Chipotle', 'Kendrick', 'Kazakhstan', 'Magnolia', 'Chestnut', 'Alliteration', 'Spiderman', 'Trignometry']
# Long list of possible words (11 possibilities) 
word = random.choice(randwords).lower()
#Uses random.choice function for random module and .lower() to lowercase the text
guessed_letters = []
#Creates a new list that will be added to with the guessed letters
lives = 6
#amount of opportunities they have to guess letters
amount = len(word)
#Finds how long the word is
display_word = []
#Another list for the display of the word
for i in range (amount):
    display_word.append('_')
    print ('_', end = '')
#For loop to create the x amount of _ to act as blank spaces for possible characters
print ("You have 6 six lives left to guess this word. ")
def show_word():
    print ("Current word: ", end = '')
    for letter in display_word:
        print(letter, end= '')
    print()
#To add letters to form a new word
def user_guess():
#this function gives different outcomes depending on what the user inputs
    global lives
#refers to a variable on global scope accessed inside a function
    guess = input('Guess a Letter or type "help": ').lower()
    if guess == 'help':
        print ("Letters guessed so far: ", guessed_letters)
        return
    #return statements don't take away a guess from the user
    if guess in guessed_letters:
        print("You already guessed that letter.")
        return
    #return statements don't take away a guess from the user
    guessed_letters.append(guess)
    if guess in word:
        print ("Good Guess!")
        for i in range(amount):
            if word[i] == guess:
                display_word[i] = guess
    else: 
        print("Wrong Guess")
        lives -= 1
        print("Lives left: ", lives)
    show_word()
while lives > 0 and '_' in display_word:
    user_guess()
if '_' not in display_word:
    print("You have won!")
else:
    print("Game over! The word was: ", word)
input ("Would you like to play again? If so restart this program.")

