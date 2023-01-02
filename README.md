# snake-water-gun-Game
this is a funny game
# CREATE A SNAKE GAME USING PYTHON
from pyfiglet import figlet_format
import random
l1=["s","w","g"]
total_choice=10
number_of_chance=0
score_human=0
Score_cpomputer=0
print("\t \t\tSNAKE WATER GUN")
while number_of_chance<total_choice :
     #print("Enter Your Choice :\ns-Snake\nw-Water\ng-Gun")
    inp = input("Enter Your Choice :\ns-Snake\nw-Water\ng-Gun\n")
    _random=random.choice(l1)

    if _random==inp :
        print("Tie ,No one get points ")
        print(f"Your Guess {inp} and Computer Guess {_random}")
        print(f"Your Point {score_human} and the computer score {Score_cpomputer}")

    #if user enter s
    elif inp=="s" and _random=="w":
        score_human=score_human+1
        print(f"Your Guess {inp} and Computer Guess {_random}")
        print("Human Winner")
        print(f"Your Point {score_human} and the computer score {Score_cpomputer}")



    elif  inp=="s" and _random=="g":
        Score_cpomputer = Score_cpomputer + 1
        print(f"Your Guess {inp} and Computer Guess {_random}")
        print("Computer Win")
        print(f"Your Point {score_human} and the computer score {Score_cpomputer}")


    # if user enter the w
    elif inp == "w" and _random == "s":
        Score_cpomputer = Score_cpomputer + 1
        print(f"Your Guess {inp} and Computer Guess {_random}")
        print("Computer Win")
        print(f"Your Point {score_human} and the computer score {Score_cpomputer}")


    elif  inp=="w" and _random=="g":
        score_human=score_human+1
        print(f"Your Guess {inp} and Computer Guess {_random}")
        print("Human Winner")
        print(f"Your Point {score_human} and the computer score {Score_cpomputer}")


    # if user enter the g
    elif inp == "g" and _random == "s":
        score_human=score_human+1
        print(f"Your Guess {inp} and Computer Guess {_random}")
        print("Human Winner")
        print(f"Your Point {score_human} and the computer score {Score_cpomputer}")


    elif  inp=="g" and _random=="w":
        Score_cpomputer = Score_cpomputer + 1
        print(f"Your Guess {inp} and Computer Guess {_random}")
        print("Computer Win")

    number_of_chance = number_of_chance + 1
    print(f"Chance {int(total_choice)-int(number_of_chance)} left out of {total_choice}")


print(figlet_format("G A M E  O V E R"))
print(f"human Score {score_human} and Computer Score {Score_cpomputer}")

if score_human==Score_cpomputer:
    print("Tie Situation")
elif score_human>Score_cpomputer:
    print("Human Winner Finally")
else :
    print("Computer Winner Finally")



