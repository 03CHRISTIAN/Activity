using System;

namespace Problem3_LIM
{
    class EmployeeTimeKeepingSystem 
    {
        static void Main(string[] args)
        {
            Console.WriteLine("                        ____________________");
            Console.WriteLine($"Current Time and Date:  {DateTime.Now}");
            Console.WriteLine("                        ____________________");
            Console.WriteLine();
            Console.WriteLine("____________________________________________");
            Console.WriteLine("                 welcome                    ");
            Console.WriteLine("        Employee Time Keeping System        ");
            Console.WriteLine("____________________________________________");
            Console.WriteLine();

            //time-in

            Console.WriteLine("Time-In");
            Console.WriteLine();
            Console.Write("Employee ID:");
            string employeeId = Console.ReadLine();
            Console.WriteLine();

            TimeSpan timeIn = new TimeSpan(8, 0, 0);
            Console.WriteLine($"Recorded   : {timeIn}");
            Console.WriteLine();

            //time-out

            Console.WriteLine("____________________________________________");
            Console.WriteLine();

            Console.WriteLine("Time-Out");
            Console.WriteLine();
            Console.Write("Employee ID:");
            employeeId = Console.ReadLine();
            Console.WriteLine();


            TimeSpan timeOut = new TimeSpan(15, 0, 0);
            Console.WriteLine($"Recorded   : {timeOut}");
            Console.WriteLine();
            
            Console.WriteLine("____________________________________________");
            Console.WriteLine();

            //lunch break duration

            TimeSpan lunchBreakDuration = new TimeSpan(1, 0, 0);

            //total number of hours employee worked

            TimeSpan totalHours = (timeOut - timeIn) - lunchBreakDuration;
            Console.WriteLine($"Hours Worked        : {totalHours}");

            //total office working hours

            TimeSpan regularHoursStart = new TimeSpan(8, 0, 0);
            TimeSpan regularHoursEnd = new TimeSpan(17, 0, 0);

            //late time-in computation

            TimeSpan lateIn = new TimeSpan(0, 0, 0);

            if (timeIn > regularHoursStart)
            {
                lateIn = timeIn - regularHoursStart;
            }

            //undertime time-out computation

            TimeSpan underTime = new TimeSpan(0, 0, 0);
            TimeSpan totalUndertime = new TimeSpan(0, 0, 0);

            if (timeOut < regularHoursEnd)
            {
                underTime = timeOut - regularHoursEnd;

                totalUndertime = regularHoursEnd - timeOut; 
            }

           
            //total of regular hours an employee has fulfilled

            TimeSpan totalRegularHours = totalHours - (lateIn - underTime);

            Console.WriteLine($"Regular Hours Worked: {totalRegularHours}");

            Console.WriteLine($"Under Time          : {totalUndertime}");

        }
    }
}
