$$$This is my journal$$$

CLASS NO.1:

1.What did we do?
We work as a team of 3 to write the commands for a robot to make a jelly bread using the jelly jars, the knife, cooking paper's bag and the bag of bread.

2.What did you learn?
I learned that to make a robot to do something, like making a jelly bread, I cannot just tell it: ''Make a jelly bread''. I need to give it very very specific and small commands like: ''Take a knife'', ''Stick the knife into the jelly jar'', ''Go down with the knife''. More importantly, today, I learned how to combine small commands into a big command. By repeating this big commands, I had saved time to write the command for the robot.

3.Question I have:No questions








CLASS NO.2:

1.What did we do? 
Installed Python

Learn to use def, fill, print, set up background, size, generate random color, x and y coordinates, mouseClicked.

##Coding of today##( generate a program that generate random color, random size circle each time I click into the window)
 
```.py
    def setup():
        size(1000,1000)
        background(255)
        textAlign(CENTER, CENTER)

    def draw():
        print("")

    def mouseClicked():
        x= mouseX
        y= mouseY
        z= random(10,100)
        r= random(0,255)
        g= random(0,255)
        b= random(0,255)
        fill(r, g, b)

        print(x)
        circle(x, y, z)
        fill(0)
        textSize(z/3);
        text ("Kien", x, y)
        print(x, y)
        line(500,500,x,y)
 ```
2.What did you learn? I that in Python, if I want "something1" to be infront of "something2", I need to code that "something" infront of "something2"

3.Question I have: No questions

4.##Homework##:
1.Add lines from the middle of the window to each circle: https://github.com/BrightChanges/InfoScience/blob/master/Homework_2_No_1.pyde
2.Add lines from circle to circle:
https://github.com/BrightChanges/InfoScience/blob/master/Homework_2_No_2.pyde










CLASS NO.3: 

1.What did we do? 
Creating a dice that give us random value each time we click
2.What did you learn?
I learnt the command if(), range of value of number in Python( 0~0.99=1, 1~1.99=2), draw a rectangle with curves,strengthen my understanding of def draw():, rbg value of main color like white, black, red.
3.Question I have: No questions

##Coding of today##
def setup():

    size(600,600)
    def draw():
    x=0 
    
def mouseClicked():

    n = random(0,6)
    print(n)
    background(0)
    fill(255)
    rect(100, 100, 400, 400, 20);
    fill(255,0,0)
    if 0<=n<1:
        circle(300,300,50)
    if 1<=n<2:
       circle(200,200,50) 
       circle(400,400,50)
    if 2<=n<3:
        circle(200,200,50) 
        circle(300,300,50)
        circle(400,400,50)
    if 3<=n<4:
        circle(200,200,50) 
        circle(400,400,50)
        circle(200,400,50)
        circle(400,200,50)
    if 4<=n<5:
        circle(200,200,50) 
        circle(400,400,50)
        circle(200,400,50)
        circle(400,200,50)
        circle(300,300,50)
    if 5<=n<6:
        circle(200,200,50) 
        circle(400,400,50)
        circle(200,400,50)
        circle(400,200,50)
        circle(400,300,50)
        circle(200,300,50)
        
3.Question I have: No questions



CLASS NO.4:

1.What did we do?
Create atomatic growing graphs that shows the amount of result I got from rolling, total amount of rolls's counter, and makes the dice to roll by itself
2.What did you learn?
I learnt how to use the command def barGraph():, stroke(), in...range(), and strengthen my understanding of global variables, the command print() and how to create rectangles.

##Coding of today##
one_c = 0
two_c = 0
three_c = 0
four_c = 0
five_c = 0
six_c = 0
total=0

def setup():

    size(600,600)
    textSize(30);

    
    
def draw():

    x=0 
    mouseClicked()
    delay(5)
    barGraph()

    
    
    
def barGraph():

    global one_c, two_c, three_c, four_c, five_c, six_c
    fill(255)
    stroke(255,0,0)
    fill(255,0,0)
    rect(50,540-one_c,20,one_c)
    rect(150,540-two_c,20,two_c)
    rect(250,540-three_c,20,three_c)
    rect(350,540-four_c,20,four_c)
    rect(450,540-five_c,20,five_c)
    rect(550,540-six_c,20,six_c)
    for x in range(0,6):
        text(x+1, 50 + 100*x,570)
 
    
