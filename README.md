# Phython-game
rock, paper, lizard, spock
import random
def str2num (str):
    if str=="Spock":
        return 1
    if str=="Rock":
        return 0
    if str=="Paper":
        return 2
    if str=="Scissers":
        return 4
    if str=="Lizard":
        return 3
def num2str(num):
    if num==0:
        return "Rock"
    if num==1:
        return "Spock"
    if num==2:
        return "Paper"
    if num==3:
        return "Lizard"
    if num==4:
        return "Scissers"
p=0
c=0
while p<3 or c<3:
    player_str=raw_input("Enter you choice:")
    player_num=str2num(player_str)
    comp_num=random.randrange(0,5)
    comp_str=num2str(comp_num)
    diff=(player_num-comp_num)%5
    print "Computer choice",comp_str
    print "Pleyer choice",player_str
    if diff==0:
        print"Tie"
    elif diff==1 or diff==2:
        print"Player wins"
        p+=1

    else:
        print"Computer wins"
        c+=1
    print
