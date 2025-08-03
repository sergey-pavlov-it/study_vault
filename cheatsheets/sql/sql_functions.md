## 🔥 **SQL Функции (Cheatsheet)**

---

### 📂 **Математические операторы**

#### Сложение (+)
```bash
SELECT column1 + column2 AS result FROM table_name;
-- Пример: SELECT 10 + 5 AS result; -- Результат: 15
```

#### Вычитание (-)
```bash
SELECT column1 - column2 AS result FROM table_name;
-- Пример: SELECT 10 - 3 AS result; -- Результат: 7
```

#### Умножение (*)
```bash
SELECT column1 * column2 AS result FROM table_name;
-- Пример: SELECT 4 * 6 AS result; -- Результат: 24
```

#### Деление (/)
```bash
SELECT column1 / column2 AS result FROM table_name;
-- Пример: SELECT 10 / 4 AS result; -- Результат: 2.5
```

#### Остаток от деления (MOD)
```bash
SELECT MOD(column1, column2) AS result FROM table_name;
-- Пример: SELECT MOD(10, 3) AS result; -- Результат: 1
```

#### Целочисленное деление (DIV в MySQL)
```bash
SELECT column1 DIV column2 AS result FROM table_name;
-- Пример: SELECT 10 DIV 3 AS result; -- Результат: 3
```

---

### 📂 **Математические функции**

#### Округление (ROUND)
```bash
SELECT ROUND(column, 2) AS rounded_value FROM table_name;
```

#### Возведение в степень (POWER)
```bash
SELECT POWER(base_column, exponent_column) AS result FROM table_name;
```

#### Квадратный корень (SQRT)
```bash
SELECT SQRT(column) AS result FROM table_name;
```

#### Абсолютное значение (ABS)
```bash
SELECT ABS(column) AS result FROM table_name;
```

#### Наименьшее и наибольшее значение (LEAST, GREATEST)
```bash
SELECT LEAST(column1, column2), GREATEST(column1, column2);
```

#### Округление в меньшую сторону (FLOOR)
```bash
SELECT FLOOR(column) AS floored_value FROM table_name;
```

#### Округление в большую сторону (CEIL / CEILING)
```bash
SELECT CEIL(column) AS ceiled_value FROM table_name;
```

#### Генерация числовой последовательности (GENERATE_SERIES)
```bash
SELECT * FROM generate_series(1, 5);
-- Результат: 1, 2, 3, 4, 5

SELECT generate_series('2024-01-01'::date, '2024-01-10'::date, '1 day'::interval);
-- Даты от 1 до 10 января 2024 с шагом 1 день
```

---

### 📂 **Утилитарные функции**

#### Замена NULL значением (COALESCE)
```bash
SELECT COALESCE(NULL, 'default');  -- default
SELECT COALESCE(NULL, NULL, 'backup');  -- backup
```

#### Возврат NULL, если значения равны (NULLIF)
```bash
SELECT NULLIF(10, 10);  -- NULL
SELECT NULLIF(10, 5);   -- 10
```

#### Работа с массивами (PostgreSQL)
```bash
SELECT UNNEST(ARRAY[1,2,3]);
SELECT ARRAY[1,2,3] || ARRAY[4,5];  -- [1,2,3,4,5]
```

---

### 📂 **Строковые функции**

#### Конкатенация строк (CONCAT)
```bash
SELECT CONCAT('Hello', 'World');  -- HelloWorld
```

#### Конкатенация с разделителем (CONCAT_WS)
```bash
SELECT CONCAT_WS('-', '2023', '08', '01');  -- 2023-08-01
```

#### Длина строки (LENGTH)
```bash
SELECT LENGTH('SQL');  -- 3
```

#### Приведение к верхнему и нижнему регистру
```bash
SELECT UPPER('text');  -- TEXT
SELECT LOWER('SQL');   -- sql
```

#### Извлечение подстроки
```bash
SELECT SUBSTRING('database' FROM 1 FOR 4);  -- data
```

#### Удаление пробелов
```bash
SELECT TRIM('  sql  ');  -- sql
```

#### Замена символов
```bash
SELECT REPLACE('2023-08-01', '-', '.');  -- 2023.08.01
```

---

### 📂 **Функции даты и времени**

#### Текущая дата и время
```bash
SELECT NOW();               -- Дата и время
SELECT CURRENT_DATE;        -- Только дата
SELECT CURRENT_TIME;        -- Только время
SELECT CURRENT_TIMESTAMP;   -- Дата и время
```

#### Извлечение частей даты
```bash
SELECT EXTRACT(YEAR FROM CURRENT_DATE);         -- Год
SELECT EXTRACT(MONTH FROM CURRENT_DATE);        -- Месяц
SELECT EXTRACT(DAY FROM CURRENT_DATE);          -- День
SELECT EXTRACT(HOUR FROM CURRENT_TIMESTAMP);    -- Часы
SELECT EXTRACT(MINUTE FROM CURRENT_TIMESTAMP);  -- Минуты
SELECT EXTRACT(SECOND FROM CURRENT_TIMESTAMP);  -- Секунды
```

#### Разность между датами
```bash
SELECT DATE '2023-01-01' - DATE '2022-12-01';  -- 31
```

#### Разница в возрасте (AGE)
```bash
SELECT AGE(DATE '2020-01-01');  -- между сегодня и 2020
SELECT AGE(TIMESTAMP '2023-01-01', TIMESTAMP '2020-01-01');
```

#### Добавление / вычитание интервала
```bash
SELECT INTERVAL '1 day';  -- создать интервал
SELECT CURRENT_DATE + INTERVAL '7 days';
SELECT CURRENT_DATE - INTERVAL '1 month';
```

#### Преобразование типов и форматирование (CAST, ::, TO_CHAR, TO_DATE)
```bash
SELECT '2024-01-01'::DATE;
SELECT CAST('123' AS INTEGER);

SELECT TO_CHAR(CURRENT_DATE, 'YYYY-MM-DD');
SELECT TO_CHAR(NOW(), 'HH24:MI:SS');  -- часы:минуты:секунды (24-часовой формат)
SELECT TO_DATE('01.01.2024', 'DD.MM.YYYY');
```

#### Округление даты (DATE_TRUNC)
```bash
SELECT DATE_TRUNC('month', NOW());  -- начало месяца
SELECT DATE_TRUNC('day', NOW());    -- начало дня
```

---

### 📂 **Регулярные выражения**

#### Специальные символы

- `.` — любой символ  
- `^` — начало строки  
- `$` — конец строки  
- `*` — 0 или больше  
- `+` — 1 или больше  
- `?` — 0 или 1  
- `{}` — количество повторений  
- `[]` — множество символов  
- `()` — группировка  
- `|` — логическое ИЛИ  
- `\\` — экранирование  
- `\\d` — цифра  
- `\\s` — пробел/табуляция  

---

### 📂 **Комментарий (промт для оформления шпаргалок)**

```
Заголовок ## имеет эмодзи 🔥 и жирный шрифт  
Заголовки ### имеют эмодзи 📂 и жирный шрифт  
Заголовки #### не содержат эмодзи и обычный шрифт  
Команды должны выделяться в блоках: ```bash команда ```
```