def mouseClicked():

    global one_c, two_c, three_c, four_c, five_c, six_c, total
    n = random(0,6)
    background(0)
    fill(255)
    rect(100, 100, 400, 400, 20);
    fill(255,0,0)
    
    if 0<=n<1:
        circle(300,300,50)
        one_c +=1
        total +=1
        
    if 1<=n<2:
       circle(200,200,50) 
       circle(400,400,50)
       two_c +=1
       total +=1
       
    if 2<=n<3:
        circle(200,200,50) 
        circle(300,300,50)
        circle(400,400,50)
        three_c += 1
        total +=1
        
    if 3<=n<4:
        circle(200,200,50) 
        circle(400,400,50)
        circle(200,400,50)
        circle(400,200,50)
        four_c += 1
        total +=1
        
    if 4<=n<5:
        circle(200,200,50) 
        circle(400,400,50)
        circle(200,400,50)
        circle(400,200,50)
        circle(300,300,50)
        five_c += 1
        total +=1
    if 5<=n<6:
        circle(200,200,50) 
        circle(400,400,50)
        circle(200,400,50)
        circle(400,200,50)
        circle(400,300,50)
        circle(200,300,50)
        six_c += 1
        total +=1
    text("Number of rolls :",10,30) 
    text(total,300,30)  
    print("the number of 1", one_c)
    print("the number of 2", two_c)
    print("the number of 3", three_c)
    print("the number of 4", four_c)
    print("the number of 5", five_c)
    print("the number of 6", six_c)
3. Question I have: No questions




CLASS NO.5
1.What did we do? 
We create a traffic light that turn the light brighter for red, yellow, green in an order.
2.What did you learn?
I learn how to set up waiting time by using millis() and setting up another variable and reset codes by using close()

##Coding of today##
timer = 0
def setup():

    size(600,600)
    strokeWeight(10)
    fill(255,255,255)
    stroke(0,0,0)
    rect(200,100,200,400,20)
    
    timer=millis()    
    
def draw():

    global timer
    # turn off all LED
  
    
    clear()
    if millis()> timer + 1000:
        # red
        clear()
        fill(255,0,0)
        circle(300,180,100)
    if millis()> timer + 5000:
        # yellow
        clear()
        fill(255,255,0)
        circle(300,300,100)
        print(timer)
    
    if millis()> timer + 10000:
        clear()
        fill(0,255,0)
        circle(300,420,100)
        print(timer)
        
    if millis()> timer + 15000:
        timer = millis()

def clear():

    fill(128,0,0)
    circle(300,180,100)
    fill(149,143,24)
    circle(300,300,100)
    fill(0,100,0)
    circle(300,420,100)
3.Question I have: No questions






CLASS NO.6
1.What did we do? 
We created an optical illusion when we click on it. 
2.What did you learn?
I learned how to make a repeating command "for n in range():" , and making difference's command "offset". Also, I strengthen my skill of using variables to not write codes manytimes.

##Coding of today##
offset=50
def setup():

    size(500,500)
    background(255)

def draw():

    stroke(0)
    line(0,0,500,0) #Line
    y=0
    for n in range(10):
        line(0,y,500,y)
        y=y+50
        
    fill(3,0,0)  #First round's first black square
    stroke(255)
#odd rows

    d=0
    for n in range(5):
        c=0
        for n in range(5):
            square(c,d,50)
            c=c+100
        d=d+100

        
#even rows  

    d=50
    global offset
    for n in range(5):
        c= 0+ offset
        for n in range(5):
            square(c,d,50)
            c=c+100
        d=d+100
        
def mouseClicked():

    global offset
    offset=offset+1
    
3.Question I have: I want to learn what is the difference between stroke and strokeWeight.
4.##Homework##:
-Create another optical illusion:
"How many white dots do you see?": https://github.com/BrightChanges/InfoScience/blob/master/Optical_Illusion_H_W.pyde









