# Boolean Operators Recap
This week we continued learning about conditional statements and branching by talking about Boolean Operators.

You've already seen some of these, like `>`, `<`, `>=`, `<=`, `==` and `!=` (reminder if you're trying to saying greater than or equal to, you must put the > symbol before the = symbol. Same goes for less than or equal.) But this week we also learned about `&&` (the conditional And) and `||` (the conditional Or). The symbol for the conditional or is the two pipes and it can be found above the enter key or your keyboard.

## `&&` (Conditional And)

Let's say you want to go build a snowman but you don't want your fingers to get cold. This means that you can only build that snowman if there is snow on the ground AND if you can find your gloves. The way our English and works in this sentence is pretty similar to how it works in code:

```cs
bool snowOnGround; 
bool foundGloves; 
if (snowOnGround && foundGloves) 
{ 
    Console.WriteLine("I am going to build a snowman"); 
} 
else 
{
    Console.WriteLine("I am staying inside");
}
```

This if statement will only write "I am going to build a snowman" if BOTH the `snowOnGround` boolean AND the `foundGloves` boolean is true. If there's snow on the ground, but you did not find your gloves, you will not be able to build your snowman. If you found your gloves, but there's no snow outside, you won't be able to build that guy either. And if you don't have gloves and there's no snow, well you're really out of luck there. You'll have to stay inside.

## `||` (Conditional Or)

Conditional Ors are evaluated to true if one of the conditions is true. Let's say you're hungry for a sandwich and found the bread and cheese and now it's time to go looking for some protein. You're very particular about your sandwiches and will only eat a ham and cheese sandwich, or a turkey and cheese sandwich. This means if you can't find some ham OR some turkey you won't be able to make your tasty snack. Let's look at how this might look in code:

```cs
bool foundHam;
bool foundTurkey;
if (foundHam || foundTurkey)
{
    Console.WriteLine("I am going to make a sandwich");
} 
else 
{
    Console.WriteLine("I am going hungry for now");
} 
```

We will write out "I am going to make a sandwhich" if you find ham OR if you find turkey OR if you find both (then you get to choose your protein!). However, if both `foundHam` and `foundTurkey` are set to false, you will not go into the curly braces immediately after the `if` statement. Instead you will go into the `else` block, and we will write, "I am going hungry for now".

 

Finally, we learned about the most exciting operator: not! The not symbol is the exclamation point (`!`) What this does is flip the boolean value from `true` to `false` or from `false` to t`rue. Let's say you want to go to the pool, but the pool is only open if it is NOT raining:

```cs
bool isRaining;
if (!isRaining) 
{
    Console.WriteLine("I am going to the pool");
}
else 
{ 
    Console.WriteLine("I am not going to the pool");
}
```

The exclamation point flips the value if `isRaining`. So if it `isRaining` is set to `true`, then the if statement (`!isRaining`) will evaluate to `false` and you'll go into your `else` block where you say "I am not going to the pool" is. If `isRaining` is set to `false` then the `if` statement (`!isRaining`) will evaluate to `true` and you'll write "I am going to the pool"