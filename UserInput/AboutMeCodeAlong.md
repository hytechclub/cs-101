# About Me Code-Along: Asking the User for Values

```cs
//reading user input example
Console.WriteLine("What is your name?");
String userName = Console.ReadLine();

Console.WriteLine("What is your age?");
int userAge = Convert.ToInt32(Console.ReadLine());
int userNextAge = userAge + 1;

Console.WriteLine("How many pets do you have?");
int numberOfPets = Convert.ToInt32(Console.ReadLine());

Console.WriteLine("What school do you go to?");
String strSchool = Console.ReadLine();
 
 
Console.WriteLine("Hello! My name is " + userName);
Console.WriteLine("I am " + userAge + " years old.");
Console.WriteLine("Next year I will be " + userNextAge);
Console.WriteLine("I have " + numberOfPets + " pets.");
Console.WriteLine("I attend " + strSchool);
 
Console.ReadLine();
```