# While Loops Recap
This week's major topics were loops! Specifically `while` loops. So let's do a quick recap of the structure of these loops.

```cs
while (true)
{
    // do something
}
```

While loops are ideal when we don't know exactly how many times we need to execute our code, but we have a way of testing if we need to run it again, specifically using some type of Boolean expression.
 
The while loop only has one condition we need to worry about:
 
```cs
while (/* some condition is TRUE */)
```
 
So what can this some condition be? Well it can be anything that equates to a boolean expression, some examples:
 
```cs
while (Console.Readline() != "STOP") // as long as our user doesn't type 'STOP' we keep running our code
```
 
```cs
int myInt = 0;
while (myInt <= 7) // as long as myInt is less than or equal to 7 we keep running our code
{
    Console.WriteLine(myInt);
}
```

Now my last example in particular has a problem, can you spot what it is? Currently `myInt` never changes values, so my program will just print the value `0` indefinitely.