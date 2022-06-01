# Rock-Paper-Scissors
import random

print("Welcome to Rock Paper Scissors!")
print("where R = Rock, P = Paper, S = Scissors")
print("Are You Ready!")

###set up variables
cpuScore = 0
playerScore  = 0
tieScore = 0
possibleHands = ["R","P","S"]

def checkforwinner(playerHand, computerHand):
  if(playerHand == "R" and computerHand == "P"):
    print("sorry you lost :(")
    return "cpu"
  elif (playerHand == "R" and computerHand == "S"):
    print("congrats you have won :)")
    return "player"
    
  elif (playerHand == "S" and computerHand == "P"):
    print("congrats you have won:)")
    return "player"
    
  elif (playerHand == "S" and computerHand == "R"):
    print("sorry,you lost!")
    return "cpu"
    
  elif (playerHand == "P" and computerHand == "R"):
    print("congrats you have won:)")
    return "player"

  elif (playerHand == "P" and computerHand == "S"):
    print("sorry, you lost!")
    return "cpu"
  else:
    print("it is a tie,play again!")
    return "tie"
    
###start game Loop
while(playerScore != 3 and cpuScore != 3):

  ###validate input
  while True:
   playerHand = input("\npick a hand. , R or P or S: ")
  if(playerHand == "R" or playerHand == "P" or playerHand == "S"):
     break
  else:
    print("invalid input. try again.")
###generate computer pick
computerHand = random.choice(possibleHands)

###print results
print("your hand: ",playerHand)
print("cpu hand: ", computerHand)
result = checkforwinner(playerHand, computerHand)
if(result == "p"):
       playerScore == 1
elif(result == "cpu"):
        cpuScore += 1
else:
      tieScore += 1
print("your score: ",playerScore,"cpu: ",cpuScore, "ties: ",tieScore)
print("Game over! Thank you for playing :)")












