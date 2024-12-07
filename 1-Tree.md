## Tree
## Introduction:
Trees stand as majestic hierarchical structures, branching out into a myriad of possibilities. As we embark on this journey, we'll uncover the essence of trees, exploring their fundamental concepts and diverse applications.

## Definition of a Tree (Hierarchical structure with nodes):
A tree is a hierarchical data structure composed of nodes connected by edges. At the pinnacle of this hierarchy lies the root node, branching out into various child nodes, forming a branching structure reminiscent of natural trees.

![alt text](<Picture Files/BSTTree.jpg>)
 
## Terminology (Root, Parent, Child, Sibling):
To navigate the intricacies of trees, it's essential to grasp key terminology:

Root: The topmost node of the tree, serving as the entry point for traversal.
Parent: A node that has child nodes stemming from it.
Child: Nodes directly connected to a parent node.
Sibling: Nodes that share the same parent node.
Different types of Trees (Binary Tree, Binary Search Tree)
Trees come in various forms, each tailored to specific requirements. Two notable types include:

Binary Tree: A tree in which each node has at most two child nodes, commonly referred to as the left child and right child. Binary Search Tree (BST): A specialized binary tree that adheres to a specific ordering property, where the left child of a node contains values smaller than the node's value, and the right child contains values greater than the node's value. Binary Tree: In the realm of binary trees, we unravel the essence of simplicity intertwined with versatility. Basic operations serve as the cornerstone of binary tree manipulation, allowing us to navigate, manipulate, and extract information seamlessly.

![alt text](<Picture Files/TreesGeneral.jpg>)

## Binary Search Tree (BST):
A shining beacon of order amidst the chaos of data, the Binary Search Tree (BST) embodies precision and efficiency. Defined by its strict ordering property, the BST facilitates rapid search, insertion, and deletion operations.

Definition and properties: A Binary Search Tree (BST) is a binary tree in which the value of each node follows a specific ordering property: the value of nodes in the left subtree is less than the node's value, and the value of nodes in the right subtree is greater than the node's value.

## Operations (Insertion, Deletion, Search):
Insertion: Adding a new node to the BST while maintaining the ordering property.
Time Complexity: O(log n) on average for a balanced BST, O(n) in the worst case.
Explanation: When inserting a new node into a BST, we need to find the correct position in the tree based on the value of the node. In a balanced BST, each comparison reduces the search space by approximately half, leading to a time complexity of O(log n). However, in the worst case scenario, if the BST becomes unbalanced, insertion can take O(n) time when the tree degenerates into a linked list.
Deletion: Removing a node from the BST while preserving the ordering property.
Time Complexity: O(log n) on average for a balanced BST, O(n) in the worst case.
Explanation: Deletion in a BST involves finding the node to be deleted and then rearranging the tree structure while preserving the ordering property. Similar to insertion, deletion requires traversing the tree to find the node to delete, which has a time complexity of O(log n) on average in a balanced tree. However, in the worst case, deletion may take O(n) time if the tree is highly unbalanced.
Search: Locating a specific value within the BST with optimal efficiency, leveraging its ordered structure.
Time Complexity: O(log n) on average for a balanced BST, O(n) in the worst case.
Explanation: Searching in a BST exploits its ordered structure. At each step of the search, we compare the target value with the value of the current node and choose the appropriate subtree to continue the search. In a balanced BST, this reduces the search space by approximately half at each step, leading to a time complexity of O(log n). However, in the worst case, if the tree is unbalanced, searching may take O(n) time, as it requires traversing all nodes in one branch of the tree.

## Real-world examples of BST:
Below is an example of Python code demonstrating the implementation of insertion, deletion, and search operations in a binary search tree (BST):

## Step-by-Step Implementation
Define the Tree Node Class
The tree node class will have a value and references to its left and right children.

```
public class TreeNode
{
    public int Value { get; set; }
    public TreeNode Left { get; set; }
    public TreeNode Right { get; set; }

    public TreeNode(int value)
    {
        Value = value;
        Left = null;
        Right = null;
    }
}
```
Define the Binary Tree Class
The binary tree class will contain the root node and methods to perform various operations like insertion, traversal, etc.

```
public class BinaryTree
{
    public TreeNode Root { get; private set; }

    public BinaryTree()
    {
        Root = null;
    }

    public void Insert(int value)
    {
        Root = InsertRec(Root, value);
    }

    private TreeNode InsertRec(TreeNode root, int value)
    {
        if (root == null)
        {
            root = new TreeNode(value);
            return root;
        }

        if (value < root.Value)
        {
            root.Left = InsertRec(root.Left, value);
        }
        else if (value > root.Value)
        {
            root.Right = InsertRec(root.Right, value);
        }

        return root;
    }

    public void InOrderTraversal()
    {
        InOrderRec(Root);
    }

    private void InOrderRec(TreeNode root)
    {
        if (root != null)
        {
            InOrderRec(root.Left);
            Console.Write(root.Value + " ");
            InOrderRec(root.Right);
        }
    }

    public void PreOrderTraversal()
    {
        PreOrderRec(Root);
    }

    private void PreOrderRec(TreeNode root)
    {
        if (root != null)
        {
            Console.Write(root.Value + " ");
            PreOrderRec(root.Left);
            PreOrderRec(root.Right);
        }
    }

    public void PostOrderTraversal()
    {
        PostOrderRec(Root);
    }

    private void PostOrderRec(TreeNode root)
    {
        if (root != null)
        {
            PostOrderRec(root.Left);
            PostOrderRec(root.Right);
            Console.Write(root.Value + " ");
        }
    }

    public bool Search(int value)
    {
        return SearchRec(Root, value);
    }

    private bool SearchRec(TreeNode root, int value)
    {
        if (root == null)
        {
            return false;
        }

        if (root.Value == value)
        {
            return true;
        }

        return value < root.Value ? SearchRec(root.Left, value) : SearchRec(root.Right, value);
    }
}
```
Example Usage
Here is how you can use the BinaryTree class to create a tree, insert values, and perform traversals:

```
using System;

public class Program
{
    public static void Main()
    {
        BinaryTree tree = new BinaryTree();

        // Insert values
        tree.Insert(50);
        tree.Insert(30);
        tree.Insert(70);
        tree.Insert(20);
        tree.Insert(40);
        tree.Insert(60);
        tree.Insert(80);

        // Perform traversals
        Console.Write("In-order traversal: ");
        tree.InOrderTraversal(); // Output: 20 30 40 50 60 70 80
        Console.WriteLine();

        Console.Write("Pre-order traversal: ");
        tree.PreOrderTraversal(); // Output: 50 30 20 40 70 60 80
        Console.WriteLine();

        Console.Write("Post-order traversal: ");
        tree.PostOrderTraversal(); // Output: 20 40 30 60 80 70 50
        Console.WriteLine();

        // Search for a value
        Console.WriteLine("Search 40: " + tree.Search(40)); // Output: True
        Console.WriteLine("Search 90: " + tree.Search(90)); // Output: False
    }
}
```
Explanation
TreeNode Class:

Represents a node in the binary tree.
Contains a value and references to left and right child nodes.
BinaryTree Class:

Contains the root of the tree.
Provides methods for inserting values, performing in-order, pre-order, and post-order traversals, and searching for a value.
Program Class:

Demonstrates how to use the BinaryTree class to create a tree, insert values, perform traversals, and search for values.
This basic implementation provides a foundation for working with binary trees in C#. You can expand upon this by adding more methods such as deletion, balancing the tree, or implementing other types of trees like AVL trees or Red-Black trees.

[Answer]

[Back]
