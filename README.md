using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Half_Sum_Element
{
    class Program
    {
        static void Main(string[] args)
        {
            int n = int.Parse(Console.ReadLine());

            int maxValue = int.MinValue;
            int sum = 0;

            for (int i = 0; i < n; i++)
            {
                int m = int.Parse(Console.ReadLine());

                sum += m;

                if (maxValue < m)
                {
                    maxValue = m;
                }
            }

            int difference = sum - maxValue;
            int result = Math.Abs (difference - maxValue);

            Console.WriteLine(result == 0 ? $"Yes sum = {maxValue}": $"No diff = {result}");
        }
    }
}
