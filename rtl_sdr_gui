import Tkinter as t
import tkMessageBox as mb

## root level window
root = t.Tk()
## frame for window title
f_title = t.Frame(root)
f_title.pack()
## frame for first line of entry
f_body1 = t.Frame(root)
f_body1.pack()
## frame for second line of entry
f_body2 = t.Frame(root)
f_body2.pack()
## frame for second line of entry
f_body3 = t.Frame(root)
f_body3.pack()
## frame for text output
f_output = t.Frame(root)
f_output.pack()

# function for grabbing input from text inputs        
def buttonTest():
    CF = ent_body1.get()
    FS = ent_body2.get()
    n = ent_body3.get()
    if checkInt(CF) == 0 or checkInt(FS) == 0 or checkInt(n):
        return 0
    str_line1 = 'Center Frequency = '+ str(CF) + ' MHz\n'
    str_line2 = 'Sampling Frequency = '+ str(FS) +' MHz\n'
    str_line3 = 'REsampling Frequency = '+ str(n) +'\n'
    txt_output.insert('end', 'Current Configuration \n')
    txt_output.insert('end', str_line1)
    txt_output.insert('end', str_line2)
    txt_output.insert('end', str_line3)

def checkInt(text):
    for char in text:
        if char not in '1234567890':
            mb.showinfo("Error", "Non Integer Value Entered")
            return 0
            
## title on gui window
str_title = 'RTL-SRD Confuguration'
lab_title = t.Label(f_title, text = str_title)
lab_title.pack()

## first body entry
str_body1 = 'Center Freqency: '
lab_body1 = t.Label(f_body1, text = str_body1)
lab_body1.pack(side = 'left')
ent_body1 = t.Entry(f_body1, bd =10)
ent_body1.pack(side = 'left')
lab_body1_2 = t.Label(f_body1, text = 'MHz')
lab_body1_2.pack(side = 'left')

## second body entry
str_body2 = '     sampling rate:'
lab_body2 = t.Label(f_body2, text = str_body2)
lab_body2.pack(side = 'left')
ent_body2 = t.Entry(f_body2, bd =10)
ent_body2.pack(side = 'left')
lab_body2_2 = t.Label(f_body2, text = 'MHz')
lab_body2_2.pack(side = 'left')

## third body entry
str_body3 = '  Resampling rate:'
lab_body3 = t.Label(f_body3, text = str_body3)
lab_body3.pack(side = 'left')
ent_body3 = t.Entry(f_body3, bd =10)
ent_body3.pack(side = 'left')
lab_body3_2 = t.Label(f_body3, text = 'MHz')
lab_body3_2.pack(side = 'left')

## output body entitiy
but_outputSet = t.Button(f_output, text = 'Enter', command = buttonTest)
but_outputSet.pack()
txt_output = t.Text(f_output)
txt_output.pack( side = 'bottom' )

## run mainloop()
root.mainloop()
