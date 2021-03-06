# CodeJam-1 

- **Deadline:** 09-04-2018 23:59 
- **Куда сдавать**: Приватный репозиторий, бранч "code-jam1", папка "code-jam1", **минимум 2 коммита**, далее Pull Request вешать на своего ментора.
- **Что сдавать**: Вы должны реализовать 2 функции. Каждый функцию необходимо сохранить в отдельном файле с именем задания (Например make.js). Как только вы реализовали одну из функций, вы коммитает файл. Далее решаете и коммитаете второй. Можно рефакторить и коммитать исправления до дедлайна.

**Задание #1. Функция "sumOfOther"**.

```
Реализуйте функцию sumOfOther, которая получает на вход массив, например, [2, 3, 4, 1], а возращает, [8, 7, 6, 9]. Входной массив - одномерный, целочисленный, произвольной длины. 
В результирующем массиве каждый элемент по индексу i - это сумма остальных элементов оригинального массива. 
```

**Задание #2. Функция "make"**.

Реализовать функцию make, которую можно вызвать следующим образом:

```javascript
make(15)(34, 21, 666)(41)(sum); // return 777

function sum(a, b) {
    return a + b;
}

```
Пока переданный аргумент не функция, запоминаем значения аргументов (способы перечислены ниже), затем применяем функцию к аргументам по принципу `Array.prototype.reduce`, возвращаем полученное значение

Step | a    | b    | result
---- | ---- | ---- | ----
  0  |  15  |  34  |  49
  1  |  49  |  21  |  70
  2  |  70  |  666 |  736
  3  |  736 |  41  |  777

нельзя использовать глобальные переменные, сохранять промежуточные значения в `make.smth` или в `make.prototype`

Cпособы:
* через замыкание
* частичное применение (google: "partial application javascript")
* рекурсия (для гиков :smirk_cat:)

**Бонусное задание. Покрыть функции тестами**.
