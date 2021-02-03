# HW6 
using System.Diagnostics;

namespace HW6
{
    class Program
    {
        static void Main(string[] args)
        {
            Tasklist();
            Taskkill();
        }
        static void Tasklist()
        {
            Process[] processes = Process.GetProcesses();
            for (int i = 0; i<processes.Length; i++)
            {
                Console.WriteLine(processes[i]);
            }
            Console.ReadLine();
            return;
        }
        static void Taskkill()
        {
            Console.WriteLine("Введите имя процесса");
            Process nameOfProc = Process.Start(Console.ReadLine());
            Console.WriteLine("Нажмите любую клавишу для завершения процесса...");
            Console.ReadKey();
            nameOfProc.Kill();
            return;
        }        
    }
}
