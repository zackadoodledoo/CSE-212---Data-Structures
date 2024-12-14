## Stack
## Introduction:
A stack is a fundamental data structure that operates on the principle of Last In, First Out (LIFO). Picture a stack of plates in a cafeteria: the last plate placed onto the stack is the first one to be removed. In this section, we'll explore the definition of a stack and its real-world applications.

A stack is a LIFO (toward the end in first out) information structure. Consider stacking an assortment of things where anything you embed in a stack will be set at the top and on the off chance that you want to eliminate something, it will be taken out from the top. A pile of plates or a book stack are two normal instances of a stack.

## Definition of a Stack (LIFO - Last In, First Out):
A stack is a linear data structure that follows the Last In, First Out (LIFO) principle. This means that the last element added to the stack will be the first one to be removed. 

![alt text](<Picture Files/Stack.jpg>)

## Real-world examples of stacks:
Stacks are ubiquitous in both the digital and physical worlds. Consider the Undo/Redo functionality in text editors or graphic design software. Each action performed is added to a stack, allowing users to backtrack through their history. Similarly, in programming, the call stack manages function calls during program execution, ensuring that each function call is processed in the reverse order of its invocation.

## Operations:

![alt text](<Picture Files/Stack2.jpg>)

Push: Adding an element to the top of the stack. Push in a stack implies adding components to the stack.


Time Complexity: O(1)

Explanation: Since you're adding the element to the top of the stack, regardless of the size of the stack, the time taken is constant.

Pop: Removing and returning the top element from the stack. Pop in a stack implies eliminating a component from the stack.

Look: A Peek activity returns the last added component in the stack or the top component of the stack.

Time Complexity: O(1)
Explanation: Similar to push, popping from the top of the stack can be done in constant time, regardless of the stack's size.

Size: Returning the number of elements currently in the stack.
Time Complexity: O(1)

Explanation: To keep track of the number of elements in the stack, most implementations maintain a variable that stores this count. Accessing this count variable takes constant time.

Empty: Checking if the stack is empty.

Time Complexity: O(1)

Explanation: Similar to the size operation, checking whether the stack is empty typically involves examining a single variable or condition, which can be done in constant time.

## Generic Stack in C#:

The Generic Stack in C# is an assortment class that chips away at the guideline of Last In First Out (LIFO) and this class is available in System.Collections.Generic namespace.

This Stack assortment class is practically equivalent to a pile of plates. For instance, to add another plate to the heap of plates, then, at that point, we will just put it on top of the multitude of previously existing plates.

Additionally, to eliminate a plate from the stack, then, at that point, we will just eliminate the one that we have last added. The stack assortment class likewise works in the comparable design. The last thing to be added (pushed) to the stack will be the main thing to be taken out (flew) from the stack.

## C# Stack with Examples:

A Stack addresses a rearward in, the first-out assortment of items. It is utilized when you want toward the end, first-out admittance to things. It is both a nonexclusive and non-conventional kind of assortment.


The nonexclusive stack is characterized in System.Collections.Generic namespace through the non-conventional stack is characterized under System. Collections namespace, here we will talk about non-conventional sort stack. A stack is utilized to make a unique assortment that develops, as indicated by the need of your program. In a stack, you can store components of similar sort or various sorts.


## Significant Points:
The Stack class executes the IEnumerable, ICollection, and ICloneable connection points.
Whenever you add a thing in the rundown, it is called pushing the component.
Whenever you eliminate it, it is called popping the component.
The limit of a Stack is the number of components the Stack can hold. As components are added to a Stack, the limit is consequently expanded as expected through redistribution.
In Stack, you are permitted to store copy components.
A Stack acknowledges invalid as a legitimate incentive for reference types.

How to make a Stack?
Stack class has three constructors which are utilized to make a stack which is as per the following:

Stack(): This constructor is utilized to make a case of the Stack class which is vacant and has the default introductory limit.

