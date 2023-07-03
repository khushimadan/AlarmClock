#Task-1 Building an Alarm Clock

from tkinter import *
import datetime
import time 
from pygame import mixer
import threading
from tkinter import messagebox

root = Tk()
root.title("Alarm Clock")
root.geometry("530x330") #size of the window

alarmtime= StringVar()
msg1= StringVar()

head = Label(root,text="Alarm Clock",font=('comic sans',20))
head.grid(row=0,columnspan=3,pady=10)

mixer.init()

def ala():

    a= alarmtime.get()

    AlarmT = a
    CurrentTime= time.strftime("%H:%M") #getting the current time in the 24 hour format
    
    while AlarmT!=CurrentTime:
        CurrentTime= time.strftime("%H:%M") #updating current time if the current time is not equal to the alarm time
    
    if AlarmT==CurrentTime:
        mixer.music.load('alarm-clock-short-6402.mp3') 
        mixer.music.play() #playing the alarm
        msg= messagebox.showinfo('It is time!',f'{msg1.get()}') #displaying the user input message
        if msg == 'ok':
            mixer.music.stop() #stopping alarm after pressing the okay button

clockimg= PhotoImage(file="clock.png")

img = Label(root,image=clockimg)
img.grid(rowspan=4,column=0)

inputt = Label(root,text="Enter Time :",font=('comic sans',18))
inputt.grid(row=1,column=1)

altime = Entry(root,textvariable=alarmtime,font=('comic sans',18),width=6)
altime.grid(row=1,column=2)

msg = Label(root,text="Message",font=('comic sans',18))
msg.grid(row=2,column=1,columnspan=2)

msginput = Entry(root,textvariable=msg1,font=('comic sans',18))
msginput.grid(row=3,column=1,columnspan=2)

submit = Button(root,text="SUBMIT",font=('comic sans',18),command=ala) #creating the submit button and setting command as ala function
submit.grid(row=4,column=1,columnspan=2)

root.mainloop()   
 










 
