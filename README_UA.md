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

presence = Presence("")  # client id here

buttons = [  # maximum 2 buttons
    {
        "label": "Button 1",  # button name
        "url": "https://none.com/"  # button url
    },
    {
        "label": "Button 2",  # button name
        "url": "https://none.com/"  # button url
    }
]


presence.connect()  # connect
presence.update(  # the first line in the status is the application name
    state="status",  # third line in status
    details="details",  # second line in the status
    start=time(),  # start timer
    buttons=buttons,  # button connection
    large_image="img_1",  # large image, enter its name in large_image
    small_image="img_2",  # small image, enter its name in small_image
    large_text="large_image_text",  # text when hovering over a large image
    small_text="small_image_text"  # text when hovering over a small image
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
