
# Basic Settings
ctk.set_appearance_mode("dark")
ctk.set_default_color_theme("blue")

class App(ctk.CTk):
    def __init__(self):
        super().__init__()
        self.title("Kaushik's UI Project")
        self.geometry("400x480")

        # UI Elements
        self.label = ctk.CTkLabel(self, text="Welcome Back", font=("Roboto", 24))
        self.label.pack(pady=40)

        self.entry1 = ctk.CTkEntry(self, placeholder_text="Username", width=250)
        self.entry1.pack(pady=12)

        self.entry2 = ctk.CTkEntry(self, placeholder_text="Password", show="*", width=250)
        self.entry2.pack(pady=12)

        self.button = ctk.CTkButton(self, text="Login", command=self.login, width=200)
        self.button.pack(pady=24)

        self.checkbox = ctk.CTkCheckBox(self, text="Remember Me")
        self.checkbox.pack(pady=10)

    def login(self):
        print("Login Attempted!")

if __name__ == "__main__":
    app = App()
    app.mainloop()