ClASS NO.7
No class but has 2 H.W:
1. Create an generative art:
Code:
def setup():

    size(1000, 1000)
    background(255, 255, 255)
    

    noStroke()

    
    for c in range(1000):
        center_x= random(200, 800)
        center_y= random(200, 800)
        cs=50
        #Draw Shadow
        noStroke()
        fill(15,15,15,10)
        for i in range(30):
            circle(center_x,center_y,cs-i*5)
     
    #Draw Circle
        stroke(30,30,30)
        fill(random(50, 255), random(50, 255), random(200, 255))
        circle(center_x-25,center_y-25,cs)
Product: https://github.com/BrightChanges/InfoScience_Kien-Le-Trung/blob/master/Generative%20Art.png
        
2. Create a game board with 2D array
Code:
grid = [ [1]*8 for n in range(8)]
grid[0][0] = -1
grid[7][7] = -1

w=70

def setup():

    size(800,600)
    
def draw():

    x,y= 0,0
    for row in grid:
        for col in row:
            if col == -1:
               fill(255,0,0)
            else:
                fill(255)
            rect(x,y,w,w)
            x=x+w
        y=y+w
        x=0
        
def mousePressed():
    grid[mouseY/w][mouseX/w] = grid[mouseY/w][mouseX/w]*-1
  
Product:https://github.com/BrightChanges/InfoScience_Kien-Le-Trung/blob/master/Screen%20Shot%200002-03-10%20at%205.17.49%20PM.png








CLASS NO.8
1.What did we do? 
We started learning how to code Arduino
2.What did you learn?
I learnt how to connect the LED bulbs to a breadboard, a battery,and an Arduino. I also learnt how to write some simple codes to make the LED bulbs blink.
##Coding of today##
void setup()
{
  pinMode(13, OUTPUT);
  pinMode(12, OUTPUT);
  pinMode(11, OUTPUT);
  pinMode(10, OUTPUT);
}

void loop()
{
  digitalWrite(13, HIGH);
  delay(1000); // Wait for 1000 millisecond(s)
  digitalWrite(13, LOW);
  delay(1000); // Wait for 1000 millisecond(s)
  digitalWrite(12, HIGH);
  delay(1000); // Wait for 1000 millisecond(s)
  digitalWrite(12, LOW);
  delay(1000); // Wait for 1000 millisecond(s)
  digitalWrite(11, HIGH);
  delay(1000); // Wait for 1000 millisecond(s)
  digitalWrite(11, LOW);
  delay(1000); // Wait for 1000 millisecond(s)
  digitalWrite(10, HIGH);
  delay(1000); // Wait for 1000 millisecond(s)
  digitalWrite(10, LOW);
  delay(1000); // Wait for 1000 millisecond(s)
}
3.Questions I have: No question.


CLASS NO.9 (ONLINE STUDY STARTS FROM HERE)
1.What did we do? 
We created simulation that shows people movings around. In the future, we will shows interactions, outcomes and predictions for the Coronavirus.

2.What did you learn?
I learnt how to add values to a list and strengthened my understanding in random, for loop, global, and variable assignments.
##Homework's coding for the 2 tasks##

#Task 2(creating 10 individuals moving around in random positions)(Task 2's code includes Task 1's code):

     x= [ ]
     y= [ ]

     def setup():
         global x, y
         size(500,500)

    #Setting up the 10 random coordinates
    for i in range(10):
        x.append(random(50,450))
        y.append(random(50,450))
            
                 

    def draw():
        global x, y
        background(255)
          #Drawing the 10 individuals
        for individuals in range(10):
            strokeWeight(2)
            circle(x[individuals], y[individuals], 40)
            x[individuals]= x[individuals] + random(-10,10)
            y[individuals]= y[individuals] + random(-10,10)
        
        if x[individuals] > 500:
                x[individuals] = 500
    
 #Task 1(3 additional conditions):

           if y[individuals] > 500:
                    y[individuals] = 500
        if x[individuals] < 0:
                    x[individuals] = 0
        if y[individuals] < 0:
                    y[individuals] = 0
            
        delay(100)

            delay(100)
 Outcome: https://github.com/BrightChanges/InfoScience_Kien-Le-Trung/blob/master/Screen%20Shot%200002-04-01%20at%206.29.37%20PM.png       
 3.Questions I have: I had a lot of questions(mostly about errors) but I had asked Dr.Ruben and he had help me.