Stack(ICollection): This constructor is utilized to make an occasion of the Stack class which contains components duplicated from the predefined assortment, and has a similar beginning limit as the number of components replicated.

Stack(Int32): This constructor is utilized to make an example of the Stack class which is unfilled and has determined introductory limit or the default starting limit, whichever is more noteworthy.


We should perceive how to make a stack utilizing Stack() constructor:
Stage 1: Include System.Collections namespace in your program with the assistance of utilizing catchphrases.

```c#
utilizing System. Collections;
```

Stage 2: Create a stack utilizing Stack class as displayed beneath:

```c#
Stack stack_name = new Stack();
```

Stage 3: If you need to add components to your stack, then, at that point, use Push() technique to add components in your stack. As displayed in the beneath model.


How to eliminate components from the Stack?
In Stack, you are permitted to eliminate components from the stack. The Stack class gives two distinct techniques to eliminate components and the strategies are:

Clear: This strategy is utilized to eliminate every one of the articles from the stack.

Pop: This technique eliminates the starting component of the stack.


Stack<'T>. Pop Method is utilized to eliminate and return the item at the highest point of the Stack<'T>. This strategy goes under the System.Collections.Generic namespace.

Stack addresses a rearward in, first out an assortment of articles. It is utilized when you really want a rearward in, first-out admittance to things. At the point when you add a thing in the rundown, it is called pushing the thing and when you eliminate it, it is called popping the thing. Stack<'T>. Clear Method is utilized to Removes all objects from the Stack<'T>. This technique is an O(n) activity, where n is Count.


Properties:

The limit of a Stack is the number of components the Stack can hold. As components are added to a Stack, the limit is naturally expanded as expected through redistribution.
Assuming that Count is not exactly the limit of the stack, Push is an O(1) activity. Assuming that the limit should be expanded to oblige the new component, Push turns into an O(n) activity, where n is Count. Pop is an O(1) activity.
Stack acknowledges invalid as a legitimate worth and permits copy components.

How to get the highest component of the Stack?
In Stack, you can without much of a stretch observe the highest component of the stack by utilizing the accompanying techniques given by the Stack class:

Step by step explanation :

Suppose the elements are pushed onto the stack in the order {4, 2, 14, 1, 18} .

Step 1 : Push 4, Current max : 4

Step 2 : Push 2, Current max : 4

Step 3 : Push 14, Current max : 14

Step 4 : Push 1, Current max : 14

Step 5 : Push 18, Current max : 18

Step 6 : Pop 18, Current max : 14


How to take a look at the accessibility of components in the stack?
In a stack, you can check whether or not the given component is available utilizing Contains () technique. Or then again as such, to look through a component in the given stack use Contains () technique. This technique returns valid assuming that the component is present in the stack. In any case, get back bogus.


Note: The Contains () strategy takes O(n) time to check on the off chance that the component exists in the stack. This ought to be thought about while utilizing this strategy.


How to carry out a stack which will uphold the following activities in O(1) time intricacy?

1) push() which adds a component to the highest point of the stack.
2) pop() which eliminates a component from the top of the stack.
3) find middle() which will return the center component of the stack.
4) deleteMiddle() which will erase the center component.

Structure:
In this program, the stack neighborhood variable is doled out to another Stack containing three numbers. The ints were added with the 10000 last. Next in Main the qualities are printed out to the Console. Stack addresses a toward the end in, first out assortment of item. It is utilized when you really want a rearward in, first-out admittance to things. At the point when you add a thing in the rundown, it is called pushing the thing and when you eliminate it, it is called popping the thing.


Tip: You can see that 10000 is shown first. This is clarified by the LIFO idea toward the end in first out.

LIFO: The last component added (with Push) to Stack is the first eliminated (with Pop).

Pop. Here we see the Pop technique on Stack and the Peek strategy. Whenever you call Pop, the components from the highest point of the Stack are returned, and the component is eliminated from the assortment.

Next: This model uses a similar Stack assortment as above, and that implies Pop brings 10000 back.

