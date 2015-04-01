# -*- coding: utf-8 -*-
"""
Created on Tue Mar 24 15:40:38 2015

@author: Gabriel
"""
import turtle
import random
turtle.setup(1200,500)


def forca():
    forca = turtle.Turtle()    
    forca.hideturtle()
    forca.penup()
    forca.setpos(-200,-100)
    forca.pendown()    
    forca.pensize(5)
    forca.left(90)
    forca.forward(200)
    forca.right(90)
    forca.forward(60)
    forca.right(90)
    forca.forward(20)

def cabeca():
    forca = turtle.Turtle()   
    forca.speed(10)    
    forca.hideturtle()
    forca.pensize(5)
    forca.penup()    
    forca.setpos(-140,80)
    forca.left(180)    
    forca.pendown()
    forca.circle(20)
    
    
def corpo():
    forca = turtle.Turtle()    
    forca.hideturtle()
    forca.pensize(5)
    forca.penup()
    forca.setpos(-140,40)
    forca.pendown()
    forca.right(90)
    forca.forward(60)  
    
    
def bracoe():
    forca = turtle.Turtle()
    forca.hideturtle()
    forca.pensize(5)
    forca.penup()
    forca.setpos(-140,35)
    forca.pendown()
    forca.right(30)
    forca.forward(20)
    
    
def bracod():
    forca = turtle.Turtle()
    forca.hideturtle()
    forca.pensize(5)
    forca.penup()
    forca.setpos(-140,35)
    forca.pendown()
    forca.right(150)
    forca.forward(20)
    
    
def pernae():
    forca = turtle.Turtle()
    forca.hideturtle()
    forca.pensize(5)
    forca.penup()
    forca.setpos(-140,-20)
    forca.pendown()
    forca.right(30)
    forca.forward(25)
        

def pernad():
    forca = turtle.Turtle()
    forca.hideturtle()
    forca.pensize(5)
    forca.penup()
    forca.setpos(-140,-20)
    forca.pendown()
    forca.right(150)
    forca.forward(25)
    
janela = turtle.Screen()
janela.bgcolor('blue')
forca() 
escolha = 0


erros = 0
acertos = []    
tentativas = []
digitadas = []
arquivo=open('entrada.csv','r')
leitura=arquivo.read(1000)
l=leitura.split(',')
palavra=random.choice(l).lower()
print(palavra)
numletras = len(palavra)
print (numletras)
    
    
while erros<6:
    forca = turtle.Turtle()
    forca.clear()
    senha = ""    
    for letra in palavra:
        senha += letra if letra in acertos else "  " if letra == (" ") else "_ "
         
        forca.hideturtle()    
        forca.penup()    
        forca.setpos(-500,-200)       
        forca.write(senha, move=False, align="left", font=("Arial", 45, "normal"))
        
    if senha == palavra:
        forca.clear()            
        ganhou = turtle.Turtle()
        ganhou.hideturtle()
        ganhou.penup()    
        ganhou.setpos(-200,-200)    
        ganhou.write('Voce ganhou!', move=False, align="left", font=("Arial", 45, "normal"))
        break
    tentativa= janela.textinput('','Digite uma letra ').lower().strip()
    if tentativa == ('exit'):
        break
    if tentativas in digitadas:
        forca.clear()
        forca.write('Letra ja digitada', move=False, align="left", font=("Arial", 30, "normal"))
        continue
    else:
        digitadas += tentativa
        forca.clear()
        if tentativa in palavra:
            acertos += tentativa
            forca.clear()
        else:
            erros = erros + 1
        if erros == 1:
            cabeca()
        elif erros == 2:
            corpo()
        elif erros == 3:
            bracod()
        elif erros == 4:
            bracoe()
        elif erros == 5:
            pernad()
        elif erros == 6:
            perdeu = turtle.Turtle()
            pernae()
            forca.clear()                
            perdeu.hideturtle()
            perdeu.penup()            
            perdeu.setpos(-200,-200)
            perdeu.write(palavra, move=False, align="left", font=("Arial", 45, "normal"))
            perdeu.setpos(-70,0)
            perdeu.write('voce perdeu', move=False, align="left", font=("Arial", 45, "normal"))



janela.exitonclick()

