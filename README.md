import tkinter as tk
import random
#隨機改變按鈕的位置
def move_no_button():
    x = random.randint(0, 300)
    y = random.randint(0, 200)
    no_button.place(x=x, y=y)
#結果
def on_yes():
    result_label.config(text="我就知道你想給我票")
#建造視窗
window = tk.Tk()
window.title("答非所問")
window.geometry("600x400")
#問題標籤
question_label = tk.Label(window, text="要不要給我周杰倫的票?", font=("Arial", 16))
question_label.pack(pady=20)
#肯定按鈕
yes_button = tk.Button(window, text="要", command=on_yes, width=10, height=2, bg="lightblue", fg="black")
yes_button.pack(side=tk.LEFT, padx=50, pady=20)
#否定按鈕
no_button = tk.Button(window, text="不要", command=move_no_button, width=10, height=2, bg="pink", fg="black")
no_button.place(x=200, y=150)

result_label = tk.Label(window, text="")
result_label.pack(pady=20)
#主迴圈
window.mainloop()
