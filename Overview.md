
 <br />

## 1. What package/library was selected?
The package selected is Tkinter. <br />

<img src="https://github.com/CS2613-FA23/explorationactivity1-SubyDoo/assets/93729876/30de9af0-5b4f-4227-b76f-80420ecc2f1e" width=20% height=20%>

 <br />
 



## 2. What is the package/library and functionality?

- What purpose does it serve

  Tkinter (TK interface) is the only graphical user interface (GUI) functionality that comes in python's standard library. It is a wrapper for an extension called TK of another programming language called TCL and implements its widgets as classes in python [1].
  Tkinter uses a window as the foundation and widgets to provide functionalily while adding its own logic over the TCL functionality [3]. It is lightweight and so it is beginner friendly, however, it does have an outdated look/functionality where some other popular 3rd party python GUI libraries don't suffer from [2].


- How do you use it

The GUI in Tkinter is basically A window with widgets/frames that have functionality and/or design.
 <br />

<img src="https://github.com/CS2613-FA23/explorationactivity1-SubyDoo/assets/93729876/4492789c-64a2-49b1-b3ac-e00c85e9e78f" width=80% height=80%> <br />
Description: image of program for reference
<img src="https://github.com/CS2613-FA23/explorationactivity1-SubyDoo/assets/93729876/cfbd11f9-b691-495f-a4ad-03dc6212f963" width=80% height=80%> <br />
Description: schematics of program in terms of grid rows and columns and its widgets/frames <br />
 <br />

In order to use TKinter you need to import it.
```
import tkinter as tk
```
 <br />

The GUI begins with a root, this is the main window that will be worked in.
```
root = tk.Tk()
```
 <br />

You can change the starting window size with geometry("widthxheight") and you can set the title with title().
```
root.geomety("300x200")
root.title("Sentence Report")
```
 <br />


In order to position the label and entry together in a grid we need to combine them in frame, this can be seen as a
container for more frames or widgets.
```
inputFrame = tk.Frame(root)
```
 <br />

You can display text with a Label(). You need the text= so that the function knows what that string is used for.
The justify and anchor parameter is make sure the left is positioned and aligned from the left, anchor uses compass directions. After creating the label you can add it to the frame and give its row and column position. 
Any other widget/frame should have a different position otherwise it will be overwritten.
The padx paramter is there so that there is 10px of spacing from the border and other widgets. 

```
label1 = tk.Label(inputFrame, text="Input a sentence for statistics:", justify="left", anchor="w")
label1.grid(sticky="w", row=0, column=0, padx=10)
```
 <br />


Here we are creating and adding an entry which is a textbox that takes user input. The sticky parameter makes
sure that the widget is aligned to the left of the cell. To get the text from the entry you can use get().
```
input_Entry = tk.Entry(inputFrame, width=50)
input_Entry.grid(sticky="w", row=0, column=1, padx=10)

inputString = input_Entry.get()
```
 <br />


Here we are adding the frame into the root window
```
inputFrame.grid(row=0, column=0)
```
 <br />


Here we are creating a button and adding it to a button frame. Here we set the text of the button, set the
color of it using hex, and finally creating a click event handler (command) which points to the function clear.
If you needed to pass a parameter, you would do "command=lambda: function_name(args)" instead.
```
#function for the clear button action
def clear():
    input_Entry.delete(0, "end")

exit_button = tk.Button(buttonFrame, text="Clear Text", bg="#69b2bf", command=clear)
exit_button.grid(sticky="w", row=0, column=1)
```
 <br />



This is an important component in creating the GUI. This mainloop() is necessary for the window/widgets to be drawn
and for events to be captured.
```
root.mainloop()
```
 <br />



 <br />
Refereces: <br />
[1]https://docs.python.org/3/library/tk.html#:~:text=Tk%2FTcl%20has%20long%20been,and%20the%20tkinter.ttk%20modules.  <br />
[2] https://realpython.com/python-gui-tkinter/ <br />
[3] https://docs.python.org/3/library/tkinter.html <br />
[image] https://collinjoel.medium.com/tkinter-quickstart-guide-3c81348a5b7 <br />
 
 <br />






 
## 3. When was it created?
Tkinter has been part of Python's standard library since version 1.1 released in 1994 [1][2]. 

Refereces: <br />
[1] https://subscription.packtpub.com/book/programming/9781788835886/1/ch01lvl1sec10/introducing-tkinter-and-tk <br />
[2] https://python-course.eu/tkinter/
 
 <br />








 
## 4. Why did you select this package/library
I selected this library because I am currently learning to create UI in Java with JavaFX. When I was first learning java, the process of creating a GUI with javaFX was more of a challenge to understand.
Since taking this class, I had the chance to learn python more and now prefer it over java because of the simplicity to do something. I wanted to see if this is the case as well with UI creation. I also would like to
create more complex GUI based programs in Python related to data extraction and representation in the future.

 <br />







## 5. How did learning the package/library influence your learning of the language?
Using Tkinter helped me further understand interactive programs in python and the similarity it has with that I already knew in JavaFX. The was the first time I read through the documentation of a library to a greater extent so I 
learned how some python libraries are structured. This may help me when looking at future python libraries.


 <br />






 
## 6. How was your overall experience with the package/library?
- When would you recommend this package/library to someone?
I would recommend this package to someone who prefers python over java and who has no experience with graphical user interfaces and would like an intoduction. The simplicity of this library makes it easy to understand
however, it may take some trial and error to get the grid placement for widgets in the right spot. I did not like the error details you would get when you did something wrong as it didn't help me identify the issue without research.

- Would you continue using this package/library? Why or why not?
I would continue using this package but not for much longer as I would like to move to more modern/complex GUI libraries to create better looking programs. Since I am already learning the fundamentals in JavaFX I think it would be better to
move on to something more advanced in a language I prefer more.


 <br />

 
