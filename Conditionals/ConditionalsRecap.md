# Conditionals
We use conditional statements in code to help us make decisions if a condition is true or false.
The section in the parentheses is what we're evaluating to either `true` or `false`. If the value we evaluate is `true`, we'll do the section inside the `if` block. 
We also looked at `else` statements which allow us to run another section of code if the condition we're checking is `false`.

Example:

```cs
Console.WriteLine("What percent did you get on your test??"); 
string testResult = Console.ReadLine();
int myScore = Convert.ToInt32(testResult);

if(myScore >= 90)
{
 	Console.WriteLine("Awesome! You got an A.");
}
else if (myScore >= 80)
{
 	Console.WriteLine("Good job, you got a B.");
}
else
{
 	Console.WriteLine("You should keep studying.");
}
```

In this example, if the user enters an test score greater than or equal to `90`, then the section inside the parenthesis evaluates to true, and the first block of code is run.

If we don’t enter the first code block because our score is say, `85`, we would then evaluate the 2nd block, `(myScore >= 80)`. This expression would equate to true so we would then write to the console "Good job, you got a B".

If the test score is `79` or less the code inside the `else` block runs!
