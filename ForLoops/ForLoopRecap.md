# For Loops Recap
This week's major topics were loops! Specifically For loops. So let's do a quick recap of the structure of these loops.

```cs
for (int i = 0; i < length; i++)
{
    //do something
}
```

## Initialization
`for` loops are great when we know how many times we need to run through a process. It's structure allows us to declare how many times we wish to run through and we can even control how fast we reach that quote. So let's take a step back and pick apart its structure.

```cs
int i = 0;
```

This is our initialization of the variable we are going to use to iterate through this loop. We can set the initial value to whatever makes sense for our application. It's important to note, we can use this variable within our loop however we would like but once we exit our loop this variable is no longer available to us.

## Condition
```cs
i < length;
```

This is our condition, as long as this statement returns `true` our loop will continue to execute. The evaluation takes place before our loop executes, and the loop will continue until this evaluates to false!

## Increment
```cs
i++
```

This is where we increment our initialized variable. In order for our loop to eventually come to an end we need to modify the value of `i` since that’s what our `for` loop looks for, and this where we do it. We don’t have to increase the value by `1 (`++`), we can modify it however we would like.

## Example
As an example lets write a program that will write 0-10 to the console window.
 
```cs
for (int i = 0; i <= 10; i++)
{
    Console.WriteLine(i);
}

/* This prints the following to the console. 
0
1
2
3
4
5
6
7
8
9
10
*/
```