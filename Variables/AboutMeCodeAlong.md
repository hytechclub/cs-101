# About Me Code-Along: Hard-Coded Values
Create a program that stores some information about a user, and then prints it out in a sentence format. Start by creating a new C# Repl, and then follow the steps below.

## Name Variable
First, _declare_ and _set_ a new variable. This variable will hold a name; feel free to use your own name, or any other name you'd like.

1. Remove any code from the `Main` code block
1. Create a new `string` variable named `userName` with `string userName`
1. Set the value of the variable to a new string with `= ""`
1. Fill out the name between the opening and closing quotation marks
1. Add a semi-colon at the end

```cs
string userName = "Jordan Conrad";
```

## Other Variables
After the first variable is declared and set, it's time to add some additional variables. Remember to end each statement with a semi-colon!

1. Make a new line under the first variable
1. Declare a new `int` variable named `userAge`, and set it equal to any age (e.g. `27`)
1. Make another new line
1. Declare another `int` variable named `numberOfPets`, and set it equal to any number (e.g. `2`)
1. Make another new line
1. Declare a `string` variable named `school`, and set it equal to a value between quotes (`""`)
1. Fill out a value for the `school` variable (e.g. `"Medina High School"`)

Run the program, and make sure there are no errors.

```cs
int userAge = 27;
int numberOfPets = 2;
string school = "Medina High School";
```

## Displaying the Name Information
Now that the information is properly stored in variables, try displaying it in a sentence format. Start with the `userName` value.

1. Make a new line under the variables
1. Create a `Console.WriteLine();` statement to display a message
1. Within the parentheses for the `Console.WriteLine();`, add a set of double quotes (`""`)
1. Within the double quotes, type out "Hello! My name is "
    - Make sure to include the space
1. After the ending quote, add a `+` and the `userName` variable

Run the program, and verify that the sentence appears in the console!

```cs
Console.WriteLine("Hello! My name is " + userName);
```

## Displaying the Other Information
Next, display the rest of the information.

1. Under the previous statement, add another `Console.WriteLine();`
1. Within the parentheses, add a string that says "I am "
1. After the quote, use `+` to add the `userAge` variable
1. After the variable, use `+` _again_ to complete the message with " years old"

```cs
Console.WriteLine("I am " + userAge + " years old");
```

1. Under that, add another `Console.WriteLine();`
1. Within the parentheses, add a string that says "I have "
1. After the quote, use `+` to add the `numberOfPets` variable
1. After the variable, use `+` _again_ to complete the message with " pets

```cs
Console.WriteLine("I have " + numberOfPets + " pets");
```

1. Under that, add another `Console.WriteLine();`
1. Within the parentheses, add a string that says "I went to school at "
1. After the quote, use `+` to add the `school` variable

```cs
Console.WriteLine("I went to school at " + school);
```

Run the code, and make sure all the information is displayed properly!

## Final Code
```cs
string userName = "Jordan Conrad";
int userAge = 27;
int numberOfPets = 2;
string school = "Medina High School";

Console.WriteLine("Hello! My name is " + userName);
Console.WriteLine("I am " + userAge + " years old");
Console.WriteLine("I have " + numberOfPets + " pets");
Console.WriteLine("I went to school at " + school);
```