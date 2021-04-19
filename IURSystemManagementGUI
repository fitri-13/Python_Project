import tkinter
from tkinter import *
from tkinter import font
from PIL import Image, ImageTk
import tkinter as tk
from tkinter import messagebox
from threading import Timer
import time

def InputData():
    registWindow.withdraw()
    buttonFont = font.Font(family='Calibri', size=12, weight='bold')
    inputdata = tkinter.Toplevel(mainWindow, width=wWindow, height=hWindow, highlightthickness=0)
    inputdata.geometry('%dx%d' % (wWindow, hWindow))
    inputdata['background'] = '#ffffff'
    inputdata.title("Input Data")
    inputdata.resizable(width=False, height=False)
    inputdata.iconbitmap('HP.ico')

    titleB = tkinter.Button(inputdata, state="disable", bd='0', bg='#365685', height=2, width=int(wWindow))
    titleB.place(x=0, y=0)

    # titleD = tkinter.Button(inputdata, state="disable", bd='0', bg='#000001', height=2, width=int(wWindow))
    # titleD.place(x=0, y=hWindow - 35)

    title = tkinter.Label(inputdata, text=" INPUT INFORMATION ", bg='#365685', fg='#ffffff', font=titleFont)
    title.place(x=wWindow / 2.7, y=-2)

    serialNumber = tkinter.Label(inputdata, text='Serial Number', bg='#ffffff', fg='#121212', font=buttonFont)
    serialNumber.place(x=20, y=hWindow / 4)

    serialnumbertext = tkinter.Entry(inputdata, bd=1, bg="#DFE0E1", fg='#121212', width=30)
    serialnumbertext.place(x=w / 10, y=h / 8)

    productName = tkinter.Label(inputdata, text='Product Name', bg='#ffffff', fg='#121212', font=buttonFont)
    productName.place(x=20, y=hWindow / 3)

    productNameText = tkinter.Entry(inputdata, bd=1, bg="#DFE0E1", fg='#121212', width=30)
    productNameText.place(x=w / 10, y=h / 6)

    sKUNumber = tkinter.Label(inputdata, text='SKU Number', bg='#ffffff', fg='#121212', font=buttonFont)
    sKUNumber.place(x=20, y=hWindow / 2.4)

    sKUNumberText = tkinter.Entry(inputdata, bd=1, bg="#DFE0E1", fg='#121212', width=30)
    sKUNumberText.place(x=w / 10, y=h / 4.8)

    phase = tkinter.Label(inputdata, text='Phase', bg='#ffffff', fg='#121212', font=buttonFont)
    phase.place(x=20, y=hWindow / 2)

    phaseText = tkinter.Entry(inputdata, bd=1, bg="#DFE0E1", fg='#121212', width=30)
    phaseText.place(x=w / 10, y=h / 4)


def Registration():
    # mainWindow.withdraw()
    welcome.destroy()
    registtitle = font.Font(family='Century Gothic', size=20, weight='bold')
    textTitle = font.Font(family='Century Gothic', size=9, weight='bold')
    global registWindow
    registWindow = tkinter.Toplevel(mainWindow, width=w / 3, height=h / 3, highlightthickness=0)
    registWindow['background'] = '#ffffff'
    registWindow.title("Login")
    registWindow.resizable(width=False, height=False)
    registWindow.iconbitmap('HP.ico')

    titleB = tkinter.Button(registWindow, state="disable", bd='0', bg='#365685', height=2, width=int(wWindow))
    titleB.place(x=0, y=0)

    title = tkinter.Label(registWindow, text="ADMIN LOGIN", bg='#365685', fg='#ffffff', font=registtitle)
    title.place(x=w / 8, y=-1)

    usernameText = tkinter.Entry(registWindow, text="username", bd=2, fg='#000001', width=25)
    usernameText.place(x=w / 7.5, y=h / 8)
    usernameTitle = tkinter.Label(registWindow, text="E-mail", bg='#ffffff', fg='#2e2e2e', font=textTitle)
    usernameTitle.place(x=w / 9.5, y=h / 8)

    passText = tkinter.Entry(registWindow, text="password", bd=2, fg='#000001', show="*", width=25)
    passText.place(x=w / 7.5, y=h / 6)
    passTitle = tkinter.Label(registWindow, text="Password", bg='#ffffff', fg='#2e2e2e', font=textTitle)
    passTitle.place(x=w / 10.4, y=h / 6)

    loginButton = tkinter.Button(registWindow, text='  Login  ', bg='#365685', fg='#ffffff', bd='1', font=buttonFont,
                                 command=InputData)
    loginButton.place(x=w / 6.7, y=h / 4)
    loginButton.bind("<Enter>", on_enter)
    loginButton.bind("<Leave>", on_leave)

