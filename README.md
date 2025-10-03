# 🗂️ DB_Manager — SQLite менеджер для проектов

## 📋 Описание

DB_Manager — это простой Python-скрипт для работы с базой данных SQLite, который помогает создавать таблицы для хранения информации о проектах, навыках и статусах.

## 🚀 Быстрый старт

1. Установи Python 3 (если ещё не установлен) 🐍
2. Убедись, что файл `config.py` содержит переменную `DATABASE` с путём к твоей базе данных.
3. Запусти скрипт:

```bash
python db_manager.py
```

После запуска будут созданы следующие таблицы:
- **projects** 📁 — информация о проектах
- **skills** 🛠️ — список навыков
- **project_skills** 🔗 — связь проектов и навыков
- **status** 📊 — статусы проектов

## 🏗️ Структура таблиц

- **projects**:  
  - `project_id` (PK)  
  - `user_id`  
  - `project_name`  
  - `description`  
  - `url`  
  - `status_id` (FK → status.status_id)

- **skills**:  
  - `skill_id` (PK)  
  - `skill_name`

- **project_skills**:  
  - `project_id` (FK → projects.project_id)  
  - `skill_id` (FK → skills.skill_id)

- **status**:  
  - `status_id` (PK)  
  - `status_name`

## ⚙️ Использование

Для создания таблиц просто запусти файл.  
Если нужно изменить структуру — отредактируй методы в классе `DB_Manager`.

## 💬 Обратная связь

Если есть вопросы или предложения — пиши! 😊

---

**Автор:** YUNUSULRTA123
