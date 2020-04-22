# Monte-Hall-Game
It is a small game in which there are two doors .A door has a gift while other two have goats .The door that the player chooses first cant be opened then he has to choose another door and decide wether to open or swap.
import random
Doors=[0]*3
goat_doors=[0]*21
swap=0 #No of swap wins
no_swap=0 #No of no swap wins
x=random.randint(0,2) #xth door will comprise of prize
Doors[x]="BMW"
for i in range(0,3):
    if (i==x):
        continue;
    else:
        Doors[i]="Goats"
        goat_doors.append(i)
choice=int(input("Enter your choice"))
door_open=random.choice(goat_doors) #Open door that comprise Goat
while(door_open==choice):
    door_open=random.choice(goat_doors) #door open shouldnot be equal to choice made by the participant
ch=input("Do you want to swap? y/n ")
if(ch=="y"):
    if(Doors[choice]=="Goats"):
        print(" Player Wins")
        swap=swap+1
    else:
        print("Player lost")
else:
    if(Doors[choice]=="Goats"):
          print("Player lost")
    else:
          print("Player wins")
          no_swap=no_swap+1
print(swap)
print(no_swap)    
        
    
  
        
