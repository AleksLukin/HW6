using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Diagnostics;

namespace HW6
{
    class Program
    {
        static void Main(string[] args)
        {
            Process[] process = Process.GetProcesses();
            for (int i = 0; i < process.Length; i++)
            {
                Console.WriteLine($"{process[i].ProcessName} -- {process[i].Id}");
            }
            Console.ReadLine();

            
            Console.WriteLine("Введите имя процесса");
            string nameOfProc = Console.ReadLine();
    
            for (int i = 0; i < process.Length; i++) 
                if (process[i].ProcessName == nameOfProc)
            {
                process[i].Kill();

            }

        }        
    }
}

/*Написать консольное приложение Task Manager: 
1. Которое выводит на экран запущенные процессы
2. Позволяет завершить указанный процесс. 
3. Предусмотреть возможность завершения процессов с помощью указания его ID или имени процесса. 
В качестве примера можно использовать консольные утилиты Windows ​ tasklist​ и ​ taskkill​.*/
