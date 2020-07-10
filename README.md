# Тестовое задание

### 1. Напишите программу, которая выводит на экран числа от 1 до 100. При этом вместо чисел, кратных трем, программа должна выводить слово Fizz, а вместо чисел, кратных пяти — слово Buzz. Если число кратно пятнадцати, то программа должна выводить слово FizzBuzz. Решение должно быть записано в одну строку (без точек с запятой).


```python
', '.join([(not i % 3) * 'Fizz' + (not i % 5) * 'Buzz' or str(i) for i in range(1,101)])
```




    '1, 2, Fizz, 4, Buzz, Fizz, 7, 8, Fizz, Buzz, 11, Fizz, 13, 14, FizzBuzz, 16, 17, Fizz, 19, Buzz, Fizz, 22, 23, Fizz, Buzz, 26, Fizz, 28, 29, FizzBuzz, 31, 32, Fizz, 34, Buzz, Fizz, 37, 38, Fizz, Buzz, 41, Fizz, 43, 44, FizzBuzz, 46, 47, Fizz, 49, Buzz, Fizz, 52, 53, Fizz, Buzz, 56, Fizz, 58, 59, FizzBuzz, 61, 62, Fizz, 64, Buzz, Fizz, 67, 68, Fizz, Buzz, 71, Fizz, 73, 74, FizzBuzz, 76, 77, Fizz, 79, Buzz, Fizz, 82, 83, Fizz, Buzz, 86, Fizz, 88, 89, FizzBuzz, 91, 92, Fizz, 94, Buzz, Fizz, 97, 98, Fizz, Buzz'



### 2. Найти глобальный минимум функции $$f(x) = x^4 + 5x^3 - 10x$$ на отрезке [-5, 5]. Можно использовать библиотеку scipy.


```python
from scipy import optimize

def foo(x): return x ** 4 + 5 * x ** 3 - 10 * x
result = optimize.minimize_scalar(foo, bracket=(-5, 5))

result.x, result.fun
```




    (-3.551831156908821, -29.371443855487968)