CLASS NO.10.
1.What did we do?
We add a infected individual in the beginning and a function so that if other individuals get to close to that one infected individual, they will also get infected and turn from white to red.
2.What did you learn?
I learn how to create a defenition and later use it in other codes, how to use list and later apply it in loops and "if, else" statement.

##Code of today##

    x= [ ]
    y= [ ]
    h= [False, True] #False=> infected

    def setup():
        size(500,500)
    
    #Setting up the 10 random coordinates
    for i in range(10):
        x.append(random(0,500))
        y.append(random(0,500))
        h.append(True) #All healthy, h is health
        
    def distance(x1, x2, y1, y2):
        a=(x1-x2)
        b=(y1-y2)        
        c= sqrt(a**2 + b**2)
        return c



    def draw():
        global x, y
        background(255)
          #Drawing the individuals
        for individuals in range(len(x)):
            strokeWeight(2)
            if h[individuals] == True:
                fill(255)  #healthy
            else:
                fill(255,0,0)  #infected
            
        circle(x[individuals], y[individuals], 40)
        #calulate the distance to each neighbors
        for neighbors in range(len(x)):
            if neighbors == individuals:
                continue
            d = distance(x[individuals], x[neighbors], y[individuals], y[neighbors])
            if d < 40 and (h[neighbors] == False or h[individuals]==False):
                #infection happens
                h[individuals] = False
                h[neighbors] = False
            
        
    for m in range(len(x)):
        x[m]= x[m] + random(-10,10)
        y[m]= y[m] + random(-10,10)    
        if x[m] > 500:
                x[m] = 500
    
        if y[m] > 500:
                    y[m] = 500
        if x[m] < 0:
                    x[m] = 0
        if y[m] < 0:
                    y[m] = 0
            
    delay(100)
Result picture: https://github.com/BrightChanges/InfoScience_Kien-Le-Trung/blob/master/Task%2026.png
3.Questions I have: No question.

4. Homeworks/3 task for week 29:
Taks1-create a program that prints 100 bears:

    bears = ['bears', 'bears' , 'bears']


    def setup():
        size (500, 500)
        for i in range (98):
            bears.append('bears')
        bears[1] = 'bear'    
        items = (0, 'bears')
        index, letter = items
        for index, letter in enumerate (bears):
            print index, letter
   Result: https://github.com/BrightChanges/InfoScience_Kien-Le-Trung/blob/master/Screen%20Shot%200002-04-09%20at%209.17.05%20PM.png and 4 other pictures in my main file on Github.         
            
 Task2-create a program that prints the years from 1900 to 2000:
 
    years = [ ]

    def setup():
        size(500, 500)
        for i in range(1900,2001):
            print 'The year is',i
  Result:https://github.com/BrightChanges/InfoScience_Kien-Le-Trung/blob/master/Screen%20Shot%200002-04-09%20at%209.19.06%20PM.png and 3 other pictures in my main file on Github.          

