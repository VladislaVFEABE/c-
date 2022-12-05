# c-using System;
using System.Collections.Generic;
using System.Collections;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using static System.Console;
using static System.String;

namespace Kybersport
{
    class Program
    {
        static void Main()
        {
            ForegroundColor = ConsoleColor.Blue;
            BackgroundColor = ConsoleColor.Yellow;
            Write("Я 18 вариант\n");
            WriteLine("Введите номер задачи от 1 до 7");
            int wibor = Convert.ToInt32(Console.ReadLine());
            switch (wibor)
            {
                case 1:
                   Funkciya();
                    break;
                case 2:
                    Treugolbnik();
                    break;
                case 3:
                    GrafikFunc();
                    break;
                case 4:
                    PriznakiTransporta();
                    break;
                case 5:
                  Vklad();
                    break;
                case 6:
                    Chess();
                    break;
                case 7:
                    Chislo();
                    break;
            }
         
            
        }
        static void Funkciya()
        {
            Console.Write("Введите x: \n");
            double x = Convert.ToInt32(Console.ReadLine());
            Console.Write("Введите e: \n");
            double e = Convert.ToInt32(Console.ReadLine());
            double y = 0;
            if (x > Math.PI) y = Math.Sqrt(e + Math.Sqrt(x)) -Math.Cos(x);
            if (1 <= x && x <= 2) y = Math.Pow(x,2) + Math.Log(x);
            Console.WriteLine($"y = {Math.Round(y, 4)}");
        }
        static void Treugolbnik()
        {
            Write("Определить является ли треугольник со сторонами a,b,c прямоугольным\n");
            WriteLine("Введите сторону а:\n");
            int a = Convert.ToInt32(Console.ReadLine());
            WriteLine("Введите сторону b:\n");
            int b = Convert.ToInt32(Console.ReadLine());
            WriteLine("Введите сторону c:\n");
            int c = Convert.ToInt32(Console.ReadLine());
            if ((c * c == a * a + b * b))
            {
                Console.WriteLine("Треугольник существует. Он прямоугольный.");
            }
            else
            {
                Console.WriteLine("Треугольник существует. Он непрямоугольный.");
            }
        }
        static void GrafikFunc()
        {
          
        }
        static void PriznakiTransporta()
        {
            Write("Дан признак т/с автомобиль(а), велосипед(в), мотоцикл(м), самолет(с), поезд(п) \n");
            Write("Вывести на экран максимальную скорость т/с в зависиммости от введнего признака\n");
            WriteLine("Введите скорость автомобиля\n");
            int speedauto = Convert.ToInt32(Console.ReadLine());
            Write($"Скорость автомобиля = {speedauto} км/ч \n");
            WriteLine("Введите скорость велосипеда \n");
            int speedvel = Convert.ToInt32(Console.ReadLine());
            Write($"Скорость  велосипеда = {speedvel} км/ч \n");
            WriteLine("Введите скорость мотоцикла \n");
            int speedmoto = Convert.ToInt32(Console.ReadLine());
            Write($"Скорость мотоцикла = {speedmoto} км/ч \n");
            WriteLine("Введите скорость самолета \n");
            int speedfly = Convert.ToInt32(Console.ReadLine());
            Write($"Скорость  самолета = {speedfly} км/ч \n");
            WriteLine("Введите скорость поезда \n");
            int speedtrain = Convert.ToInt32(Console.ReadLine());
            Write($"Скорость  поезда = {speedtrain} км/ч \n");
            if(speedauto > speedvel)
            {
                Write("Автомобиль быстрее велосипеда\n");
            }
            else
            {
                Write("Автомобиль медленее велосипеда\n");
            }
            if (speedvel > speedmoto)
            {
                Write("Велосипед быстрее мотоцикла что странно кстати\n");
            }
            else
            {
                Write("Велосипед медленее мотоцикла\n");
            }
            if(speedmoto > speedfly)
            {
                Write("Мотоцикл быстрее самолета\n");
            }
            else
            {
                Write("Мотоцикл медленее самолета\n");
            }
            if (speedfly > speedtrain)
            {
                Write("Самолет быстрее поезда\n");
            }
            else
            {
                Write("Самолет медленее поезда\n");
            }
            Write($"Введенные скорости {speedauto}, {speedvel}, {speedmoto}, {speedfly}, {speedtrain} км/ч"); 
        }
        static void Vklad()
        {
            Write("известен начальный вклад клиента в банк и процент годового дохода\n");
            Write("определить через сколько лет вклад превысит заданный размер и каков при этом будет размер вклада\n");
            WriteLine("Введите сумму вклада ");
            int vkladik = Convert.ToInt32(Console.ReadLine());
            WriteLine("Введите процент годового дохода");
            int procentik = Convert.ToInt32(Console.ReadLine());
            WriteLine("Введите на сколько дней хотите сделать вклад ");
            int day = Convert.ToInt32(Console.ReadLine());
            int result = (vkladik * procentik * day /365)/ 100;
            Write($"Размер вклада будет {result}р. 00коп");
        }
        static void Chess()
        {
            int[,] chess = new int[8, 8];
            chess[0, 0] = 1;
            chess[0, 2] = 1;
            chess[0, 4] = 1;
            chess[0, 6] = 1;
            chess[1, 1] = 1;
            chess[1, 3] = 1;
            chess[1, 5] = 1;
            chess[1, 7] = 1;
            chess[2, 0] = 1;
            chess[2, 2] = 1;
            chess[2, 4] = 1;
            chess[2, 6] = 1;
            chess[3, 1] = 1;
            chess[3, 3] = 1;
            chess[3, 5] = 1;
            chess[3, 7] = 1;
            chess[4, 0] = 1;
            chess[4, 2] = 1;
            chess[4, 4] = 1;
            chess[4, 6] = 1;
            chess[5, 1] = 1;
            chess[5, 3] = 1;
            chess[5, 5] = 1;
            chess[5, 7] = 1;
            chess[6, 0] = 1;
            chess[6, 2] = 1;
            chess[6, 4] = 1;
            chess[6, 6] = 1;
            chess[7, 1] = 1;
            chess[7, 3] = 1;
            chess[7, 5] = 1;
            chess[7, 7] = 1;



            for (int i = 0; i < 8; i++)
            {
                for (int j = 0; j < 8; j++)
                {
                    Console.Write("{0}\t", chess[i, j]);
                }
                Console.WriteLine();
            }
            Console.ReadKey();
        }
        static void Chislo()
        {
            Console.Write("Введите цифру из диапазона K[1-150]:=\n");
            int k = Convert.ToInt32(Console.ReadLine());
            for(int i =1; i<=k; i++)
            {
                if(i % 3 == 0)
                {
                    Write($"{i}\n");
                }
                else if(i == 0)
                {
                    Write("Err");
                }
            }
        }
    }
  
}
