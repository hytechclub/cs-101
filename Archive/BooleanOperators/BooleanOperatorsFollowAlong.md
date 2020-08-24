# Boolean Operators - Follow-Along
Read through the following for some examples of boolean operators.

# `&&` (Conditional And)
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

This `if` statement will only write "I am going to build a snowman" if BOTH the `snowOnGround` boolean AND the `foundGloves` boolean are `true`. If there's snow on the ground, but you did not find your gloves, you will not be able to build your snowman. If you found your gloves, but there's no snow outside, you won't be able to build that guy either. And if you don't have gloves and there's no snow, well you're really out of luck there. You'll have to stay inside.

## `||` (Conditional Or)
Conditional Ors are evaluated to `true` if one of the conditions is `true`. Let's say you're considering eating some soup. You will be hungry for soup if it's snowy out, OR if you're feeling sick. Let's look at how this might look in code:

```cs
bool snowOnGround;
bool feelingSick;
if (snowOnGround || feelingSick)
{
    Console.WriteLine("I am going to eat some soup");
} 
else 
{
    Console.WriteLine("I do not want soup");
} 
```

We will write out "I am going to eat some soup" if it's snowy OR if you feel sick OR if both are true. However, if both `snowOnGround` and `feelingSick` are set to `false`, you will not go into the curly braces immediately after the `if` statement. Instead you will go into the else block, and we will write, "I am going hungry for now".

## `!` (Not) 
Finally, we learned about the most exciting operator: not! The not symbol is the exclamation point (`!`). What this does is flip the boolean value from `true` to `false` or from `false` to `true`. Let's say you want to go to school, but you can only go to school if you are NOT sick:

```cs
bool feelingSick;
if (!feelingSick) 
{
    Console.WriteLine("I am going to school!");
}
```

The exclamation point flips the value of `feelingSick`. So if `feelingSick` is set to `true`, then the `if` statement (`!feelingSick`) will evaluate to `false` and the program will not enter the if block. If `feelingSick` is set to `false` then the if `statement` (`!feelingSick`) will evaluate to `true` and the program will write "I am going to school!" 