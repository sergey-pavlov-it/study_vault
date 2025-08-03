## 🔥 **SQL Функции (Cheatsheet)**

---

### 📂 **Математические операторы**

#### Сложение
```bash
SELECT column1 + column2 AS result FROM table_name;
-- Пример: SELECT 10 + 5 AS result; -- Результат: 15
```

#### Вычитание
```bash
SELECT column1 - column2 AS result FROM table_name;
-- Пример: SELECT 10 - 3 AS result; -- Результат: 7
```

#### Умножение
```bash
SELECT column1 * column2 AS result FROM table_name;
-- Пример: SELECT 4 * 6 AS result; -- Результат: 24
```

#### Деление
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
-- Пример: SELECT ROUND(10.4567, 2) AS rounded_value; -- Результат: 10.46
```

#### Возведение в степень (POWER)
```bash
SELECT POWER(base_column, exponent_column) AS result FROM table_name;
-- Пример: SELECT POWER(2, 3) AS result; -- Результат: 8
```

#### Квадратный корень (SQRT)
```bash
SELECT SQRT(column) AS result FROM table_name;
-- Пример: SELECT SQRT(25) AS result; -- Результат: 5
```

#### Абсолютное значение (ABS)
```bash
SELECT ABS(column) AS result FROM table_name;
-- Пример: SELECT ABS(-42) AS result; -- Результат: 42
```

#### Наименьшее и наибольшее значение (LEAST, GREATEST)
```bash
SELECT LEAST(column1, column2) AS min_value, GREATEST(column1, column2) AS max_value FROM table_name;
-- Пример: SELECT LEAST(5, 10), GREATEST(5, 10); -- Результат: 5, 10
```

#### Округление в меньшую сторону (FLOOR)
```bash
SELECT FLOOR(column) AS floored_value FROM table_name;
-- Пример: SELECT FLOOR(5.9) AS floored_value; -- Результат: 5
```

#### Округление в большую сторону (CEIL / CEILING)
```bash
SELECT CEIL(column) AS ceiled_value FROM table_name;
-- Пример: SELECT CEIL(4.1) AS ceiled_value; -- Результат: 5
```

---

### 📂 **Строковые функции**

#### Конкатенация строк (CONCAT)
```bash
SELECT CONCAT(column1, column2) AS result FROM table_name;
-- Пример: SELECT CONCAT('Hello', 'World') AS result; -- Результат: HelloWorld
```

#### Конкатенация строк с разделителем (CONCAT_WS)
```bash
SELECT CONCAT_WS(separator, column1, column2, ...) AS result FROM table_name;
-- Пример: SELECT CONCAT_WS('-', '2023', '08', '01') AS result; -- Результат: 2023-08-01
```

#### Длина строки (LENGTH)
```bash
SELECT LENGTH(column) AS result FROM table_name;
-- Пример: SELECT LENGTH('SQL') AS result; -- Результат: 3
```

#### Приведение к верхнему регистру (UPPER)
```bash
SELECT UPPER(column) AS result FROM table_name;
-- Пример: SELECT UPPER('hello') AS result; -- Результат: HELLO
```

#### Приведение к нижнему регистру (LOWER)
```bash
SELECT LOWER(column) AS result FROM table_name;
-- Пример: SELECT LOWER('SQL') AS result; -- Результат: sql
```

#### Извлечение подстроки (SUBSTRING / SUBSTR)
```bash
SELECT SUBSTRING(column FROM start FOR length) AS result FROM table_name;
-- Пример: SELECT SUBSTRING('database' FROM 1 FOR 4) AS result; -- Результат: data
```

#### Удаление пробелов (TRIM)
```bash
SELECT TRIM(column) AS result FROM table_name;
-- Пример: SELECT TRIM('  sql  ') AS result; -- Результат: sql
```

#### Замена символов (REPLACE)
```bash
SELECT REPLACE(column, 'old', 'new') AS result FROM table_name;
-- Пример: SELECT REPLACE('2023-08-01', '-', '.') AS result; -- Результат: 2023.08.01
```

---

### 📂 **Комментарий (промт для оформления шпаргалок)**

```
Заголовок ## имеет эмодзи 🔥 и жирный шрифт  
Заголовки ### имеют эмодзи 📂 и жирный шрифт  
Заголовки #### не содержат эмодзи и обычный шрифт  
Команды должны выделяться в блоках: ```bash команда ```
```
