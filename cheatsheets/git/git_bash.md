## 🔥 **Команды**

---

### 📂 **Конфигурация Git (имя, email, конфиги)**

#### Проверка установки и справка
```bash
# Проверка установлен ли git
git

# Краткая справка
git -h

# Помощь по командам
git --help
```

#### Глобальные настройки
```bash
# Установить глобальное имя и email
git config --global user.name "Pragmatic Programmer"
git config --global user.email "prag_prog@gmail.com"

# Включить цветной интерфейс
git config --global color.ui true

# Установить редактор по умолчанию (например, VS Code)
git config --global core.editor "code --wait"
```

#### Локальные настройки (внутри репозитория)
```bash
# Установить имя/email только для этого проекта
git config user.name "Pragmatic Programmer"
git config user.email "prag_prog@gmail.com"
```

#### Просмотр текущих настроек
```bash
# Все настройки (по умолчанию — глобальные и локальные)
git config --list

# Только имя/email
git config user.name
git config user.email

# Только глобальные
git config --global --list

# Только локальные
git config --local --list
```

#### Где хранятся конфиги
```bash
# Системный конфиг
cat /etc/gitconfig

# Глобальный конфиг
cat ~/.gitconfig

# Локальный конфиг
cat .git/config
```
1. Системные настройки (для всех пользователей)  
`C:\Program Files\Git\etc\gitconfig`

2. Глобальные настройки (для текущего пользователя)  
`%USERPROFILE%\.gitconfig`

3. Локальные настройки (для конкретного репозитория)  
`<Путь_к_репозиторию>\.git\config`

---

### 📂 **Создание и контроль репозитория**

#### Полный цикл создания нового репозитория
```bash
# Создать директорию и перейти в неё
mkdir first_project && cd first_project

# Инициализировать репозиторий
git init

# Создать файл и добавить в индекс
touch README.md
git add README.md

# Сделать первый коммит
git commit -m "initial commit"

# Проверить состояние
git status
```

---

### 📂 **Работа с локальным репозиторием (изменения и история)**

#### Добавление и коммиты
```bash
# Проверить состояние
git status

# Добавить файл или все файлы
git add page1.html
git add .

# Сделать коммит
git commit -m "обновил содержимое"
```

#### История и содержимое
```bash
# История коммитов
git log

# Сжатый формат истории
git log --oneline

# Посмотреть содержимое файла
cat page1.html
```

---

### 📂 **Работа с удалённым репозиторием (push, clone, pull)**

#### Отправка изменений
```bash
# Проверить состояние
git status

# Добавить все изменения
git add .

# Сделать коммит
git commit -m "обновил проект"

# Отправить на GitHub
git push
```

#### Клонирование и обновление
```bash
# Склонировать репозиторий с GitHub
git clone https://github.com/<твой_логин>/study_vault.git

# Перейти в каталог проекта
cd study_vault

# Получить последние изменения
git pull
```

---

### 📂 **Работа с ветками**
```bash
# Создать новую ветку и перейти на неё
git checkout -b feature/login

# Переключиться на другую ветку
git checkout main

# Посмотреть список всех веток
git branch

# Удалить локальную ветку
git branch -d old-branch

# Слить ветку в текущую
git merge feature/login
```

---

### 📂 **Откат изменений**
```bash
# Отменить изменения в файле (если не закоммичено)
git checkout -- index.html

# Убрать файл из индекса, не удаляя его
git reset index.html

# Удалить последний коммит, оставить изменения
git reset --soft HEAD~1

# Полный откат последнего коммита и изменений
git reset --hard HEAD~1
```

---

### 📂 **Временное сохранение (stash)**
```bash
# Спрятать текущие изменения
git stash

# Показать список сохранений
git stash list

# Вернуть последнее сохранение
git stash pop
```

---

### 📂 **Игнорируемые файлы (.gitignore)**

Пример файла `.gitignore`:
```bash
__pycache__/
*.log
.env
*.sqlite
node_modules/
```

```bash
# Создать файл и записать правило
touch .gitignore
echo "*.log" >> .gitignore

# Добавить и закоммитить
git add .gitignore
git commit -m "добавил gitignore"
```

---

### 📂 **SSH-ключи для GitHub**
```bash
# Сгенерировать SSH-ключ
ssh-keygen -t ed25519 -C "your_email@example.com"

# Запустить ssh-agent
eval "$(ssh-agent -s)"

# Добавить приватный ключ
ssh-add ~/.ssh/id_ed25519
```

> 🔑 Ключ нужно добавить вручную в GitHub:  
**Settings → SSH and GPG keys**

---

### 📂 **Комментарий (промт для оформления лекций)**
```
Заголовок ## имеет эмодзи 🔥 и жирный шрифт  
Заголовки ### имеют эмодзи 📂 и жирный шрифт  
Заголовки #### не содержат эмодзи и обычный шрифт  
Команды должны выделяться в блоках: ```bash команда ```
```
