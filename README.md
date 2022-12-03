/*Задайте значение N. Напишите программу, которая выведет все натуральные числа в промежутке от N до 1. Выполнить с помощью рекурсии.

Console.WriteLine("Введите натуральное число больше 1:");
int number = int.Parse(Console.ReadLine());

///Метод вывода натуральных чисел от N до 1:
void NumberCounter (int number)
{
    if (number < 0) Console.Write($"{number} не натуральное число");
    if (number == 0) return;
    Console.Write("{0,4}", number);
    NumberCounter (number - 1);
}

NumberCounter(number);


Задайте значения M и N. Напишите программу, которая найдёт сумму натуральных элементов в промежутке от M до N.

Console.WriteLine("Чтобы узнать сумму натуральных чисел между числами M и N, введите целое положительное число M: ");
int M = Convert.ToInt32(Console.ReadLine());
Console.WriteLine("Чтобы узнать сумму натуральных чисел между числами M и N, введите целое положительное число N: ");
int N = Convert.ToInt32(Console.ReadLine());
 
void SumNumbers(int a, int b)
{
    if (a == 0 || b == 0) return 0;
    if (a < b || a > b)
    {       
        return (a * SumNumbers(a + 1, b)); 
        Console.Write($"{a} ");
    }
    if (a==b)
    {
        Console.Write($"{a} "); return;
    }
}
SumNumbers(M, N);


Напишите программу вычисления функции Аккермана с помощью рекурсии. Даны два неотрицательных числа m и n.*/

Console.Write("Введите число M: ");
int m = Convert.ToInt32(Console.ReadLine());

Console.Write("Введите число N: ");
int n = Convert.ToInt32(Console.ReadLine());

AkkermanFunction(m,n);

void AkkermanFunction(int m, int n)
{
    Console.Write(Akkerman(m, n)); 
}

int Akkerman(int m, int n)
{
    if (m == 0)
    {
        return n + 1;
    }
    else if (n == 0 && m > 0)
    {
        return Akkerman(m - 1, 1);
    }
    else
    {
        return (Akkerman(m - 1, Akkerman(m, n - 1)));
    }
}
