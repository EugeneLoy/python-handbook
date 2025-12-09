# tkinter - віджет Entry

`Entry` (поле введення) — віджет для створення однострокових полів введення тексту у вікні. Він використовується, коли потрібно отримати текст від користувача, який можна потім обробити або використати в програмі.

## Приклад:

```python
from tkinter import *

window = Tk()
window.geometry("200x100")

label_x = Label(text="x =")
label_x.pack()

entry_x = Entry()
entry_x.pack()

label_r = Label(text="Корень квадратний = ?")
label_r.pack()

def click():
    x = float(entry_x.get())
    r = x ** 0.5
    label_r.configure(text="Корень квадратний = " + str(r))

button = Button(text="Порахувати", command=click)
button.pack()

window.mainloop()
```

Результат:

![Результат](tkinter%20-%20віджет%20Entry/1.png) ![Результат](tkinter%20-%20віджет%20Entry/2.png)

У прикладі поле введення `entry_x` створюється для отримання числа від користувача. Метод `get()` використовується для зчитування тексту з поля, який потім перетворюється на число за допомогою `float()`. Після обчислення квадратного кореня результат виводиться через зміну тексту мітки `label_r`.

## Основні властивості Entry

| Властивість | Опис | Приклад |
| --- | --- | --- |
| `width` | Ширина у символах | `Entry(width=20)` |
| `bg` | Фоновий колір | `Entry(bg="yellow")` |
| `fg` | Колір тексту | `Entry(fg="blue")` |
| `font` | Шрифт (назва, розмір) | `Entry(font=("Arial", 16))` |
| `state` | Стан поля (`"normal"`, `"disabled"`, `"readonly"`) | `Entry(state="disabled")` |
| `show` | Символ для приховання введеного тексту | `Entry(show="*")` |

## Методи Entry

| Метод | Опис | Приклад |
| --- | --- | --- |
| `get()` | Повертає текст з поля | `text = entry.get()` |
| `insert(index, text)` | Вставляє текст у позицію | `entry.insert(0, "Привіт")` |
| `delete(first, last)` | Видаляє символи з позиції first до last | `entry.delete(0, END)` |
| `configure(**options)` | Змінює властивості поля | `entry.configure(bg="yellow")` |

