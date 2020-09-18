# About Me Code-Along: Asking the User for Values
Create a program that asks the user for information, and then prints it out in a sentence format. Start by creating a new C# Repl, and then follow the steps below.

## Asking for a Name
First, ask the user for their name.

1. Remove any existing code within the `Main` block
1. Add a `Console.WriteLine` statement to print a message: "What is your name?"
1. Under the `Console.WriteLine`, add a `Console.ReadLine()` statement
1. Store the answer in a new `string` variable named `userName`

Run the program and make sure there are no errors.

```cs
Console.WriteLine("What is your name?");
string userName = Console.ReadLine();
```

## Asking for an Age
Next, ask the user how old they are. This will be used to calculate their upcoming birthday age.

1. Make a new line under the previous statement
1. Add a `Console.WriteLine` statement to print a message: "How old are you?"
1. Under the `Console.WriteLine`, add a `Console.ReadLine()` statement
1. Wrap the `Console.ReadLine()` in a `Convert.ToInt32()` so the result becomes a number
1. Store the answer in a new `int` variable named `userAge`
1. Under that, set another variable named `userNextAge` to the user's current age plus one

Run the program and make sure there are no errors.

```cs
Console.WriteLine("How old are you?");
int userAge = Convert.ToInt32(Console.ReadLine());
int userNextAge = userAge + 1;
```

## Asking for Pets
Next, ask the user how many pets they have.

1. Make a new line under the previous statement
1. Add a `Console.WriteLine` statement to print a message: "How many pets do you have?"
1. Under the `Console.WriteLine`, add a `Console.ReadLine()` statement
1. Wrap the `Console.ReadLine()` in a `Convert.ToInt32()` so the result becomes a number
1. Store the answer in a new `int` variable named `numberOfPets`

Run the program and make sure there are no errors.

```cs
Console.WriteLine("How many pets do you have?");
int numberOfPets = Convert.ToInt32(Console.ReadLine());
```

## Asking for School
Next, ask the user which school they attend.

1. Make a new line under the previous statement
1. Add a `Console.WriteLine` statement to print a message: "How many pets do you have?"
1. Under the `Console.WriteLine`, add a `Console.ReadLine()` statement
1. Store the answer in a new `string` variable named `school`

Run the program and make sure there are no errors.

```cs
Console.WriteLine("What school do you go to?");
string school = Console.ReadLine();
```

## Printing the Results
Finally, it's time to print out all of the information!

1. Make a new line under the previous statement
1. Create a `Console.WriteLine` statement
1. Set the message to say "Hello! My name is "
1. Add the `userName` variable to the end of the message string using `+`
1. Create another `Console.WriteLine` statement
1. Set the message to say "I am "
1. Add the `userAge` variable to the end of the message string using `+`
1. Add " years old" to the end of the message string using `+`
1. Create another `Console.WriteLine` statement
1. Set the message to say "Next year I will be "
1. Add the `userNextAge` variable to the end of the message string using `+`
1. Create another `Console.WriteLine` statement
1. Set the message to say "I have "
1. Add the `numberOfPets` variable to the end of the message string using `+`
1. Add " pets" to the end of the message string using `+`
1. Create another `Console.WriteLine` statement
1. Set the message to say "I attend "
1. Add the `school` variable to the end of the message string using `+`

Run the program and make sure that all the proper information is displayed!

```cs
Console.WriteLine("Hello! My name is " + userName);
Console.WriteLine("I am " + userAge + " years old");
Console.WriteLine("Next year I will be " + userNextAge);
Console.WriteLine("I have " + numberOfPets + " pets");
Console.WriteLine("I attend " + school);
```

## Final Code
```cs
Console.WriteLine("What is your name?");
string userName = Console.ReadLine();

Console.WriteLine("How old are you?");
int userAge = Convert.ToInt32(Console.ReadLine());
int userNextAge = userAge + 1;

Console.WriteLine("How many pets do you have?");
int numberOfPets = Convert.ToInt32(Console.ReadLine());

Console.WriteLine("What school do you go to?");
string school = Console.ReadLine();
 
Console.WriteLine("Hello! My name is " + userName);
Console.WriteLine("I am " + userAge + " years old");
Console.WriteLine("Next year I will be " + userNextAge);
Console.WriteLine("I have " + numberOfPets + " pets");
Console.WriteLine("I attend " + school);
```