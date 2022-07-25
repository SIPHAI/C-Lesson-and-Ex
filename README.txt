# C-Lesson-and-Ex
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace lesson03exercise03
{
    class Account
    {
        private string strtype;
        private string strname;
        private float fltbalance;

        public string types
        {
            get { return strtype; }
        }
        public string name
        {
            get { return strname; }
        }
        public float Balance
        {
            get { return fltbalance * (float)0.018; }
        }
        public Account(float bal, string nam, string typ)
        {
            fltbalance = bal;
            strtype = nam; 
            strname = typ;
        }
        public string CalInterest()
        {
            string toreturn;
            toreturn = "The interest : $" + Balance.ToString();
            return toreturn;
        }
    }
    internal class Program
    {
        static void Main(string[] args)
        {
            Account accObj;
            

            Console.Write("Enter the type of the investment : ");
            string types = Console.ReadLine();
            Console.Write("Enter the name of invester : ");
            string name = Console.ReadLine();
            Console.Write("Enter the Balance $ : ");
            float Balance = float.Parse(Console.ReadLine());
            accObj = new Account(Balance, types, name);

            Console.WriteLine("\nBalance: ${0} ", Balance.ToString());
            Console.WriteLine(accObj.CalInterest());
            Console.ReadKey(); 

        }
    }
}
