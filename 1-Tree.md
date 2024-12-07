Tree
## Introduction:
Trees stand as majestic hierarchical structures, branching out into a myriad of possibilities. As we embark on this journey, we'll uncover the essence of trees, exploring their fundamental concepts and diverse applications.
Data representation characterizes a hierarchical structure in the form of a tree. Every node in a tree comprises two distinct components (Data and References). The top node of the tree is referred to as the Root node, and the two products that fall beneath it are referred to as the "Left Subtree" and the "Right Subtree."

You can now go on to the next topic to learn about the types of trees now that you have a basic knowledge of the definition of Trees in C#.


## Definition of a Tree (Hierarchical structure with nodes):
A tree is a hierarchical data structure composed of nodes connected by edges. At the pinnacle of this hierarchy lies the root node, branching out into various child nodes, forming a branching structure reminiscent of natural trees.

![alt text](<Picture Files/Tree.jpg>)

Terminology (Root, Parent, Child, Sibling):
To navigate the intricacies of trees, it's essential to grasp key terminology:

## Root: 
The topmost node of the tree, serving as the entry point for traversal.
Parent: A node that has child nodes stemming from it.
Child: Nodes directly connected to a parent node.
Sibling: Nodes that share the same parent node.
Different types of Trees (Binary Tree, Binary Search Tree)
Trees come in various forms, each tailored to specific requirements. Two notable types include:

## Binary Tree: 
A tree in which each node has at most two child nodes, commonly referred to as the left child and right child. Binary Search Tree (BST): A specialized binary tree that adheres to a specific ordering property, where the left child of a node contains values smaller than the node's value, and the right child contains values greater than the node's value. Binary Tree: In the realm of binary trees, we unravel the essence of simplicity intertwined with versatility. Basic operations serve as the cornerstone of binary tree manipulation, allowing us to navigate, manipulate, and extract information seamlessly.

## Binary Search Tree (BST):
A binary search tree (BST) is a binary tree that follows rules for data that is put into the tree. Data is placed into the BST by comparing the data with the value in the parent node. If the data being added is less than the parent node, then it is put in the left subtree. If the data being added is greater than the parent node, then it is put in the right subtree. If duplicates are allowed than the duplicate can be put either to the left or to the right of the root. By using this process, the data is stored in the tree sorted.
A shining beacon of order amidst the chaos of data, the Binary Search Tree (BST) embodies precision and efficiency. Defined by its strict ordering property, the BST facilitates rapid search, insertion, and deletion operations.
A binary search tree (BST) is a binary tree with some additional constraints. In BST, the value of the node's left child must be less than or equal to the value of its parent, while the value of the right child must be greater than or equal to the value of the parent.

## Definition and properties: 
A Binary Search Tree (BST) is a binary tree in which the value of each node follows a specific ordering property: the value of nodes in the left subtree is less than the node's value, and the value of nodes in the right subtree is greater than the node's value.

## Operations (Insertion, Deletion, Search):
Insertion: Adding a new node to the BST while maintaining the ordering property.
Time Complexity: O(log n) on average for a balanced BST, O(n) in the worst case.
Explanation: When inserting a new node into a BST, we need to find the correct position in the tree based on the value of the node. In a balanced BST, each comparison reduces the search space by approximately half, leading to a time complexity of O(log n). However, in the worst case scenario, if the BST becomes unbalanced, insertion can take O(n) time when the tree degenerates into a linked list.

## Deletion: 
Removing a node from the BST while preserving the ordering property.
Time Complexity: O(log n) on average for a balanced BST, O(n) in the worst case.
Explanation: Deletion in a BST involves finding the node to be deleted and then rearranging the tree structure while preserving the ordering property. Similar to insertion, deletion requires traversing the tree to find the node to delete, which has a time complexity of O(log n) on average in a balanced tree. However, in the worst case, deletion may take O(n) time if the tree is highly unbalanced.

## Search: 
Locating a specific value within the BST with optimal efficiency, leveraging its ordered structure.

## Time Complexity: 
O(log n) on average for a balanced BST, O(n) in the worst case.

## Explanation: 
Searching in a BST exploits its ordered structure. At each step of the search, we compare the target value with the value of the current node and choose the appropriate subtree to continue the search. In a balanced BST, this reduces the search space by approximately half at each step, leading to a time complexity of O(log n). However, in the worst case, if the tree is unbalanced, searching may take O(n) time, as it requires traversing all nodes in one branch of the tree.

## Real-world examples of BST:
Below is an example of Python code demonstrating the implementation of insertion, deletion, and search operations in a binary search tree (BST):

```
class TreeNode {
  // Property to hold the value of a node
  private _value: number;
  public get value(): number {
    return this._value;
  }
  public set value(v: number) {
    this._value = v;
  }

  // Property to hold reference to the left child node
  private _left: TreeNode;
  public get left(): TreeNode {
    return this._left;
  }
  public set left(node: TreeNode) {
    this._left = node;
  }

  // Property to hold reference to the right child node
  private _right: TreeNode;
  public get right(): TreeNode {
    return this._right;
  }
  public set right(v: TreeNode) {
    this._right = v;
  }

  // Initialize a new node
  constructor(value: number) {
    this._value = value;
    this._left = null;
    this._right = null;
  }
}
```
Answer

Back
