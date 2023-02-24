# Serializable-Tree
A generic tree structure that can be displayed in the Unity Inspector, with a position pointer to the Current Node.

- install

Download the souce code and extract it to your project.

- Create Tree

An initial Value must always be given for the Root Node of the given Tree
``` C#
Tree<T> newTree = new Tree<T>(rootValue);
```
- Add Nodes

Adding Nodes to a Tree requies the new value and the index for an int[] of the child/leaf to add it to (which can be accessed directly from a selected Node)
```C#
newTree.Add(child, node.index);
```
- Cursor/Pointer
# Serializable-Tree

A generic tree structure that can be displayed in the Unity Inspector, with a position pointer to the Current Node.
- install

Download the souce code and extract it to your project.
- Create Tree

An initial Value must always be given for the Root Node of the given Tree
``` C#
Tree<T> newTree = new Tree<T>(rootValue);
```
- Add Nodes

Adding Nodes to a Tree requies the new value and the index for an int[] of the child/leaf to add it to (which can be accessed directly from a selected Node)
```C#
newTree.Add(child, node.index);
```
- Cursor Position

You can use the Cursor to Step Back or Forward through the Tree's Hierarchy.
```C#
newTree.StepForward(int indexOnCurrentLayer); //Go to the the node at the given Index on the current Layer.
newTree.StepForward(T nodeWithValue); //Go to the Node with the given Value on the current Layer.
newTree.StepForward(string nodeWithValueToSting); //Go to the Node the given Value when converted to a string.
newTree.StepBackward(); //Step back to the parent node.
```

- Access the Current Node

Lastly, you can get the value of the Current Node using...
```C#
newTree.CurrentNode.value;
```
