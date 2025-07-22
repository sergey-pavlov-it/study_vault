## 🔥 **SQL Шпаргалка (Основные конструкции)**

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

### 📂 **Комментарий (промт для оформления шпаргалок)**

```
Заголовок ## имеет эмодзи 🔥 и жирный шрифт  
Заголовки ### имеют эмодзи 📂 и жирный шрифт  
Заголовки #### не содержат эмодзи и обычный шрифт  
Команды должны выделяться в блоках: ```bash команда ```
```
