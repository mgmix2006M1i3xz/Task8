<img width="620" height="670" alt="image" src="https://github.com/user-attachments/assets/0e19d61c-7144-4929-afb9-3763acdc120d" />Домашнее задание к работе номер 8

Условие задачи: 

<img width="777" height="157" alt="image" src="https://github.com/user-attachments/assets/b16e7755-49b1-43ba-8264-cebe0a19de01" />


1. Алгоритм и блок-схема.

Алгоритм:

Начало.
Объявить n, sum = 0.0.
Считать значение n.
Запустить цикл for от i = 0 до n.
На каждой итерации: если i четное — прибавить 1/2^i, если нечетное — вычесть.
Вывести sum.
Конец.

Блок-схема:

<img width="620" height="670" alt="Снимок экрана 2026-10-23 184533" src="https://github.com/user-attachments/assets/b2938c7d-0572-4276-9dbb-8fca94e3478f" />


2. Реализация программы

#include <stdio.h>
#include <math.h> // Для pow()
#include <locale.h>

int main() {
    setlocale(LC_ALL, "RUS");
    int n;
    double sum = 0.0;

    printf("Введите значение n: ");
    scanf("%d", &n);

    // Цикл от 0 до n, так как первый член соответствует n=0
    for (int i = 0; i <= n; i++) {
        // Используем pow для возведения в степень
        double term = 1.0 / pow(2, i);
        
        // Определяем знак: если i четное, то плюс, иначе минус
        if (i % 2 == 0) {
            sum += term;
        } else {
            sum -= term;
        }
    }

    printf("Сумма ряда при n = %d равна: %lf\n", n, sum);

    return 0;
}

3. Результаты работы программы

Случай 1:
Введите значение n: 2
Сумма ряда при n = 2 равна: 0.750000 (1 - 0.5 + 0.25)

Случай 2:
Введите значение n: 4
Сумма ряда при n = 4 равна: 0.687500 (1 - 0.5 + 0.25 - 0.125 + 0.0625)

4. Информация о разработчике
Митин Михаил Александрович, бТИИ-261
