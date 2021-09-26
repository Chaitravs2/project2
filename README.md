# project2
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Project1
{
    class banking_Implement : Banking
    {
        static void Main(string[] args)
        {
            int ch;
            int exp_pin = 1234;
            int act_pin = 1234;
            Banking ob = new Banking();
            ob.getdetails();
            ob.display();

            Console.WriteLine("Enter the Pin");
            exp_pin = int.Parse(Console.ReadLine());
            if (exp_pin == act_pin)
            {
                Console.WriteLine("VALID PIN");
                do
                {
                    Console.WriteLine("Enter choice\n1 Deposit\n2 Withdraw\n3 Checkbal\n4 Exit");
                    ch = int.Parse(Console.ReadLine());


                    switch (ch)
                    {
                        case 1:
                                Console.WriteLine("Enter the amount to be deposited");
                                double amount =double.Parse(Console.ReadLine());
                                ob.deposit(amount);
                                break;
                        case 2:
                                 Console.WriteLine("Enter the amount to be withdrawn");
                                 amount = double.Parse(Console.ReadLine());
                                 ob.withdraw(amount);
                                 break;
                        case 3:
                                 ob.checkbal();
                                 break;
                        case 4: break;
                    }
                }
                while (ch != 4);
            }
            else
                Console.WriteLine("INVALID PIN");
                Console.WriteLine("Try Later....:)");
            }
        }
    }