Taks3-create a program that prints the conversion for Celsius to Fahrenheit 

    from 0 C to 100 C:
    from __future__ import division
    cel = [ ]


    def convert(nums):
        nums2 = (nums*9/5)+32
        return nums2

    def setup():
        size(500,500)
        for nums in range(0,101):
            cel.append(nums)
        for nums in cel:
            print nums, 'C are' , convert(nums), 'F'
  Result:https://github.com/BrightChanges/InfoScience_Kien-Le-Trung/blob/master/Screen%20Shot%200002-04-09%20at%209.15.16%20PM.png and 3 other pictures in my main file on Github.         
 
 Task4-Add a bar graph at the bottom right corner of the screen that counts the number of infected people and the number of healthy people+Add a counter for the number of times the simulation has run:
 from __future__ import division
 
        x= [ ]
        y= [ ]
        h= [False, True] #False=> infected
        infected=1
        healthy=24
        runs=1

        def setup():
            size(500,500)

            #Setting up the ... random coordinates
            for i in range(25):
                x.append(random(0,500))
                y.append(random(0,500))
                h.append(True) #All healthy, h is health
            textSize(12);

        def distance(x1, x2, y1, y2):
            a=(x1-x2)
            b=(y1-y2)        
            c= sqrt(a**2 + b**2)
            return c



        def draw():
            global x, y, infected, healthy
            background(255)


              #Drawing the individuals
            for individuals in range(len(x)):
                strokeWeight(2)
                if h[individuals] == True:
                    fill(255)  #healthy
                else:
                    fill(255,0,0)  #infected

                circle(x[individuals], y[individuals], 40)
                #calulate the distance to each neighbors
                for neighbors in range(len(x)):
                    if neighbors == individuals:
                        continue
                    d = distance(x[individuals], x[neighbors], y[individuals], y[neighbors])
                    if d < 40 and (h[neighbors] == False or h[individuals]==False) and (h[individuals] == True or h[neighbors] == True):
                        #infection happens
                        h[individuals] = False
                        h[neighbors] = False
                        infected = infected + 1
                        healthy = healthy -1
                        if healthy <0:
                            healthy=0
                        if infected >25:
                            infected=25   #Need to put infected, healthy stuff in another if statement







            for m in range(len(x)):
                x[m]= x[m] + random(-10,10)
                y[m]= y[m] + random(-10,10)    
                if x[m] > 500:
                        x[m] = 500

                if y[m] > 500:
                            y[m] = 500
                if x[m] < 0:
                            x[m] = 0
                if y[m] < 100:
                            y[m] = 100
            barGraph()        
            delay(100)


        def barGraph():
            global infected, healthy, runs
            strokeWeight(1)
            fill(255,0,0)
            rect(60, 10, infected, 10) #(x coordinate, y coordinate, width, height)
            fill(3,3,3)
            text('Infected', 10,20)
            text(infected, 180,20)
            strokeWeight(1)
            fill(255)
            rect(60, 30, healthy, 10)
            fill(3,3,3)
            text('Healthy', 10,40)
            text(healthy, 180, 35)
            text('Click screen to run the simulation again', 10, 60)
            text('Iteration # :', 10,80 )
            text(runs, 120,80)

        def mouseClicked():
            global infected, healthy, x, y, h, runs
            infected=1
            healthy=24
            x= [ ]
            y= [ ]
            h= [False, True]
            runs= runs+1
            setup()
            draw()
Result: https://github.com/BrightChanges/InfoScience_Kien-Le-Trung/blob/master/Screen%20Shot%200002-04-10%20at%203.54.42%20PM.png


CLASS NO.11. 
1.What did we do?
We add a function where after a period a time, a sick individual in the Coronavirus Simulation will be recovered and we changed True, False variables to "Healthy", "Sick" (also adding "Recovered").
2.What did you learn?
I learn that if you put the same delay time or without the delay time, a Python program will react at the same time to variables that is increased a same value. For example, if I have days[ind] -= 1 and iteration = iteration + 1, when putting in the same def funtion, the program will react to both of these at the same time.

