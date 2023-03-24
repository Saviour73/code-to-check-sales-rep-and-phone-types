# code to check sales rep and phone type
int totalCost = 0;

            Console.WriteLine("Welcome to Savy Communications.");

            Console.WriteLine("Please select 1 for Nokia NK900 at N9000");
            Console.WriteLine("Please select 2 for Samsung SG500 at N25000");
            Console.WriteLine("Please select 3 for Tecno Phamtom at N15000");

            string userInput = Console.ReadLine();

            bool isCoverted = int.TryParse(userInput, out int userChoice);

            switch (isCoverted)
            {
                case true:
                    switch (userChoice)
                    {
                        case 1:
                            totalCost = totalCost + 9000;
                            Console.WriteLine("You have purchased Nokia NK900 and your bill is {0}", totalCost);
                            break;

                        case 2:
                            totalCost = totalCost + 25000;
                            Console.WriteLine("You have purchased Samsung SG500 and your bill is {0}", totalCost);
                            break;

                        case 3:
                            totalCost = totalCost + 15000;
                            Console.WriteLine("You have purchased Tecno Phamtom and your bill is {0}", totalCost);
                            break;

                        default:
                            Console.WriteLine("Invalid choice. Please select between 1 and 3.");
                            break;
                    }
                    break;
                default:
                    Console.WriteLine("Invalid format entered.");
                    break;
            }
