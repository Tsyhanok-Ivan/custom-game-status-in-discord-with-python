# Посібник про те як налаштувати свій ігровий статус у Discord.

### Крок 1: 
#### Створіть додаток на сайті [discord.com/developers](https://discord.com/developers/applications)
![img](https://i.imgur.com/EFq1twc.gif)

---

### Крок 2:
#### Додайте зображення
![img](https://i.imgur.com/wSSKzau.png)

---

### Крок 3:
#### Завантажите бібліотеку pypresence
`pip install pypresence`

---

### Крок 4:
#### Получіть client id
![img](https://i.imgur.com/J4ajeya.png)

---

### Крок 5:
#### Запишіть цей код і замініть значення на свої власні:
```py
from pypresence import Presence
from time import time

presence = Presence("")  # client id тут

buttons = [  # maximum 2 buttons
    {
        "label": "Button 1",  # ім'я кнопки
        "url": "https://none.com/"  # посилання кнопки
    },
    {
        "label": "Button 2",  # ім'я кнопки
        "url": "https://none.com/"  # посилання кнопки
    }
]


presence.connect()  # підключення
presence.update(  # перший рядок у статусі - назва програми
    state="status",  # тдругий рядок за статусом
    start=time(),  # таймер запуску
    buttons=buttons,  # підключення кнопок
    large_image="img_1",  # велике зображення, введіть його назву з кроку 2 в large_image
    small_image="img_2",  # маленьке зображення, введіть його назву з кроку 2 в small_image
    large_text="large_image_text",  # текст при наведенні на велике зображення
    small_text="small_image_text"  # текст при наведенні на маленьке зображення
)

input()
```

---

### Крок 6:
#### Запускаємо, мої результати:
![img](https://i.imgur.com/rMV0BHk.png)

---

#### Використовував:
`python 3.9`
`pypresence 4.3.0`
