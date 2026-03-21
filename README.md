<p align="center">
  <img src="header.svg" width="854" height="150" alt="Ощепков Сергей">
</p>

## О себе
Студент 2 курса УрФУ, направление «Прикладная информатика: Прикладной искусственный интеллект».  
Специализируюсь на разработке ML-решений, дообучении языковых моделей и создании RAG-систем. Ищу возможность применить и углубить навыки в коммерческой разработке.

---

## Технический стек
<div align="center">

| Категория | Технологии |
|-----------|------------|
| **Языки** | <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/> <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black"/> |
| **ML** | <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white"/> <img src="https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white"/> <img src="https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white"/> <img src="https://img.shields.io/badge/PEFT-1C3C3C?style=flat-square&logo=huggingface&logoColor=white"/> <img src="https://img.shields.io/badge/BitsAndBytes-000000?style=flat-square&logo=python&logoColor=white"/> |
| **NLP** | <img src="https://img.shields.io/badge/RAG-00C6FF?style=flat-square&logo=ai&logoColor=white"/> <img src="https://img.shields.io/badge/Qdrant-1A1A1A?style=flat-square&logo=qdrant&logoColor=white"/> <img src="https://img.shields.io/badge/sentence--transformers-FFD21E?style=flat-square&logo=huggingface&logoColor=black"/> |
| **Backend** | <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white"/> <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/> <img src="https://img.shields.io/badge/SQLAlchemy-000000?style=flat-square&logo=sqlalchemy&logoColor=white"/> <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"/> <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white"/> <img src="https://img.shields.io/badge/n8n-1A1A1A?style=flat-square&logo=n8n&logoColor=white"/> |
| **DevOps** | <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white"/> <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/> <img src="https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white"/> <img src="https://img.shields.io/badge/JSON-000000?style=flat-square&logo=json&logoColor=white"/> |
| **GameDev** | <img src="https://img.shields.io/badge/Pygame-000000?style=flat-square&logo=pygame&logoColor=white"/> |

</div>

## Опыт проектов

### Командная разработка
#### 🎲 **Telegram Mini App (D&D с AI-мастером)** — *AI Developer*  
*Стек: Python, PyTorch, PEFT/LoRA, BitsAndBytes, Qdrant, Transformers*

- **Подготовка данных:**
  - Разработал 3 специализированных датасета (Social, Lore, Rules) для дообучения модели
  - Провел статистический анализ для устранения шаблонных фраз и избыточности
  - Оптимизировал датасеты под длину последовательности 512 токенов

- **Fine-tuning с PEFT:**
  - Дообучил Qwen2.5-7B-Instruct с использованием LoRA (библиотека PEFT 0.18.1)
  - Применил 4-битную квантизацию (NF4) через BitsAndBytes для экономии VRAM
  - Результат: 3 адаптера в формате FP16 (~39 МБ каждый)

- **Архитектура ансамбля:**
  - Реализовал rule-based маршрутизатор с динамическим взвешиванием адаптеров
  - Организовал параллельную генерацию ответов от всех специализированных адаптеров
  - Разработал агрегатор с поддержкой стратегий: `concatenate`, `weighted`, `voting`

- **RAG-система:**
  - Интегрировал векторное хранилище Qdrant для поиска по базе знаний D&D
  - Использовал эмбеддинги `paraphrase-multilingual-MiniLM-L12-v2` (384 dim)
  - Внедрил семантический поиск с фильтрацией по типу адаптера

---

#### ⚔️ [**Sword_Fall**](https://github.com/mmobik/Sword_Fall) — *Full-stack Game Developer*  
*Стек: Python, Pygame, JSON, ООП, паттерны проектирования*

2D RPG-игра с модульной архитектурой и системами, приближенными к коммерческой разработке.

**Архитектура:**
- Разработал модульную структуру (`core`, `level`, `UI`, `dialogues`, `items`)
- Реализовал `GameStateManager` для управления состояниями игры
- Создал централизованную конфигурацию с поддержкой локализации

**Системы:**
- **Инвентарь и предметы:** загрузка из JSON (оружие, броня, расходники), сетка 4×32 с drag-and-drop, система экипировки с пересчетом характеристик
- **Сохранения:** полная сериализация состояния (позиция, инвентарь, прогресс диалогов) с обработкой ошибок
- **Диалоги:** система на основе JSON-конфигураций
- **UI/UX:** многоязычный интерфейс (русский/английский), меню настроек, система звука

**Технические решения:**
- Паттерн Observer для системы статистики
- Оптимизация рендеринга (виртуальный экран, масштабирование, кэширование)
- Y-сортировка спрайтов для корректного отображения глубины

---

#### 🧠 **Сервис диагностики меланомы** — *Исследовательский проект*  
*Стек: Python, PyTorch, Pandas*

- Экспериментировал со сверточными нейронными сетями (CNN) для анализа изображений родинок
- Столкнулся с ограничениями малого датасета и проблемой точности
- Получил ценный опыт в подготовке данных и обучении моделей компьютерного зрения

---

### Сводка проектов

| Проект | Период | Статус |
|--------|--------|--------|
| Sword_Fall | 16.01.2025 — н.в. | Активен |
| D&D AI Master | 01.02.2025 — н.в. | Активен |
| Сервис диагностики меланомы | 24.04.2025 — 26.06.2025 | Завершен |
| Pastry_Bot | 01.01.2025 — 20.01.2025 | Завершен |

---

## Образование
🎓 **Уральский федеральный университет (УрФУ)**  
*Прикладная информатика / Прикладной искусственный интеллект*  
2026 – настоящее время

---

### Личные качества

- **Коммуникабельность** — опыт командной разработки, открыт к сотрудничеству
- **Английский язык** — B1 (Intermediate)
- **Алгоритмы и структуры данных** — продвинутый уровень

---

### В настоящее время изучаю

- Автоматизация процессов (n8n)
- Контейнеризация и оркестрация (Kubernetes)
- Сетевое взаимодействие и устройство сетей
- Базы данных и API: Redis, PostgreSQL, FastAPI

---

### Профессиональные интересы

- ИИ-агенты на основе больших данных
- Инструменты автоматизации
- Распределенные системы

---

## Контакты
<div align="center">
  
[![Telegram](https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/mmobik)
[![VK](https://img.shields.io/badge/VK-4680C2?style=for-the-badge&logo=vk&logoColor=white)](https://vk.com/sergeyoshepkov)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:hak189145@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/mmobik)

</div>

<p align="center">
  <i>Открыт к предложениям и сотрудничеству</i>
</p>
