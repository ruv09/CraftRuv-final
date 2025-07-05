# 🪑 CraftRuv - Профессиональный конструктор мебели

CraftRuv - это современное веб-приложение для проектирования мебели с использованием ИИ-ассистента. Приложение позволяет создавать 3D модели мебели, рассчитывать материалы и стоимость, а также получать рекомендации от искусственного интеллекта.

## 🚀 Возможности

- **3D Проектирование** - Создание реалистичных 3D моделей мебели
- **ИИ-помощник** - Рекомендации по оптимизации конструкции и материалов
- **AR-предпросмотр** - Просмотр мебели в интерьере через дополненную реальность
- **Автоматические расчеты** - Точный расчет материалов и стоимости
- **Экспорт чертежей** - Готовые чертежи для производства
- **Облачная синхронизация** - Доступ к проектам с любого устройства

## 🛠 Технологии

### Frontend
- React 18 + TypeScript
- Vite для сборки
- Tailwind CSS для стилизации
- Radix UI компоненты
- React Router для навигации
- Lucide React для иконок

### Backend
- Node.js + Express
- MongoDB + Mongoose
- JWT для аутентификации
- Multer для загрузки файлов
- Express Validator для валидации

## 📦 Установка и запуск

### Предварительные требования
- Node.js 18+ 
- MongoDB
- pnpm (рекомендуется) или npm

### 1. Клонирование репозитория
```bash
git clone <repository-url>
cd craftruv-final
```

### 2. Установка зависимостей Frontend
```bash
cd frontend
pnpm install
```

### 3. Настройка Backend
```bash
cd backend
pnpm install
```

Создайте файл `.env` в папке `backend` на основе `env.example`:
```bash
cp env.example .env
```

Отредактируйте `.env` файл:
```env
PORT=5000
NODE_ENV=development
MONGODB_URI=mongodb://localhost:27017/craftruv
JWT_SECRET=your-super-secret-jwt-key-change-this-in-production
FRONTEND_URL=http://localhost:5173
```

### 4. Запуск MongoDB
Убедитесь, что MongoDB запущен на вашей системе:
```bash
# macOS (с Homebrew)
brew services start mongodb-community

# Ubuntu/Debian
sudo systemctl start mongod

# Windows
# Запустите MongoDB как службу
```

### 5. Запуск приложения

#### Запуск Backend
```bash
cd backend
pnpm dev
```

Backend будет доступен по адресу: http://localhost:5000

#### Запуск Frontend
```bash
# В корневой папке проекта
pnpm dev
```

Frontend будет доступен по адресу: http://localhost:5173

## 🗂 Структура проекта

```
craftruv-final/
├── src/                    # Frontend исходный код
│   ├── components/         # React компоненты
│   ├── contexts/          # React контексты
│   ├── pages/             # Страницы приложения
│   ├── hooks/             # Пользовательские хуки
│   └── lib/               # Утилиты и конфигурация
├── backend/               # Backend исходный код
│   ├── src/
│   │   ├── routes/        # API маршруты
│   │   ├── models/        # MongoDB модели
│   │   ├── middleware/    # Express middleware
│   │   └── config/        # Конфигурация
│   └── uploads/           # Загруженные файлы
├── public/                # Статические файлы
└── package.json           # Зависимости проекта
```

## 🔧 API Endpoints

### Аутентификация
- `POST /api/auth/register` - Регистрация пользователя
- `POST /api/auth/login` - Вход в систему
- `GET /api/auth/me` - Получение данных пользователя
- `PUT /api/auth/profile` - Обновление профиля

### Проекты
- `GET /api/projects` - Получение списка проектов
- `POST /api/projects` - Создание нового проекта
- `GET /api/projects/:id` - Получение проекта по ID
- `PUT /api/projects/:id` - Обновление проекта
- `DELETE /api/projects/:id` - Удаление проекта

### Мебель
- `GET /api/furniture/templates` - Получение шаблонов мебели
- `POST /api/furniture/calculate` - Расчет материалов и стоимости

### ИИ
- `POST /api/ai/suggest` - Получение ИИ-рекомендаций
- `POST /api/ai/optimize` - Оптимизация проекта
- `POST /api/ai/validate` - Валидация проекта

## 👥 Пользователи

### Роли пользователей
- **user** - Обычный пользователь (бесплатный план)
- **premium** - Премиум пользователь
- **admin** - Администратор

### Планы подписки
- **free** - Бесплатный план (ограниченные возможности)
- **basic** - Базовый план
- **pro** - Профессиональный план

## 🎨 Особенности интерфейса

- **Адаптивный дизайн** - Работает на всех устройствах
- **Темная/светлая тема** - Автоматическое переключение
- **Современный UI** - Использование последних трендов дизайна
- **Интуитивная навигация** - Простое и понятное управление

## 🔒 Безопасность

- JWT токены для аутентификации
- Хеширование паролей с bcrypt
- Валидация данных на сервере
- Rate limiting для защиты от атак
- CORS настройки для безопасности

## 🚀 Развертывание

### Production сборка Frontend
```bash
pnpm build
```

### Production запуск Backend
```bash
NODE_ENV=production pnpm start
```

## 🤝 Вклад в проект

1. Fork репозитория
2. Создайте ветку для новой функции
3. Внесите изменения
4. Создайте Pull Request

## 📄 Лицензия

MIT License - см. файл LICENSE для подробностей.

## 📞 Поддержка

Если у вас есть вопросы или проблемы:
- Создайте Issue в репозитории
- Обратитесь к документации
- Проверьте логи приложения

---

**CraftRuv** - Превращаем идеи в реальность! 🪑✨
