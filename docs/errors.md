# OSError: Cannot open resource
Эта ошибка означает что у вас не установлены шрифты, требуемые при создании цитаты/демотиватора.
При создании демотиватора по умолчанию используется шрифт: times.ttf.
При создании цитаты по умолчанию используются шрифты: verdana.ttf, ariali.ttf (Arial Italic).
Если вы используете Ubuntu, установите шрифты командой: sudo apt-get install msttcorefonts.
Если вы используете Windows, поместите необходимые шрифты в папку рядом с исполняемым python файлом.

# Не отображаются эмоджи при создании демотиватора
... Установите шрифт Symbola.ttf, после укажите данный шрифт в кастомизации.

# Не работает библиотека, что делать?
1. Запускаем код:
```python
from orpl import *

filename = 'filename.png'  # Имя выходного файла

try:
    demotivator = Demotivator('Эй', 'что?')
    demotivator.create(filename)
    
    quote = Quote('Каво', "Молодой чебурек")
    quote.get(filename)
    
    print('Библиотека полностью работает.')
except Exception as e:
    print(e)
```
2. Создаем Issue с ошибкой, если она есть.