Too: It utilizes Peek, which does likewise as Pop yet doesn’t eliminate the component.

Pop and Peek both follow up on the highest point of Stack, meaning the component most as of late added. They likewise both return that top worth. Be that as it may, Peek doesn’t eliminate the component from the Stack assortment. It just gets the worth it “looks” at the worth.

Furthermore: Pop eliminates the reference. On the off chance that you call Pop, thereafter Peek and Pop will return the following worth when they are called.

Clear, count: You can utilize Clear and Count on your Stack. These strategies won’t raise special cases except if your Stack reference is invalid. The Count property is utilized without enclosure, while Clear() is a parameter less strategy.

Note: The model gets the Stack utilized in the above models, then, at that point, counts it, clears it, lastly counts it once more.


## The Advantage and Disadvantage of a stack in collection in C#:

## Advantage:

- In stack, the request in which the information shows up is significant. Stacks are great for authorizing consecutive principles of access i.e., LIFO.
- Stacks are utilized for switching things. If you push something, say a String onto a Stack each character in turn, and afterward build a String from the individuals flew off the Stack, then, at that point, the String is switched.
- Simple to begin
- Less Hardware Requirement
- Cross-Platform
- Assists you with dealing with the information in a Last In First Out (LIFO) technique which is preposterous with Linked rundown and exhibit.
- At the point when a capacity is known as the neighborhood factors are put away in a stack, and it is consequently

## Disadvantage

- Not adaptable
- Absence of scalability
- Unfit to Copy and Paste
- In light of dynamic memory allotment on the off chance that we did not utilize all memory space then there will be wastage of memory space.

![alt text](<Picture Files/Stack example.jpg>)

## Example Problem: 
Implement a stack to reverse a string.

```c#
using System;
using System.Collections.Generic;

public class StackReverseString
{
    public static string ReverseString(string input)
    {
        Stack<char> stack = new Stack<char>();

        foreach (char c in input)
        {
            stack.Push(c);
        }

        char[] reversedArray = new char[input.Length];
        int index = 0;

        while (stack.Count > 0)
        {
            reversedArray[index++] = stack.Pop();
        }

        return new string(reversedArray);
    }

    public static void Main()
    {
        string original = "Hello, World!";
        string reversed = ReverseString(original);

        Console.WriteLine("Original String: " + original);
        Console.WriteLine("Reversed String: " + reversed);
    }
}

```

## Explanation:
StackReverseString Class: Contains the method to reverse a string using a stack.

ReverseString(string input): Pushes each character of the input string onto a stack, then pops them off to create the reversed string.

Main Method: Tests the ReverseString method with an example string.
Solution:

The provided code takes an input string, reverses it using a stack, and prints both the original and reversed strings.




## Problem to Solve: 
Use a stack to validate balanced parentheses in an expression.

```c#
using System;
using System.Collections.Generic;

public class StackBalancedParentheses
{
    public static bool IsBalanced(string expression)
    {
        // Enter code here
    }

    public static void Main()
    {
       // Enter code here
    }
}


```



















































































## Answer to the problem:

```c#
using System;
using System.Collections.Generic;

public class StackBalancedParentheses
{
    public static bool IsBalanced(string expression)
    {
        Stack<char> stack = new Stack<char>();

        foreach (char c in expression)
        {
            if (c == '(' || c == '{' || c == '[')
            {
                stack.Push(c);
            }
            else if (c == ')' || c == '}' || c == ']')
            {
                if (stack.Count == 0)
                {
                    return false;
                }

                char top = stack.Pop();
                if ((c == ')' && top != '(') ||
                    (c == '}' && top != '{') ||
                    (c == ']' && top != '['))
                {
                    return false;
                }
            }
        }

        return stack.Count == 0;
    }

    public static void Main()
    {
        string expression = "{[()]}";
        bool isBalanced = IsBalanced(expression);

        Console.WriteLine("Expression: " + expression);
        Console.WriteLine("Is Balanced: " + isBalanced);
    }
}
```