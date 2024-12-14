## III. Linked List 

![alt text](<Picture Files/LinkedListCover.png>)

## Introduction: 
A linked list is a linear data structure where elements are stored in nodes, each pointing to the next node in the sequence. It's useful for dynamic memory allocation. Linked lists offer flexibility, efficient insertions/deletions, and dynamic memory allocation. Whether you’re building a custom data structure or solving algorithmic problems, understanding linked lists is essential.

## Types of Linked Lists: 
Singly linked lists, doubly linked lists, and circular linked lists.

## 1. Singly Linked List:
Each node points only to the next node. Traversal is forward-only. Commonly used for simple scenarios.

## 2. Doubly Linked List:
Each node points both to the next and previous node. Allows bidirectional traversal. Useful for implementing data structures like LRU caches.

## 3. Circular Linked List:
The last node points back to the first node(circular structure). Usefull for creating circular buffers or scheduling algorithms.

## Implementing a Singly Linked List in c#:

```c#
using System;

public class Node<T>
{
    public T Data { get; set; }
    public Node<T> Next { get; set; }

    public Node(T data)
    {
        Data = data;
        Next = null;
    }
}

public class LinkedList<T>
{
    private Node<T> head;

    public void Add(T data)
    {
        var newNode = new Node<T>(data);
        if (head == null)
            head = newNode;
        else
        {
            var current = head;
            while (current.Next != null)
                current = current.Next;
            current.Next = newNode;
        }
    }

    public void Display()
    {
        var current = head;
        while (current != null)
        {
            Console.Write(current.Data + " ");
            current = current.Next;
        }
        Console.WriteLine();
    }
}

class Program
{
    static void Main()
    {
        var myList = new LinkedList<int>();
        myList.Add(10);
        myList.Add(20);
        myList.Add(30);
        myList.Display(); // Output: 10 20 30
    }
}

```

## Operations on Linked Lists: 
Insertion, deletion, search, and traversal through the list.

## Advantages and Disadvantages: 

## 1.Dynamic Data Structure:
Linked lists can grow and shrink dynamically during runtime. Memory is allocated as needed, avoiding fixed-size constraints.

## 2. Efficient Insertions and Deletions:
Adding or removing elements within a linked list is efficient. No need to shift other elements(as in arrays). Compared to arrays, they allow easier insertion and deletion but have slower access times.

## 3. No Memory Overhead:
Linked lists don't require pre-allocated memory like arrays. Nodes are allocated individually, reducing wasted space.

## 4. Versatility:
Linked lists can be used to implement other data structures(i.e. stacks, queues, hash tables). They are essential gor graph algorithms and adjacency lists. 

## Efficiency of Common Operations: 
Insertion and deletion can be O(1) if the position is known; searching is O(n).

## Example Problem: 
Implement a function to reverse a linked list.

```c#
public void Reverse()
    {
        Node prev = null;
        Node current = head;
        Node next = null;
        while (current != null)
        {
            next = current.Next;
            current.Next = prev;
            prev = current;
            current = next;
        }
        head = prev;
    }

```

## Problem to Solve: 
Create a linked list to store and display in reverse order.

![alt text](<Picture Files/Linked List Problem example.png>)

```c#
using System;

public class Node
{
    public int Data;
    public Node Next;

    public Node(int data)
    {
        Data = data;
        Next = null;
    }
}

public class LinkedList
{
    // Insert code here

   
}

public class Program
{
    public static void Main()
    {
        // Insert code here
    }
}
```

## Scroll down for answer












































## Answer to the problem:
```c#
using System;

public class Node
{
    public int Data;
    public Node Next;

    public Node(int data)
    {
        Data = data;
        Next = null;
    }
}

public class LinkedList
{
    private Node head;

    public LinkedList()
    {
        head = null;
    }

    public void Add(int data)
    {
        Node newNode = new Node(data);
        if (head == null)
        {
            head = newNode;
        }
        else
        {
            Node current = head;
            while (current.Next != null)
            {
                current = current.Next;
            }
            current.Next = newNode;
        }
    }

    public void DisplayReverse(Node node)
    {
        if (node == null)
        {
            return;
        }
        DisplayReverse(node.Next);
        Console.Write(node.Data + " ");
    }

    public void DisplayReverse()
    {
        DisplayReverse(head);
    }
}

public class Program
{
    public static void Main()
    {
        LinkedList list = new LinkedList();
        list.Add(1);
        list.Add(2);
        list.Add(3);
        list.Add(4);
        list.Add(5);

        Console.WriteLine("Linked List in Reverse Order:");
        list.DisplayReverse();
    }
}
```

## Explanation:
Node Class: 
Represents a node in the linked list, containing data and a reference to the next node.

LinkedList Class: 
Manages the linked list operations.

Add(int data): 
Adds a new node with the given data to the end of the list.

DisplayReverse(Node node): 
Recursively displays the linked list in reverse order.

DisplayReverse(): 
Public method to start the reverse display from the head node.

Program Class: 
Contains the Main method to test the linked list functionality.

## Solution:
The provided code creates a linked list, adds some integers to it, and then displays the list in reverse order using recursion. When you run the program, it will output the linked list in reverse order.