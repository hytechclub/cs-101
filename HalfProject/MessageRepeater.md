# Message Repeater
This program should repeat a message a number of times using a user-defined color. Start by creating a [new Repl project](https://replit.com/new/csharp), and then complete each part below.

All changes should take place in the `Main` block (between the `{` and `}`). Refer back to the previous lessons for help.

## Part 1 - User Input
The first step is to retrieve some information from the user. Use `Console.WriteLine`, `Convert.ToInt32`, and `Console.ReadLine` to accomplish the two pieces below.

#### How Many Times?
Print out a message asking the user how many times they would like to repeat the message. Then, store their answer in a variable, converted to the proper numeric type.

#### What Color?
Print out a message asking the user which color they would like to use. Then, store their answer in a new variable.

## Part 2 - Color Changer
The next step is to change the color of the text in the console based on the color the user entered. Use `if`/`else if` and `Console.ForegroundColor` to accomplish this.

Support at least three different colors from this list:
- `ConsoleColor.Red`
- `ConsoleColor.Blue`
- `ConsoleColor.Green`
- `ConsoleColor.Yellow`
- `ConsoleColor.Cyan`
- `ConsoleColor.Magenta`

## Part 3 - Repeating a Message
The final step is to print out a message the proper number of times. Feel free to use any appropriate message. Use a `while` loop and `Console.WriteLine` to accomplish this. To loop through a certain number of times, try this strategy:

- Set a new variable to `0`
- For the `while` condition (between parentheses), check if the new variable is less than the number of times to repeat
- In the `while` body (between the curly brackets), add any code that will be repeated
- Also in the `while` body, increment the new variable by 1

## Part 4 - Testing the Program
Now that all the code should be complete, test the program and make sure it works. As the user, follow these steps:

- The program should print a message asking how many times to repeat
- Enter a number of times (like 10)
- The program should print a message asking which color to use
- Enter a color (like Red)
- The program should repeat the message the proper number of times in the proper color!

It should look something like this:

![](https://i.imgur.com/hwvldnK.png)