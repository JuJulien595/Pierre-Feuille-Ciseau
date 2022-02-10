from tkinter import *

from random import randint

from tkinter import ttk

window = Tk()
window.title ("Misaraka Production : Pierre, Feuille, Ciseau")
window.geometry("500x600")
window.iconbitmap ('master.ico.ico')
# Change fond d'écran :
window.config(bg="white")

# Insertion des images :
Pierre = PhotoImage(file='Screenshot_3.png')
Feuille = PhotoImage(file='Screenshot_1.png')
Ciseau = PhotoImage(file='Screenshot_2.png')

# Attribution des images à leurs noms :
image_list = [Pierre, Feuille, Ciseau]

pick_number = randint(0,2)

image_label = Label(window, image=image_list[pick_number], bd=0)
image_label.pack(pady=20)

def spin():
    pick_number = randint(0, 2)
    image_label.config(image=image_list[pick_number])

    if user_choice.get() == "Pierre" :
        user_choice_value = 0
    elif user_choice.get() == "Feuille" :
        user_choice_value = 1
    elif user_choice.get() == "Ciseau":
        user_choice_value = 2

# L'utilisateur utilise la Pierre :
    if user_choice_value ==0 : #Pierre
        if pick_number == 0:
            win_lose_label.config(text="Il y à EGALITE! recommence...")
        elif pick_number == 1:
            win_lose_label.config(text="La feuille couvre la pierre, Vous avez PERDU...")
        elif pick_number == 2:
            win_lose_label.config(text="La pierre casse le ciseau, Vous avez GAGNEZ!!")

    # L'utilisateur utilise la Feuille :
    if user_choice_value ==1 : #Feuille
        if pick_number == 1:
            win_lose_label.config(text="Il y à EGALITE! recommence...")
        elif pick_number == 0:
            win_lose_label.config(text="La feuille couvre la pierre, Vous avez GAGNEZ!!")
        elif pick_number == 2:
            win_lose_label.config(text="Le ciseau coupe la feuille, Vous avez PERDU...")

    # L'utilisateur utilise le ciseau :
    if user_choice_value ==2 : #Ciseau
        if pick_number == 2:
            win_lose_label.config(text="Il y à EGALITE! recommence...")
        elif pick_number == 0:
            win_lose_label.config(text="La pierre casse le ciseau, Vous avez PERDU...")
        elif pick_number == 1:
            win_lose_label.config(text="Le ciseau coupe la feuille, Vous avez GAGNEZ!!")


user_choice = ttk.Combobox(window, values=("Pierre", "Feuille", "Ciseau"))
user_choice.current(0)
user_choice.pack(pady=20)

spin_button = Button(window, text="Recommencer!", border=0, command=spin)
spin_button.pack(pady=10)

win_lose_label = Label(window, text="", font=("Helvetica", 18), bg="white")
win_lose_label.pack(pady=50)




window.mainloop()
