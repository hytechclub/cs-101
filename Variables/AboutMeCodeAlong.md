# About Me Code-Along

## Hard-coded Values
```CS
string userName = "Jordan Conrad";
int userAge = 26;
int numberOfPets = 2;
string schoolAttended = "Medina High School & Baldwin Wallace University!";


Console.WriteLine("Hello! My name is " + userName);
//Hello! My name is Jordan Conrad

Console.WriteLine("I am " + userAge + " years old and have " + numberOfPets + " pets!");
// I am 26 years old and have 2 pets!

Console.WriteLine("I went to school at " + schoolAttended + "!");
//I went to school at Medina High School & Baldwin Wallace University!
```

## Asking the User for Values
```CS
//reading user input example
Console.WriteLine("What is your name?");
String userName = Console.ReadLine();

Console.WriteLine("What is your age?");
int userAge = Convert.ToInt32(Console.ReadLine());

Console.WriteLine("How many pets do you have?");
int numberOfPets = Convert.ToInt32(Console.ReadLine());

Console.WriteLine("What school do you go to?");
String strSchool = Console.ReadLine();
 
 
Console.WriteLine("Hello! My name is " + userName);
Console.WriteLine("I am " + userAge + " years old.");
Console.WriteLine("I have " + numberOfPets + " pets.");
Console.WriteLine("I attend " + strSchool);
 
Console.ReadLine();
```