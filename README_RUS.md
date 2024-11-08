# Math

Проект **Math** представляет собой реализацию собственной версии математической библиотеки `math.h` на языке программирования C. Основные математические функции, реализованные в проекте, охватывают базовые операции, используемые в различных алгоритмах. 

Проект нацелен на закрепление знаний по вычислительным методам и структурному программированию. Выполнен в команде.

## Оглавление

1. [Описание функциональности](#описание-функциональности)
    - [Функции](#функции)
2. [Требования](#требования)
3. [Сборка](#сборка)
4. [Использование](#использование) 
5. [Тестирование](#тестирование)

## Описание функциональности

### Функции

Проект реализует следующие функции из библиотеки `math.h`:

| №  | Функция                      | Описание                                                          |
| --- | ----------------------------- | ----------------------------------------------------------------- |
| 1   | `int s21_abs(int x)`          | Вычисляет абсолютное значение целого числа                        |
| 2   | `long double s21_acos(double x)` | Вычисляет арккосинус                                           |
| 3   | `long double s21_asin(double x)` | Вычисляет арксинус                                             |
| 4   | `long double s21_atan(double x)` | Вычисляет арктангенс                                           |
| 5   | `long double s21_ceil(double x)` | Возвращает ближайшее целое число, не меньшее заданного значения |
| 6   | `long double s21_cos(double x)`  | Вычисляет косинус                                               |
| 7   | `long double s21_exp(double x)`  | Возвращает значение e, возведенное в заданную степень           |
| 8   | `long double s21_fabs(double x)` | Вычисляет абсолютное значение числа с плавающей точкой          |
| 9   | `long double s21_floor(double x)`| Возвращает ближайшее целое число, не превышающее заданное значение |
| 10  | `long double s21_fmod(double x, double y)` | Остаток от деления с плавающей точкой                 |
| 11  | `long double s21_log(double x)`  | Вычисляет натуральный логарифм                                   |
| 12  | `long double s21_pow(double base, double exp)` | Возводит число в заданную степень                     |
| 13  | `long double s21_sin(double x)`  | Вычисляет синус                                                 |
| 14  | `long double s21_sqrt(double x)` | Вычисляет квадратный корень                                      |
| 15  | `long double s21_tan(double x)`  | Вычисляет тангенс                                               |

## Требования

- Язык программирования: C (стандарт C11)
- Компилятор: GCC (GNU Compiler Collection)
- Система сборки: Makefile
- Стандарт: POSIX.1-2017
- Код соответствует Google Style Guide

## Сборка

Для сборки библиотеки и выполнения тестов предусмотрен `Makefile` с целями:
- `all` — компиляция библиотеки и тестов
- `clean` — очистка скомпилированных файлов
- `test` — запуск модульных тестов
- `s21_math.a` — сборка статической библиотеки
- `gcov_report` — генерация отчёта покрытия кода в формате HTML

### Шаги для сборки

1. Клонирование репозитория:
    ```
    git clone https://github.com/llllenivka/Math.git
    cd Math
    ```

2. Сборка библиотеки и тестов:
    ```
    make all
    ```

3. Очистка скомпилированных файлов:
    ```
    make clean
    ```

4. Генерация отчета покрытия кода:
    ```
    make gcov_report
    ```

## Использование

После сборки можно использовать скомпилированную библиотеку `s21_math.a` в своих проектах. Все функции имеют префикс `s21_`, чтобы избежать конфликтов с оригинальной библиотекой `math.h`.

Пример кода для использования `s21_math`:
```c
#include "s21_math.h"

int main() {
    double result = s21_sqrt(25.0);
    printf("Square root of 25 is %Lf\n", result);
    return 0;
}
```

## Тестирование

Тестирование функций осуществляется с помощью библиотеки `Check`. Тесты проверяют корректность работы каждой функции, сравнивая результаты с соответствующими функциями из стандартной библиотеки math.h. Минимальное покрытие тестами — 80% для каждой функции.

Запуск всех тестов осуществляется командой:

```
make test
```
## Отчёт покрытия кода
Для анализа покрытия тестами используется gcov. Для генерации HTML-отчёта покрытия кода выполните:

```
make gcov_report
```