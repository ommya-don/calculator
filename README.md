# calculator
from tkinter import * 

window=Tk()
window.geometry("400x400")
window.title("Harsh Site")
window.config(bg="brown")
 

def click(num):
    result=e1.get()
    e1.delete(0, END)
    e1.insert(0 , str(result)+str(num) )
  
#button  
button1=Button(window , text="1" , bg="orange" , font=("bold",15) ,width=6, height=2 , command=lambda:click(1)) 
button2=Button(window , text="2" , bg="orange" , font=("bold",15) ,width=6, height=2 ,command=lambda:click(2)) 
button3=Button(window , text="3" , bg="orange" , font=("bold",15) ,width=6, height=2 ,command=lambda:click(3)) 
button4=Button(window , text="4" , bg="orange" , font=("bold",15) ,width=6, height=2 ,command=lambda:click(4)) 
button5=Button(window , text="5" , bg="orange" , font=("bold",15) ,width=6, height=2,command=lambda:click(5)) 
button6=Button(window , text="6" , bg="orange" , font=("bold",15) ,width=6, height=2, command=lambda:click(6)) 
button7=Button(window , text="7" , bg="orange" , font=("bold",15) ,width=6, height=2 , command=lambda:click(7)) 
button8=Button(window , text="8" , bg="orange" , font=("bold",15) ,width=6, height=2 , command=lambda:click(8)) 
button9=Button(window , text="9" , bg="orange" , font=("bold",15) ,width=6, height=2 , command=lambda:click(9)) 
button0=Button(window , text="0" , bg="orange" , font=("bold",15) ,width=19, height=2 , command=lambda:click(0))

#OPERATORS
def add () : 
    n1=e1.get()
    global math
    math="addition"
    global i 
    i=int(n1)
    e1.delete(0 , END)  
button13=Button(window, text="+" , bg= "orange", font=("bold",15) , width=6, height=2, command=add)
def sub() : 
    n1=e1.get()
    global math 
    math="subtraction"
    global i 
    i=int(n1)
    e1.delete(0 , END)  
button14=Button(window, text="-" , bg= "orange", font=("bold",15) , width=6, height=2 , command=sub)
def mul () : 
    n1=e1.get()
    global math
    math="multiplication"
    global i 
    i=int(n1)
    e1.delete(0 , END)  
button15=Button(window, text="x" , bg= "orange", font=("bold",15) , width=6, height=2 , command=mul)
def div () : 
    n1=e1.get()
    global math 
    math="division"
    global i 
    i=int(n1)
    e1.delete(0 , END) 
 
button16=Button(window, text="/" , bg= "orange", font=("bold",15) , width=6, height=2 , command=div)

def equal():
    n2=e1.get()
    e1.delete(0, END)
    if math=="addition" :
        e1.insert(0,i+ int(n2))
    elif math=="subtraction" :
        e1.insert(0, i - int (n2))
    elif math=="multiplication" :
        e1.insert(0, i* int(n2))
    elif math=="division" : 
        e1.insert(0, i / int(n2))
           
button12=Button(window, text="=" , bg= "orange", font=("bold",15) , width=12, height=2 , command=equal)
def clear():
    e1.delete(0,END)
button121=Button(window, text="clear" , bg= "orange", font=("bold",15) , width=12, height=2 , command=clear)





e1=Entry(window , width=45 , borderwidth=6)


button1.place(x=50 , y= 100)
button2.place(x=120, y=100)
button3.place(x=190, y=100)
button4.place(x=50 , y= 160)
button5.place(x=120 , y=160)
button6.place(x=190 , y=160)
button7.place(x=50, y= 220)
button8.place(x=120 , y= 220)
button9.place(x=190 , y= 220)

button0.place(x=50, y= 280)
button12.place(x=50 , y= 342)
button13.place(x=260 , y=100)
button14.place(x=260, y=160)
button15.place(x=260 , y= 220)
button16.place(x=260 , y=280)
button121.place(x=192, y=342)
e1.place(x=50 , y= 50)




mainloop()







