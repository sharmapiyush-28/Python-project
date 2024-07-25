#Python-project
#2nd semester project of python on Typing speed
from time import *
import random as r

def mistake(partest, usertest):
    error=0
    for i in range(len(partest)):
        try:
            if partest[i] != usertest[i]:
                error = error + 1
        except:
            error = error + 1
    return error

def speed_time(time_s, time_e, userinput):
    time_delay = time_e - time_s
    time_R = round(time_delay,2)
    speed = len(userinput)/ time_R
    return round(speed)
while True:
    check = input("Ready to test: Yes/No:")
    if check == "yes":
        test = ["The quick brown fox jumps over the lazy dog. Typing swiftly requires practice and precision. Consistency is key to improving typing speed. Keep practicing to become a faster typist!"]
        test_1 = r.choice(test)
        print( "  ****** typing speed ******   ")
        print(test_1)
        print()
        print()
        time_1 = time()
        testinput = input("Start writing:")
        time_2 = time()
        print('Speed:',speed_time(time_1,time_2,testinput),"w/sec")
        print("Error:", mistake(test_1,testinput))
    elif check == "No":
        print("Thank You")
        break
    else:
        print("Wrong input")


