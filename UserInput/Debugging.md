# Debugging
One of the most important parts of programming is [debugging](https://en.wikipedia.org/wiki/Debugging). **Debugging** is the process of finding and fixing errors in computer programs. Legend has it that computer science pioneer Admiral Grace Hopper discovered the first ever computer bug back in the 1940s: an actual physical moth.

![](https://i.imgur.com/WkKTe19.jpg)

Today, most debugging is done by walking through the code step-by-step. Replit does not have this capability for C#, but there are other ways to test code.

## Error Messages
The most basic form of debugging involves running the code, and looking for error messages. They often look something like this:

![](https://i.imgur.com/jkirlQL.png)

An error like that one contains some important information:

- File: `main.cs`
- Line Number and Position: `(5,5)`
- Error Code: `error CS0103`
- Error Message: `The name 'console' does not exist in the current context`

Using these clues, it will be possible to find the issue in the code.

## Misbehaving Code
If there are no errors, but the program does not run as expected, it can be a little more difficult to debug (especially without a true debugger tool).

One of the most common ways to figure out what's happening is to use print statements. In the case of C#, this means using `Console.WriteLine`. Printing out the value of a variable at a certain point in the code can make it much easier to tell what's going on. For example, in a complex math equation:

```cs
int velocity = 2;
int acceleration = 1;
int time = 10;

int start = 5 + 9;
int additionalVel = velocity * time;
int additionalAcc = .5 * acceleration * time * time;

Console.WriteLine(start + additionalVel + additionalAcc);
```

If the result is not expected, printing out each value (`start`, `additionalVel`, and `additionalAcc`) may indicate where the code went wrong. If the value of `start` is correct, and the value of `additionalVel` is correct, but the value of `additionalAcc` is _not_ correct, that means something is wrong with the `int additionalAcc` line:

```cs
int velocity = 2;
int acceleration = 1;
int time = 10;

int start = 5 + 9;
Console.WriteLine(start);

int additionalVel = velocity * time;
Console.WriteLine(additionalVel);

int additionalAcc = .5 * acceleration * time * time;
Console.WriteLine(additionalAcc);

Console.WriteLine(start + additionalVel + additionalAcc);
```

## A Buggy Example
Try out an example to see how the bug fixing process can work. There are five total bugs to be found! Fork [this Repl project](https://replit.com/@JosephMaxwell/DebuggingExample) to begin.

### Bug 1
Run the code to see what's happening. Oh no! There are multiple errors! In Replit for C#, error messages appear in red.

```
main.cs(6,2): error CS1525: Unexpected symbol 'Console'
main.cs(7,78): error CS1525: Unexpected symbol ';', expecting ')' or ','
```

Whenever there are multiple errors, try not to become to overwhelmed. Start with the first one:

```
main.cs(6,2): error CS1525: Unexpected symbol 'Console'
```

It looks like something is wrong on line **6**... take a look at that line:

```cs
Console.WriteLine("Welcome to the Graduation Year Calculator!");
```

Is there anything wrong with that code? It actually looks fine... but sometimes, an "Unexpected symbol" error happens on the line _after_ where the error occurs. Check out line **5**:

```cs
Console.Clear()
```

Is there anything wrong with that code? ...Yes! It is missing a semi-colon (`;`). Add a semi-colon to the end of the line, run the code again, and verify that the error message is gone!

### Bug 2
One of the error messages is gone, but there is still one remaining. Take a look at this one:

```
main.cs(7,78): error CS1525: Unexpected symbol ';', expecting ')' or ','
```

Based on the output, something is going wrong on line **7**, at character **78**. The error message says there is a `;` when there should be a `)` or a `,`. Take a look at line **7**:

```cs
Console.WriteLine("We can estimate how long it will be until you graduate.";
```

Toward the end of the statement... aha! There is no closing parenthesis. Before the semi-colon, add a `)`. Run the code again, and verify that _this_ error message is gone!

### Bug 3
Two down, three to go. After fixing those two errors, a couple more have cropped up. As before, start with the first error message:

```
main.cs(9,11): error CS0117: 'System.Console' does not contain a definition for 'Writeline'
```

Based on the message, it is possible to deduce that the error is on line **9**, character **11**. It looks like **Writeline** is not defined, but that's strange... it seems to be working on the other lines. Take a look at the code on line **9**:

```cs
Console.Writeline("");
```

Hmm... I see! Instead of `WriteLine`, it has `Writeline`. The `L` must be capitalized in order for the code to work! Change it to `WriteLine`, run the code again, and verify that the error message disappears.

### Bug 4
Now, only one error should appear when the code runs. Take a look at the message:

```
main.cs(11,21): error CS0029: Cannot implicitly convert type 'string' to 'int'
```

Line **11**, character **21** - it seems to be something related to types. Go to line **11** to see what's happening:

```cs
int age = Console.ReadLine();
```

The syntax all looks okay... what could it be? Oh yeah! `Console.ReadLine()` returns a `string` value, but the `age` variable is an `int`.

One idea would be to change the `int` to `string` in the code, but that will actually mess up some of the code below. Instead, the code should _convert_ the `string` value from `Console.ReadLine` into an `int` value. Luckily, `Convert.ToInt32` does just that.

Wrap the `Console.ReadLine` in a `Convert.ToInt32()`, run the code again, and verify that the error message disappears!

### Bug 5
Now, the program actually runs! Looks like there's nothing left to do... but wait. It would be a good idea to test out the program before calling it a day.

Run the program, enter an age, and see how the calculation works. Not quite as intended. For example, entering `17` will say there are `-35` years until graduation! That's not right. Entering `14` will say there are `-32` years. The program definitely still has a bug.

Looking at the code, it may not be immediately obvious where the bug occurs. One way to figure out what the code is doing is to add `Console.WriteLine` statements under each part, displaying information about the program at a certain point. This can help pinpoint the issue.

1. Add a `Console.WriteLine` statement under `int age` printing out the `age`: `"Age: " + age`
1. Add a `Console.WriteLine` statement under `int birthYear` printing out the `birthYear` value
1. Add additional `Console.WriteLine` statements for the other two variables: `gradYear` and `yearsUntilGraduation`
1. Run the program
1. Enter an age of `17` for testing purposes
1. View the output, and notice that everything seems fine until the `gradYear` variable
1. Check the line where `gradYear` is set... there must be an issue
1. Notice that the calculation is wrong - it should be addition, not subtraction!
1. Fix the bug
1. Remove the extraneous `Console.WriteLine` statements
1. Test the program again, and verify that it works!

Well, that program had a lot of bugs, but fixing them one-by-one makes it much less overwhelming.

## More Bug Fixes
Practice debugging with these additional activities! Visit each Repl project, find the bugs, and make the programs work as intended.

- [Bug 1](https://replit.com/@JosephMaxwell/InputBug-1#main.cs)
- [Bug 2](https://replit.com/@JosephMaxwell/InputBug-2#main.cs)
- [Bug 3](https://replit.com/@JosephMaxwell/InputBug-3#main.cs)
- [Bug 4](https://replit.com/@JosephMaxwell/InputBug-4#main.cs)