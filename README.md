# Kapi — Линукс ИИ Ассистент
Kapi — это Линукс ИИ Асистент, написанный на Python, который использует API Together и модель lgai/exaone-3-5-32b-instruct для обработки запросов пользователей. Бот поддерживает диалог на русском языке, сохраняет историю разговоров в файле history.json и автоматически очищает её при завершении работы. Проект разработан в рамках совместной работы для учебных целей.
Основные возможности

💬 Интерактивный диалог: Задавайте вопросы, получайте ответы от ИИ в консоли.

📝 Сохранение истории: История разговоров сохраняется в history.json для поддержки контекста.

🗑️ Очистка истории: История автоматически сбрасывается при выходе из программы.

😊 Настраиваемый тон: Используется системный промт для дружелюбных и лаконичных ответов.

🚀 Лёгкая настройка: Простая установка и запуск в локальной среде.

# Требования

os.ex

Python 3.13 или выше
Библиотека together для работы с API Together
API-ключ от Together AI (см. документацию)

# Установка

Клонируйте репозиторий:
``` bash
git clone https://github.com/<ваш-username>/kapi.git
cd kapi
```


Создайте виртуальное окружение (рекомендуется):
``` bash
python3 -m venv .venv
```
``` bash
source .venv/bin/activate  # Для Linux/Mac
```
``` bash
.venv\Scripts\activate     # Для Windows
```

Установите зависимости:
``` bash
pip install together
```


Настройте API-ключ:

Убедитесь, что в main.py указан ваш API-ключ для Together API_KEY = "ваш-api-ключ"


Получите ключ на https://api.together.xyz.



# Использование

Запустите чат-бот:
``` bash
python3 main.py
```


Взаимодействуйте с ботом:

Введите запрос в консоли:You: Привет, как дела?

Kapi: Привет! 😊 Отлично, а у тебя? Чем могу помочь?


Для выхода введите exit

История очищена.




Особенности:

История разговоров сохраняется в history.json и очищается при завершении.
Ответы генерируются с учётом системного промта для дружелюбного тона.



Структура проекта
kapi/
├── api.py              # Интерфейс для взаимодействия с API Together
├── core.py             # Основная логика чат-бота
├── database.py         # Управление историей разговоров (history.json)
├── interfaces.py       # Абстрактные интерфейсы для компонентов
├── main.py             # Точка входа для запуска чат-бота
├── parser.py           # Парсинг запросов и ответов
├── history.json        # Файл для хранения истории разговоров
├── .gitignore          # Игнорирование временных файлов (__pycache__, *.pyc)
└── README.md           # Документация проекта

# Описание компонентов

api.py: Реализует отправку запросов к API Together с использованием модели deepseek-reasoner.
core.py: Оркестрирует работу парсера, истории и API, включая системный промт.
database.py: Управляет файлом history.json, хранящим историю разговоров.
interfaces.py: Определяет абстрактные интерфейсы для обеспечения модульности.
parser.py: Преобразует текст в JSON и удаляет теги <think> из ответов.
main.py: Запускает консольный интерфейс и очищает историю при выходе.


# Разработка и вклад

Клонируйте и создайте ветку:
``` bash
git checkout -b feature/ваша-фича
```

Внесите изменения и закоммитьте:
``` bash
git add .
```

``` bash
git commit -m "Описание изменений"
```

Отправьте изменения:
В ваш репозиторий:
``` bash
git push myrepo feature/ваша-фича
```

В репозиторий учителя (через PR):
``` bash
git push origin feature/ваша-фича
```



Создайте Pull Request на GitHub:
Перейдите на https://github.com/YegorPanin/kapi (или ваш форк).
Создайте PR из вашей ветки в main.


😊 Kapi готов помочь вам в обучении и экспериментах с ИИ!
