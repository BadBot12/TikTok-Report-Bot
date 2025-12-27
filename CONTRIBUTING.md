import tkinter as tk
from tkinter import messagebox
import webbrowser

# Fenêtre principale
fenetre = tk.Tk()
fenetre.title("Les Lions de l'Électronique")
fenetre.geometry("450x350")

# Fonctions
def info_app():
    messagebox.showinfo(
        "Information",
        "Cette application aide à comprendre comment signaler un contenu sur TikTok\n"
        "de manière responsable et conforme aux règles."
    )

def guide_signalement():
    messagebox.showinfo(
        "Guide TikTok",
        "Étapes pour signaler un contenu :\n"
        "1. Ouvrir la vidéo\n"
        "2. Appuyer sur 'Partager'\n"
        "3. Choisir 'Signaler'\n"
        "4. Sélectionner la raison appropriée"
    )

def ouvrir_tiktok():
    webbrowser.open("https://www.tiktok.com/safety")

def quitter():
    fenetre.destroy()

# Titre
titre = tk.Label(
    fenetre,
    text="Les Lions de l'Électronique\nTikTok Report Helper",
    font=("Arial", 14, "bold"),
    justify="center"
)
titre.pack(pady=20)

# Boutons
btn_info = tk.Button(fenetre, text="À propos", width=25, command=info_app)
btn_info.pack(pady=5)

btn_guide = tk.Button(fenetre, text="Guide de signalement", width=25, command=guide_signalement)
btn_guide.pack(pady=5)

btn_tiktok = tk.Button(fenetre, text="Ouvrir l’aide TikTok", width=25, command=ouvrir_tiktok)
btn_tiktok.pack(pady=5)

btn_quitter = tk.Button(fenetre, text="Quitter", width=25, command=quitter)
btn_quitter.pack(pady=15)

# Lancer l'application
fenetre.mainloop()
