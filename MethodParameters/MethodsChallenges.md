# Methods Challenges
Complete the exercises below using a single `.cs` file. In the `Main` method, _call_ each of the methods you _define_.

## 1 - Calculate the next leap years
Write a method that takes in a year and determines if it is a leap year.

Leap years are defined as follows:
* If the year is divisible by 4 then it is a leap year
* Except if the year is divisible by 100 then it IS NOT a lear year
* Except if the year is divisible by 400 then it IS a leap year

Write a program that asks the user for a year, and writes a message to the console telling the user whether or not the year they entered was a leap year.

### Challenge
Write a method that does the following:
* Using the current year, generate the next 50 leap years
* Print these years out to the console

## 2 - Bunny Eyes
Define a method named `drawBunny` that prints an ASCII bunny to the console. It should look something like this:

```
() ()
(. .)
(u u)
```

Once the method has been defined, update it so that it has a _parameter_. The parameter should determine the eyes for the bunny.

### Example 1
```cs
drawBunny("*");
```

```
() ()
(* *)
(u u)
```

### Example 2
```cs
drawBunny("-");
```

```
() ()
(- -)
(u u)
```

## 3 - Countdown
Create a program that will ask the user for a date and the name of an event, and then display how many days there are until that date. For example, if today was 03/10/20 and the user entered `05/01/2020` as the date and `my birthday` as the event name, the program should say "There are 52 days until my birthday."

1. Write a method that takes the date and determines the number of days until that date
1. Write another that asks the user to input a date and event name and outputs the message with the countdown

### Challenge items
- The program should calculate the amount of time remaining in years, months, weeks, days, hours, minutes, and seconds
- The program should properly handle invalid input (e.g., fake months like `Smarch` or invalid numbers like `the 28.3th of April`)
- The program should be able to handle a date provided in as many forms as possible (e.g., `03/09/2019`, `March 9th, 2019`, `9 Mar 2019`, `the 9th of March in 2019`)

### Extra challenge
- The program should be able to display multiple countdowns at once
- The program should store each countdown name/date in a text file, and load them from the text file each time the program runs

## 4 - While Loop Methods
Update the code from the [While Loop Challenges](../WhileLoops/WhileLoopChallenges.md) so that each program is defined as one method. The `Main` method should have a menu that allows the user to select which method to run.

## 5 - Recursion
>[Land of Lakes Example](https://media0.giphy.com/media/l0HUi9wxwHRrYBKSY/giphy.gif)

In computer science, [**recursion**](https://en.wikipedia.org/wiki/Recursion) occurs when a method calls itself in its own definition. Read through [this article](https://www.geeksforgeeks.org/recursion/) to learn more.

### Fibonacci Sequence
The [**Fibonacci Sequence**](https://www.mathsisfun.com/numbers/fibonacci-sequence.html) is a famous bit of mathematics, and it happens to have a recursive definition. The first two values in the sequence are `0` and `1` (essentially 2 base cases). Each subsequent value is the sum of the previous two values, so the whole sequence is:

```
0, 1, 1, 2, 3, 5, 8, 13, 21... and so on
```

Define a recursive `fibonacci` method that takes a number `n` and returns the `n`th fibonacci number, with `n=0` representing the start of the sequence.

#### Examples
- `fibonacci(0)` returns `0`
- `fibonacci(1)` returns `1`
- `fibonacci(2)` returns `1`
- `fibonacci(3)` returns `2`
- `fibonacci(4)` returns `3`
- `fibonacci(5)` returns `5`
- `fibonacci(6)` returns `8`

#### Hint
The trick to defining a recursive method is to pretend the method is already defined. In the body of the `fibonacci` method, call the `fibonacci` method as if it will always return exactly what it should return.