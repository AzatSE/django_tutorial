## 🚀 Запуск

**1. Скопируйте проект**

```bash
git clone <ССЫЛКА-НА-РЕПОЗИТОРИЙ>
cd <ИМЯ-ПАПКИ-ПРОЕКТА>
```

**2. Создайте и активируйте виртуальное окружение**

```bash
python -m venv venv
```

| Система | Команда активации |
|---------|-------------------|
| Windows | `venv\Scripts\activate` |
| macOS / Linux | `source venv/bin/activate` |

**3. Установите зависимости**

```bash
python -m pip install -r requirements.txt
```

**4. Создайте файл `.env`**

Скопируйте `.env.example` в `.env`:

| Система | Команда |
|---------|---------|
| Windows | `copy .env.example .env` |
| macOS / Linux | `cp .env.example .env` |

**5. Сгенерируйте `SECRET_KEY`**

```bash
python -c "from django.core.management.utils import get_random_secret_key; print(get_random_secret_key())"
```

Скопируйте полученную строку и вставьте в `.env` после `SECRET_KEY=`.
Для `DEBUG` оставьте `True`.

**6. Подготовьте базу и создайте администратора**

```bash
python manage.py migrate
python manage.py createsuperuser
```

**7. Запустите сервер**

```bash
python manage.py runserver
```

## ✅ Проверка

- http://127.0.0.1:8000/polls/ — приложение
- http://127.0.0.1:8000/admin/ — админка (войдите под созданным администратором)

Если всё открывается, вы готовы к уроку 🎉

> **Не работает?** Скопируйте текст ошибки целиком и покажите преподавателю.