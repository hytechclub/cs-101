# Conditional Exercises
After completing the [code-along activity](ConditionalsCodeAlong.md), work on the exercises below.

## One More Question
Building from the Choose Your Path project, add an additional question to make the game a little more involved.

1. In the **main.cs** file, in the `Main` body, find the final `if` statement
1. Above that, use `Console.WriteLine` to ask another question - `"You get to school. Do you stop at the water fountain?"`
1. Display the options: `"  A. Yes"` / `"  B. No"`
1. Use `Console.Write` to print `"> "`
1. Under that, create a new `string` variable named `choice3`
1. Set the `choice3` variable to `Console.ReadLine()`
1. Use `Console.Clear()` to clear the console
1. Under that, create an `if` structure
	- `if` keyword
	- Parentheses (condition)
	- Curly brackets (body)
1. For the condition (between the parentheses), check if `choice3` equals `"A"`
1. In the body (between the curly brackets), set the `health` variable to `health + 1`
1. Also in the body of the `if`, display a message saying "You drink some water."
1. Under the `if` body (after the `}`), create an `else if` structure
	- `else if` keyword
	- Parentheses (condition)
	- Curly brackets (body)
1. For the `else if` condition, check if `choice3` equals `"B"`
1. In the body of the `else if`, set the `health` variable to `health - 1`
1. Also in the body of the `else if`, display a message saying "You do not drink water."

Run the program again, and verify that the third question properly impacts the game!

## A New Project - Chat Bot
Using conditional statements, a whole lot of things are possible.

![](https://i.imgur.com/KETf3GL.jpg)

While the definition of "artificial intelligence" may not always include simple `if` statements, it is certainly possible to create the illusion of intelligence using conditionals!

Create a program that can respond to a number of different chat messages.

### Setup
Start by creating the new project.

1. Create a [new C# Repl project](https://repl.it/new/csharp)
1. Name it "Chatbot"
1. In the **main.cs** file, in the `Main` body, set the text color:  
    ```cs
    Console.ForegroundColor = ConsoleColor.Black;
    ```
1. Under that, set the background color:  
    ```cs
    Console.BackgroundColor = ConsoleColor.White;
    ```
1. Under that, clear the console to make it a little cleaner:  
    ```cs
    Console.Clear();
    ```
1. Next, use `Console.WriteLine` to display a message saying "Welcome to the Chatbot"
1. Under that, add an empty `Console.WriteLine` to make some extra space

Run the program, and verify that the message appears in the proper color.

### A Question
Next, the program should ask the user a question. This can theoretically be any question.

1. Under the lowest `Console.WriteLine`, create another `Console.WriteLine`
1. Display a message with a question, like "What do you want to say?"
1. Under that, create a new `string` variable named `answer`
1. Set the `answer` variable to be a `Console.ReadLine()`

Run the program. Verify that the question appears, and it is possible to enter an answer!

### A Response
Now that the user has entered an answer, it is possible to respond to that answer. The response should depend on what the user said. For example, if the user says "You talkin' to me?" the bot could say "Well I'm the only one here."

Use an `if` statement to create that response!

1. Under the `answer` variable, create an `if` structure
	- `if` keyword
	- Parentheses (condition)
	- Curly brackets (body)
1. For the condition (between the parentheses), check if the `answer` variable equals `"You talkin' to me?"`
1. In the body (between the curly brackets), add a `Console.WriteLine` statement
1. Make the `WriteLine` display a message saying `"Well I'm the only one here."`

Run the program again. Verify that entering the exact answer "You talkin' to me?" will make the program display the correct response!

The code should look something like this:

```cs
if (answer == "You talkin' to me?")
{
	Console.WriteLine("Well I'm the only one here.");
}
```

### Other Responses
Using the same type of structure, it's possible to make the program respond to any message at all! Add some more `if` statements, each of them checking the `answer` value and printing a different response based on the answer. Feel free to customize the responses, or use the ones from this table:

| `answer` | Response |
|-|-|
| "You killed my father." | "No, I am your father!" |
| "I'm going to Mordor alone." | "Of course you are, and I'm coming with you!" |
| "You look like my grandpa." | "Oh, is your grandpa super cool?" |
| "Your grandpa invented baseball?" | "Did I say baseball? I meant spray-on eyebrows." |
| "Is this the Krusty Krab?" | "No, this is Patrick." |
| "This is the worst day of my life." | "The worst day of your life *so far*." |

### Dynamic Colors
Instead of simply setting the colors at the beginning of the program, ask the user which colors to use!

1. At the top of the `Main` body, above the `Console.ForegroundColor`, make a new space
1. There, use `Console.WriteLine` to display a message: "Which text color?"
1. Under that, create a new `string` variable named `colorAnswer`
1. Set the `colorAnswer` variable to be `Console.ReadLine()`
1. Under that, create an `if` structure
	- `if` keyword
	- Parentheses
	- Curly brackets
1. For the condition (between the parentheses), check if `colorAnswer` is `Red`
1. In the body (between the curly brackets), use `Console.ForegroundColor = ConsoleColor.Red` to set the color

Run the program, and verify that it is possible to select "Red" as the text color!

Add additional `if` structures for some additional colors, like `ConsoleColor.Green`, `ConsoleColor.Cyan`, and `ConsoleColor.Yellow`.

## Challenges
After completing these exercises, start working on the [challenges](ConditionalChallenges.md).