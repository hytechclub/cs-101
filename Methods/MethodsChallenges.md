# Methods Challenges
Complete the following challenges.

## _Optional Practice: Bugs_
Visit each of the Repl projects below. They all have something wrong with them; try to fix the errors!

- [Bug 1](https://replit.com/@JosephMaxwell/MethodBug#main.cs)
- [Bug 2](https://replit.com/@JosephMaxwell/MethodBug-1#main.cs)
- [Bug 3](https://replit.com/@JosephMaxwell/MethodBug-2#main.cs)
- [Bug 4](https://replit.com/@JosephMaxwell/MethodBug-3#main.cs)
- [Bug 5](https://replit.com/@JosephMaxwell/MethodBug-4#main.cs)
- [Bug 6](https://replit.com/@JosephMaxwell/MethodBug-5#main.cs)

## Many Methods
Create a new Repl project, and complete the challenges below. For each challenge:

- Define a new method
- Call the method from within the body of the `Main` method

### String Length
Define a method that can display how long a message is.

#### Method Setup
First, _define_ an empty method in the program.

1. Make a new line in the code where a method can be defined  
    ![](https://i.imgur.com/BStHVqz.png)
1. On that line, type in the basic method definition keywords: `public static void`
1. On the same line, type in the method name: `StringLength`
1. On the same line, type in the open and close parentheses: `()`
1. After that, type in a left curly bracket (the right one should appear automatically): `{}`
1. Between the curly brackets, press `Enter` to create a new line

The method should look something like this:
```cs
public static void StringLength() {
    // body of the method: between curly brackets
}
```

Run the code to make sure there are no errors.

#### Adding Code to the Method
Next, it's time to add some code to the method so it actually does something.

1. In the body of the method (between the brackets), add a `Console.WriteLine` command
1. Make the text for the `WriteLine` command say "Enter a message"
1. Beneath the `WriteLine`, declare a new `string` variable named `message`
1. Set the `message` variable to a `Console.ReadLine()` command
1. Beneath that, add another `Console.WriteLine` command
1. For that `WriteLine` command, put `message.Length` between the parentheses
    - This will display the length of the `message` string

At this point, the method should look something like this:
```cs
public static void StringLength() {
    Console.WriteLine("Enter a message");
    string message = Console.ReadLine();
    Console.WriteLine(message.Length);
}
```

Run the code to make sure there are no errors.

#### Calling the Method
Now, all that's left is to _call_ the method. This is where the program will actually run the code within the method.

1. Make a new line in the _body_ of the `Main` method (between the `Main` method brackets)  
    ![](https://i.imgur.com/k5P1NKP.png)
1. On the new line, type in the name of the method: `StringLength`
1. On the same line, type in open and close parentheses: `()`
1. Finally, add a semi-colon at the end of the line: `;`

At this point, the whole program should look something like this:

```cs
using System;

class MainClass {
  public static void Main (string[] args) {
    Console.WriteLine ("Hello World");

    StringLength();
    
  }

  public static void StringLength() {
    Console.WriteLine("Enter a message");
    string message = Console.ReadLine();
    Console.WriteLine(message.Length);
  }

}
```

Run the program, and make sure it works! It should ask for a message, accept an answer in the console, and display the length of the message.

### Times Two
Use the same Repl project as the `StringLength` challenge to complete this one. Create a method that asks the user for a number, and then shows them that number multiplied by two.

#### Method Setup
First, _define_ an empty method in the program.

1. Make a new line in the code where a method can be defined
    - Under the closing curly bracket of the previous method, above the final curly bracket
1. On that line, type in the basic method definition keywords: `public static void`
1. On the same line, type in the method name: `TimesTwo`
1. On the same line, type in the open and close parentheses: `()`
1. After that, type in a left curly bracket (the right one should appear automatically): `{}`
1. Between the curly brackets, press `Enter` to create a new line

Run the code to make sure there are no errors.

#### Adding Code to the Method
Next, it's time to add some code to the method so it actually does something.

1. In the body of the method (between the brackets), add a `Console.WriteLine` command
1. Make the text for the `WriteLine` command say "Enter a number"
1. Beneath the `WriteLine`, declare a new `int` variable named `number`
1. Set the `number` variable to a `Convert.ToInt32(Console.ReadLine())` command
1. Beneath that, add another `Console.WriteLine` command
1. For that `WriteLine` command, put `number * 2` between the parentheses
    - This will display the `number` integer multiplied by 2

Run the code to make sure there are no errors.

#### Calling the Method
Now, all that's left is to _call_ the method. This is where the program will actually run the code within the method.

1. Make a new line in the _body_ of the `Main` method (between the `Main` method brackets)
1. On the new line, type in the name of the method: `TimesTwo`
1. On the same line, type in open and close parentheses: `()`
1. Finally, add a semi-colon at the end of the line: `;`

Run the program, and make sure it works! It should ask for a number, accept an answer in the console, and display the value of the number multiplied by two.

### Ghost
Use the same Repl project as the previous challenges to complete this one. Create a method that prints out a ghost.

#### Method Setup
First, _define_ an empty method in the program.

1. Make a new line in the proper place in the file
1. Write out the basic code for an empty method, named `Ghost`
1. Run the code to make sure there are no errors.

#### Adding Code to the Method
Next, it's time to add some code to the method so it actually does something.

1. In the body of the method (between the brackets), add a `Console.WriteLine` command
1. Paste in the ghost emoji between the double quotes: `👻`
1. Run the code to make sure there are no errors.

#### Calling the Method
Now, all that's left is to _call_ the method. This is where the program will actually run the code within the method.

1. Make a new line in the proper place within the `Main` method
1. Call the method by typing its name followed by parentheses
1. Run the program, and make sure a ghost appears

### (BONUS) Another Emoji
Repeat the steps above to create another emoji-printing method. This method should print out something other than a ghost! Make sure to follow these steps:

1. Setup the method by defining it in the proper place
    - Make sure to give it a good name!
1. Add code to the method
    - Use `Console.WriteLine`, and paste in your favorite emoji between the double quotes
1. Call the method from within the `Main` method
