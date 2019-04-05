#A-number-winning-game.
#A game in which random number between 1-10 will Win and as well as it shows how many attempts you take to guess the correct number.


import random

winning_number= random.randint(1,10)      
#We have to import random and enter number in int.

guess=1                            
#to store number of attempts

number = int(input("Guess a number: "))    
#User will choose any number between 1-10.

game_over= False                         
while not game_over:                       
    if number == winning_number:
        print(f"Wowww..Your win this in {guess}th attempt!!")
        
        game_over=True        
        
        #Here the game will stop once user guess the winning number
    else:
        if number < winning_number:
        
            print("ohhh..sorry its quite low :( Try again.")
            
            #how far from the winning number.
        else:
            print("ohhh..sorry its high :) try again"
            
            guess+=1    
            
            #add number of attempts done
            
            number=int(input("Guess the number again:")) 
            
            #the game will continuee until user don't guess the winning number.
