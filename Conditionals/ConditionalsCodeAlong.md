# Grade Level Condition
Follow these steps to see some conditional statements in action:

1. Construct basic `if` statement (plug in `true`) that runs a `WriteLine()`
2. Next, gather user input (what grade are you in?) and run a conditional statement: `if (grade <= 5) {}`
3. Add the else if statement: `else if (grade <= 8) {}`
4. Add the else statement: `else {}`

### Code
```cs
/*
if(true)
{
    Console.WriteLine("I'm inside the 'if' statement!");
}
*/

Console.WriteLine("What grade are you in?");
int studentGrade = Convert.toInt32(Console.ReadLine());

if (grade <= 5)
{
    Console.WriteLine("Elementary");
}
else if (grade <= 8)
{
    Console.WriteLine("Middle School");
}
else
{
    Console.WriteLine("High School")
}
```