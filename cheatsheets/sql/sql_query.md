## 🔥 **SQL Шпаргалка (Основные конструкции)**

---

### 📂 **SELECT**

#### Выбрать все столбцы из таблицы
```bash
SELECT * FROM table_name;
```

#### Выбрать определённые столбцы
```bash
SELECT column1, column2 FROM table_name;
```

#### Подсчитать количество строк в таблице
```bash
SELECT COUNT(*) FROM table_name;
```

#### Выбрать уникальные значения (DISTINCT)
```bash
SELECT DISTINCT column1, column2 FROM table_name;
```

#### Создать новую таблицу на основе выборки
```bash
CREATE TABLE new_table AS
(SELECT DISTINCT column1, column2 FROM old_table);
```

#### Преобразование типов (CAST)
```bash
SELECT CAST(1.23 AS int);        -- вернёт 1
SELECT CAST('1.23' AS float) + 2; -- преобразует текст в число и выполнит сложение
SELECT CAST('2023-10-01' AS DATE);
SELECT to_date('05 Dec 2000', 'DD Mon YYYY');
```

#### Использование арифметических операций и переименование столбца (AS)
```bash
SELECT (column1 + column2) AS new_column FROM table_name;
SELECT (column * 1.07) AS new_column FROM table_name;
```

#### Использование CASE в SELECT (условные вычисления)
```bash
SELECT column1, column2,
CASE
    WHEN column1 >= column2 THEN column1 - column2
    ELSE column2 - column1
END AS new_column
FROM table_name;
```

---

### 📂 **CREATE TABLE**

#### Создание новой таблицы
```bash
CREATE TABLE table_name (
    column1 data_type [constraints],
    column2 data_type [constraints],
    column3 data_type [constraints]
);
```
Пример:
```bash
CREATE TABLE employees (
    id INT PRIMARY KEY,
    name VARCHAR(50) NOT NULL,
    salary DECIMAL(10,2),
    hire_date DATE
);
```

---

### 📂 **INSERT**

#### Добавление одной строки
```bash
INSERT INTO table_name (column1, column2, column3)
VALUES (value1, value2, value3);
```

#### Добавление нескольких строк
```bash
INSERT INTO table_name (column1, column2, column3)
VALUES (value1, value2, value3),
       (value4, value5, value6);
```

---

### 📂 **UPDATE**

#### Обновление значений в таблице (простое)
```bash
UPDATE table_name
SET column1 = new_value1,
    column2 = new_value2
WHERE condition;
```

#### Обновление с использованием CASE (одно поле)
```bash
UPDATE table_name
SET column1 = CASE
    WHEN condition1 THEN new_value1
    WHEN condition2 THEN new_value2
    ELSE column1
END
WHERE condition_for_update;
```

#### Обновление с использованием CASE (несколько полей)
```bash
UPDATE table_name
SET column1 = CASE
    WHEN condition1 THEN new_value1
    WHEN condition2 THEN new_value2
    ELSE column1
END,
    column2 = CASE
    WHEN condition1 THEN new_value3
    WHEN condition3 THEN new_value4
    ELSE column2
END
WHERE condition_for_update;
```

---

### 📂 **DELETE**

#### Удаление одной строки
```bash
DELETE FROM table_name
WHERE id = value;
```

#### Удаление нескольких строк по условию
```bash
DELETE FROM table_name
WHERE condition;
```

---

### 📂 **Навигация по БД (MySQL)**

#### Показать список таблиц в базе
```bash
SHOW TABLES;
```

#### Показать структуру таблицы
```bash
DESCRIBE table_name;
```

---

### 📂 **Комментарий (промт для оформления шпаргалок)**

```
Заголовок ## имеет эмодзи 🔥 и жирный шрифт  
Заголовки ### имеют эмодзи 📂 и жирный шрифт  
Заголовки #### не содержат эмодзи и обычный шрифт  
Команды должны выделяться в блоках: ```bash команда ```
```