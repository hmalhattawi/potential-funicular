# potential-funicular
from turtle import*
import random
print("Hello,Welcome to the Rocket Creator.Here you will select the colors for your rocket")
name=input("First please tell me your name:")
shiptopColor=input("Enter the color you want for the top of your rocket")
shipbottomColor=input("Enter the color you want for the bottom of your rocket")
shipboosterColor=input("Enter the color you want for the booster of your rocket")
takeOff=input("Do you want your rocket to take off(yes/no)")
print("Here is your rocket")

def writing(name):
  writer=Turtle()
  writer.hideturtle()
  writer.color("black")
  writer.penup()
  writer.goto(-200,-200)
  writer.pendown()
  writer.write("This rocket was made by" + name)
writing(name)

shipbottom=Turtle()
shipbottom.shape("square")
shipbottom.shapesize(10,5,1)
shipbottom.color(shipbottomColor)
bgcolor("white")
shipbottom.penup()
shipbottom.goto(0,-50)

shiptop=Turtle()
shiptop.shape("triangle")
shiptop.shapesize(5,5,1)
shiptop.color(shiptopColor)
shiptop.penup()
shiptop.goto(0,80)
shiptop.right(30)

shipbooster1=Turtle()
shipbooster1.shape("square")
shipbooster1.shapesize(8,2,10)
shipbooster1.color(shipboosterColor)
shipbooster1.penup()
shipbooster1.goto(-70,-80)
shipbooster1.pendown()


shipbooster2=Turtle()
shipbooster2.shape("square")
shipbooster2.shapesize(8,2,10)
shipbooster2.color(shipboosterColor)
shipbooster2.penup()
shipbooster2.goto(70,-80)
shipbooster2.pendown()\

flamecolor="red"

flame1=Turtle()
flame1.shape("turtle")
flame1.color(flamecolor)
flame1.penup()
flame1.hideturtle()
flame1.goto(70,-170)
flame1.speed("fastest")
flame1.pendown()

flame2=Turtle()
flame2.shape("turtle")
flame2.color(flamecolor)
flame2.penup()
flame2.hideturtle()
flame2.goto(-70,-170)
flame2.speed("fastest")
flame2.pendown()


if(takeOff=="yes"):
  for i in range(0,200,10):
    shipbottom.goto(0,-50+i)
    shiptop.goto(0,80+i)
    shipbooster1.goto(-70,-80+i)
    shipbooster2.goto(70,-80+i)
    flame1.circle(10)
    flame1.goto(70,-170+i)
    flame2.circle(10)
    flame2.goto(-70,-170+i)
elif (takeOff=="no"):
    print("You choose not to take off")
else:
    print("Sorry,you did not choose yes or no.Please try again if you want it to take off")
  
done()
