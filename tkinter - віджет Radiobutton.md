# tkinter - віджет Radiobutton

`Radiobutton` (радіокнопка) — віджет для створення групи взаємовиключних варіантів вибору у вікні. Він використовується, коли потрібно запропонувати користувачу вибір лише одного варіанту з кількох можливих. Коли один радіокнопка активується, інші в тій же групі автоматично деактивуються.

## Приклад:

```python
from tkinter import *

window = Tk()

label = Label(text="Текст", bg="blue")
label.pack()

color = StringVar()
color.set("blue")

def change_color():
    label.configure(bg=color.get())

radio_b = Radiobutton(
    text="Синій",
    variable=color,
    value="blue",
    command=change_color
)
radio_b.pack()

radio_y = Radiobutton(
    text="Жовтий",
    variable=color,
    value="yellow",
    command=change_color
)
radio_y.pack()

window.mainloop()
```

Результат:

![Результат](tkinter%20-%20віджет%20Radiobutton/1.png) ![Результат](tkinter%20-%20віджет%20Radiobutton/2.png)

У прикладі створюється змінна `color` типу `StringVar()`, яка зберігає значення вибраної радіокнопки. Дві радіокнопки (`radio_b` та `radio_y`) пов'язані з цією змінною через аргумент `variable`. Аргумент `value` вказує значення, яке змінна отримає при виборі цієї радіокнопки. При зміні вибору викликається функція `change_color`, яка змінює фон мітки на колір, що відповідає вибраній радіокнопці.

## Основні властивості Radiobutton

| Властивість | Опис | Приклад |
| --- | --- | --- |
| `text` | Текст біля радіокнопки | `Radiobutton(text="Варіант 1")` |
| `variable` | Змінна типу `StringVar()`, `IntVar()` або `BooleanVar()` для зберігання значення | `Radiobutton(text="Варіант 1", variable=var)` |
| `value` | Значення, яке змінна отримає при виборі цієї радіокнопки | `Radiobutton(text="Варіант 1", variable=var, value="1")` |
| `command` | Функція, яка викликається при виборі радіокнопки | `Radiobutton(text="Варіант 1", command=my_function)` |
| `bg` | Фоновий колір | `Radiobutton(text="Варіант 1", bg="yellow")` |
| `fg` | Колір тексту | `Radiobutton(text="Варіант 1", fg="blue")` |
| `font` | Шрифт (назва, розмір) | `Radiobutton(text="Варіант 1", font=("Arial", 16))` |
| `state` | Стан радіокнопки (`"normal"`, `"disabled"`) | `Radiobutton(text="Варіант 1", state="disabled")` |

## Методи Radiobutton

| Метод | Опис | Приклад |
| --- | --- | --- |
| `configure(**options)` | Змінює властивості радіокнопки | `radio.configure(bg="yellow")` |
| `select()` | Вибирає радіокнопку | `radio.select()` |
| `deselect()` | Скасовує вибір радіокнопки | `radio.deselect()` |