def CloseWindow():
    MsgBox = tk.messagebox.askquestion('Close Window', 'Are you sure you want to close the window?', icon='warning')
    if MsgBox == 'yes':
        mainWindow.destroy()
    else:
        tk.messagebox.showinfo('Return', 'Please click "Registration" button to continue')

def on_enter(e):
    e.widget['background'] = '#142964'

def on_leave(e):
    e.widget['background'] = '#365685'


mainWindow = Tk()
w, h = mainWindow.winfo_screenwidth(), mainWindow.winfo_screenheight()
canvas = tk.Canvas(mainWindow, width=w, height=h, highlightthickness=0)
canvas.pack()
canvas.configure(background='#365685')
mainWindow.title('BPS IUR Management System')
mainWindow.resizable(width=False, height=False)
mainWindow.focus_set()
mainWindow.geometry("%dx%d+0+0" % (w, h))
mainWindow.iconbitmap('HP.ico')

imageFile = Image.open("pict10.png")
imgWidth, imgHeight = imageFile.size
ratio = min(w / imgWidth, h / imgHeight)
imgWidth = int(imgWidth * ratio)
imgHeight = int(imgWidth * ratio)
image = ImageTk.PhotoImage(imageFile)
canvas.create_image(w / 2, h / 2, image=image)

ww = int(w / 30)
hh = int(h / 40)
wWindow = w / 2
hWindow = h / 2

welcome = tkinter.Label(mainWindow, width=ww, height=hh, bd=0, bg='#ffffff')
welcome.place(x=w / 2.7, y=h / 4)

infoFont = font.Font(family='Calibri', size=10)
titleFont = font.Font(family='Calibri', size=20, weight='bold')
buttonFont = font.Font(family='Calibri', size=11)

info = tkinter.Label(mainWindow,
                     text="HP BPS IUR Management System powered by BPS Factory Enablement \n version 21.04.06.a",
                     bd='0', bg='#365685', fg="#272426", font=infoFont)
info.place(x=w / 2.62, y=h / 1.2)

title = tkinter.Label(welcome, text="Welcome to IUR MS", bd='0', bg='#ffffff', fg="#121212", font=titleFont)
title.place(x=ww * 1.6, y=hh * 6)

registButton = tkinter.Button(welcome, text='    Registration    ', bg='#365685', fg='#ffffff', bd='0', font=buttonFont,
                              command=Registration)
registButton.place(x=ww * 2.5, y=hh * 10)
registButton.bind("<Enter>", on_enter)
registButton.bind("<Leave>", on_leave)

cancelbutton = tkinter.Button(welcome, text='    Cancel    ', bg='#365685', fg='#ffffff', bd='0', font=buttonFont,
                              command=CloseWindow)
cancelbutton.place(x=ww * 2.75, y=hh * 12)
cancelbutton.bind("<Enter>", on_enter)
cancelbutton.bind("<Leave>", on_leave)

img = tk.PhotoImage(file="HP-min.png")
img = img.zoom(1)
img = img.subsample(45)
logo = tkinter.Button(welcome, image=img, bg='#ffffff', fg='#ffffff', bd='0', font=buttonFont)
logo.place(x=ww * 3, y=hh * 2)

date_clock = tk.Label(mainWindow, bg='steelblue', fg='white', font='helvetica 12', relief=tk.SUNKEN, border=0)
date_clock.place(x=w / 2.28, y=h / 1.1)

def date_time():
    curr_time = (time.strftime('%a, %d %b %Y. %H:%M:%S'))
    date_clock.config(text=curr_time, font=infoFont, bg='#365685', fg='#272426')  # Print updated clock.
    t = Timer(1.0, date_time)
    t.setDaemon(True)
    t.start()
date_time()

mainWindow.mainloop()
