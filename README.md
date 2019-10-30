 using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    class Program
    {
        static void Main(string args)
        {
            string n = Console.ReadLine();
            char[] c = n.ToCharArray();
            string reverse = String.Empty;
            for (int i = c.Length - 1; i > -1; i--)
            {
                reverse += c[i];
            }


            Console.Write(reverse);
            Console.WriteLine(" ");

            string sent = Console.ReadLine();
            Console.WriteLine("Тестовое предложение: " + sent);
            string[] sent_mod = sent.Split('.');
            for (byte i = 0; i < sent_mod.Length; i++)
            {
                sent_mod[i] = sent_mod[i].ToLower().Replace(sent_mod[i][sent_mod[i].Length - 1], '.') + sent_mod[i][sent_mod[i].Length - 1];
                for (byte j = 0; j < sent_mod[i].Length; j++)
                    if (sent_mod[i][j] == '*')
                        continue;
                    else
                        Console.Write(sent_mod[i][j]);
                Console.Write(" ");
                Console.WriteLine(" ");
            }
            string str = Console.ReadLine();
            str = string.Join(" ", str.Split(' ').Distinct());
            Console.Write(str);
            Console.ReadKey();
        }
    }
}---
