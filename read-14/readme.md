# Trees

## Terminology

**Node** - A Tree node is a component which may contain its own values, and references to other nodes

**Root**t - The root is the node at the beginning of the tree

**Left** - A reference to one child node, in a binary tree

**Right** - A reference to the other child node, in a binary tree

**Edge** - The edge in a tree is the link between a parent and child node

**Leaf**- A leaf is a node that does not have any children

**eight** - The height of a tree is the number of edges from the root to the furthest leaf

---

## Traversals

Traversing a tree allows us to search for a node, print out the contents of a tree, and much more! There are two categories of traversals when it comes to trees:


1.**Depth First**

2.**Breadth First**

***

### **Depth First**

**Pre-order:** root **>>** left **>>** right

**In-order:** left **>>** root **>>** right

**Post-order:** left **>>** right **>>** root

 
### **Breadth First**

Breadth first traversal iterates through the tree by going through each level of the tree node-by-node.

## K-ary Trees

If Nodes are able have more than 2 child nodes, we call the tree that contains them a K-ary Tree. In this type of tree we use K to refer to the maximum number of children that each Node is able to have.

## Big O

The Big O time complexity of a Binary Search Tree’s insertion and search operations is O(h), or O(height). In the worst case, we will have to search all the way down to a leaf, which will require searching through as many nodes as the tree is tall. In a balanced (or “perfect”) tree, the height of the tree is log(n). In an unbalanced tree, the worst case height of the tree is n.

The Big O space complexity of a BST search would be O(1). During a search, we are not allocating any additional space.