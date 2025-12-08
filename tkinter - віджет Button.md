# tkinter - віджет Button

`Button` (кнопка) — віджет для створення інтерактивних кнопок у вікні. Він використовується, коли потрібно додати дію, яка виконується після натискання користувачем.

## Приклад:

```python
from tkinter import *

window = Tk()
window.geometry("200x100")

label = Label(text="кнопку не натиснено")
label.pack()

def click():
    label.configure(text="кнопку натиснуто")

button = Button(text="Натисни мене", command=click)
button.pack()

window.mainloop()
```

Результат:

![Результат](tkinter%20-%20віджет%20Button/1.png) ![Результат](tkinter%20-%20віджет%20Button/2.png)

У прикладі кнопка отримує основні властивості - `text` задає напис на кнопці, а `command` визначає функцію `click`, яка викликається при натисканні та змінює текст мітки.

## Основні властивості Button

| Властивість | Опис | Приклад |
| --- | --- | --- |
| `text` | Текст на кнопці | `Button(text="Натисни")` |
| `command` | Функція, яка викликається при натисканні | `Button(text="Натисни", command=my_function)` |
| `bg` | Фоновий колір | `Button(text="Натисни", bg="yellow")` |
| `fg` | Колір тексту | `Button(text="Натисни", fg="blue")` |
| `font` | Шрифт (назва, розмір) | `Button(text="Натисни", font=("Arial", 16))` |
| `width` | Ширина у символах | `Button(text="Натисни", width=20)` |
| `height` | Висота у символах | `Button(text="Натисни", height=2)` |
| `padx`, `pady` | Внутрішні відступи | `Button(text="Натисни", padx=10, pady=5)` |
| `state` | Стан кнопки (`"normal"`, `"disabled"`) | `Button(text="Натисни", state="disabled")` |