##Coding of Today##:

             from __future__ import division
             Xlst = list()
             Ylst = list()
             HealthState =["Infected", "Healthy"] #False - infected
             days = [30, -1]
             NumOfHumans = 25
             NumOfMoving = 25
             CriticalDist = 40 
             iteration = 0
             Infected = 1
             Recovered = 0
             DaysNeededToRecover = 30 #int convert a number into an interger number #int(random(100,200))

             def bargraph():
                 global Infected, Xlst, HealthState
                 Healthy = len(Xlst) - Infected

                 text("Infected",230, 545)
                 text(Infected,550, 545)
                 fill(255,0,0)
                 rect(315, 530,Infected*5,20)
                 fill(0)
                 text("Healthy",230, 575)
                 text(Healthy,550, 575)
                 stroke(0)
                 fill(255)
                 rect(315, 560,Healthy*5,20)
                 fill(0)
                 text("Recovered",230, 605)
                 text(Recovered,550, 605)
                 fill(137,242,255)
                 rect(340, 587,Recovered*5,20)






             def setup():
                 global Xlst,Ylst, NumOfHumans,HealthState
                 size(600,700)


                 for i in range(NumOfHumans):
                     ValX = int(random(50,450))
                     Xlst.append(ValX)
                     ValY = int(random(50,450))
                     Ylst.append(ValY)
                     ValY = int(random(50,450))
                     Ylst.append(ValY)
                     HealthState.append("Healthy")
                     days.append(-1)

                def distance(x1,x2,y1,y2):
                    a = (x1 - x2)
                    b = (y1 - y2)
                    c = sqrt(a**2 + b**2)
                    return c

                def draw():
                    global Xlst,Ylst, HealthState, NumOfHumans, CriticalDist, iteration, Healthy, Infected, Recovered, DaysNeededToRecover, NumOfMoving
                    background(255)
                    strokeWeight(2)

                 Infected = 0
                 for ind in range(NumOfHumans):
                     if HealthState[ind] == "Infected":
                         Infected += 1


                 bargraph()  
                 for ind in range(NumOfHumans):
                     if HealthState[ind] == "Healthy":
                         fill(255)   #healthy
                     elif HealthState[ind] == "Recovered":
                         fill(137,242,255)
                     else:
                         fill(255, 0, 0) #infected

                     if HealthState[ind] == "Infected":
                         days[ind] -= 1
                         if days[ind] == 0:
                             HealthState[ind] = "Recovered" 
                             Recovered += 1
                             days[ind] = 0 #0 for recovered, -1 for healthy, and 30 for sick



                     #movement of the circles   
                     circle(Xlst[ind], Ylst[ind], 40) 

                     #calculating the distance between the circles
                     for nei in range(NumOfHumans):
                         if nei==ind:
                             continue
                         d = distance(Xlst[ind], Xlst[nei], Ylst[ind], Ylst[nei])
                         if d < CriticalDist and (HealthState[nei] == "Infected" or HealthState[ind] == "Infected"):
                             if HealthState[nei] == "Healthy":
                                 HealthState[nei] = "Infected"
                                 days[nei] = DaysNeededToRecover
                             if HealthState[ind] == "Healthy":
                                 HealthState[ind] = "Infected"
                                 days[ind] = DaysNeededToRecover



                 for m in range(NumOfMoving):
                     Xlst[m] = Xlst[m] + random(-10,10)
                     Ylst[m] = Ylst[m] + random(-10,10)

                     if Xlst[m] > 500:
                         Xlst[m] = 500
                     if Xlst[m] < 0:
                         Xlst[m] = 0
                     if Ylst[m] > 500:
                         Ylst[m] = 500
                     if Ylst[m] < 0:
                         Ylst[m] = 0




                 iteration = iteration + 1
                 fill(0)
                 textSize(20)
                 text("iteration = ",50,550)
                 text(iteration,160,550)
                 delay(100)
Result picture: https://github.com/BrightChanges/InfoScience_Kien-Le-Trung/blob/master/Screen%20Shot%200002-04-23%20at%208.48.33%20AM.png    
3.Do you have any questions?
Says days[ind] -= 1 and iteration = iteration + 1 are two commands, I wonder how much commands can a Python computer program can react to at the same time.



CLASS NO.12.
1.What did we do?
We decrypt a message given by Dr Ruben
2.What did you learn?
I learn what is cyptography, the use of of it, and how to do it. 

##My cyptography solving video+decrypt program##
Video: https://drive.google.com/file/d/16ixXAUkxeVNsbFr5H1JDuuLP6Fp_zOl2/view?usp=sharing
Codes(Python):

     from string import ascii_letters

     s='F gtd bfx fy f hfwsnafq fsi bjsy yt f gttym bmjwj f rfs xfni yt ymj gtd, '
     ns=''
     for c in s:
         if c in ascii_letters:
             ns=ns+ascii_letters[(ascii_letters.index(c)+21)%len(ascii_letters)]
         else:
             ns+=c

     print(ns)
(the decrypt message will be run on the terminal)
3.Do you have any questions? 
No.

    
    
    
   

