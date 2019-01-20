# Обзор основных функций высшего порядка

## Map
Функция `map` принимает функцию и какую либо последовательность (список, вектор, хеш и т.д). И применяет полученную функцию к полученной последовательности, и возвращает результат.

### Функция map в языке Python
```python
# Возведение каждого элемента списка в квадрат:
>>> list(map(lambda x: x**2, [1, 2, 3, 4]))
[1, 4, 9, 16]

# Перемножение чисел из двух списков:
>>> list(map(lambda x, y: x*y, [1, 2, 3, 4], [5, 6, 7, 8]))
[5, 12, 21, 32]

# Подсчет кол-ва букв в словах находящихся в списке:
>>> list(map(lambda x: len(x), ["Hello", "World", "Python"]))
[5, 5, 6]

# Использование словаря в функции Map:
>>> chars = {'a': 1, 'b': 2, 'c': 3}
>>> list(map(lambda x: x*chars[x], chars))
['a', 'bb', 'ccc']
```

### Функция map в языке Scheme (GNU Guile)
```scheme
scheme@(guile-user)> (map (lambda (x) (+ x 999)) '(1000 999 998 997 996))
$1 = (1999 1998 1997 1996 1995)

```