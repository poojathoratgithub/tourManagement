from tkinter import *
from sqlite3 import * 
#from PIL import ImageTk, Image

con = connect('Tourist.db')
cur=con.cursor()
cur.execute('create table if not exists tourist1(name text,email text ,username text, password text)')


def Login():

        # frame1=Frame(window,bg="skyblue3",width=200,height=200)
        # frame1.place(x=250,y=150)       
        u=txtusername.get()
        p=txtpassword.get()
        cur.execute('select * from tourist1 where username=? and password=?',(u,p))
        rs=cur.fetchall()
        if len(rs)==0:
                print("Invalid")
        else:
                Home()
        # btnLogin = Button(frame1,command=Mainmenu)
                
        # btnLogin.grid(row=0,column=1)

        frame1.mainloop()


window=Tk()
window.title("Tourist Page ")
window.geometry('800x500')
window.configure(bg="black")
window.resizable(False,False)
frame = Frame(window, width=800, height=800)
frame.pack()
frame.place(anchor='center', relx=0.5, rely=0.5)

##img = ImageTk.PhotoImage(Image.open("E:\\Python\\Mini project\\6871.jpg_wh1200.jpg"))
#img1 = ImageTk.PhotoImage(Image.open("E:\\Python\\Mini project\\travel.jpg"))
#label = Label(frame, image = img1,bg="black",)
#label.pack()
lbl_title=Label(window,text="WELCOME TO LOGIN PAGE",font=20,fg="black",bg="light pink")
lbl_title.place(x=250,y=30,height=30)


frame1=Frame(window,bg="skyblue3",width=200,height=200)
frame1.place(x=250,y=150)

lblusername = Label(frame1,text="Enter Username :",fg="black",bg="light pink3")
txtusername = Entry(frame1)

lblpassword=Label(frame1, text="Enter Password :",fg="black",bg="light pink3")
txtpassword=Entry(frame1,show="*")
btnLogin = Button(frame1,text="Login",command=Login)
#btnLogin1 = Button(frame1,text="enter",command=Verify)
btnSignUp = Button(frame1,text="SignUp",command=Login)

# lbldata= Label(frame1)

lblusername.grid(row=0,column=0,pady=30)
txtusername.grid(row=0,column=2,padx=5)
lblpassword.grid(row=1,column=0,pady=5)
txtpassword.grid(row=1,column=2,padx=5)

btnLogin.grid(row=2,column=0,pady=10)
btnSignUp.grid(row=2,column=2,padx=20)
# lbldata.grid(row=4,column=1)

frame1.mainloop()
window.mainloop()

