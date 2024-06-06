# Recursive Singly Linked List in Python

This repository contains the implementation of a generic recursive singly linked list (SLL) in Python. The code includes two main classes: `SLLNode` for representing the nodes of the list, and `RecursiveSinglyLinkedList` for implementing the linked list functionality.

## Classes and Methods

### SLLNode Class

A class to represent a node in the singly linked list.

- `__init__(self, value: T, next: Node = None)`: Initializes an SLL node with a value and a reference to the next node.
- `__str__(self) -> str`: Returns a string representation of the node.
- `__repr__(self) -> str`: Returns a string representation of the node for debugging purposes.
- `__eq__(self, other: Node) -> bool`: Compares two nodes for equality.

### RecursiveSinglyLinkedList Class

A class to implement the singly linked list with various methods.

- `__init__(self) -> None`: Initializes an empty singly linked list.
- `__repr__(self) -> str`: Returns a string representation of the linked list.
- `__eq__(self, other: SLL) -> bool`: Compares two linked lists for equality.
- `insertion_sort(self) -> None`: Sorts the linked list using insertion sort.
- `add(self, value: T, back: bool = True) -> None`: Adds a node with a given value to the linked list. By default, adds to the end of the list.
- `to_string(self, curr: Node) -> str`: Converts the linked list to a string representation.
- `search(self, value: T) -> bool`: Searches for a node with a given value in the linked list.
- `remove(self, value: T) -> bool`: Removes the first node with a given value from the linked list.

## Usage

To use the linked list implementation, you can create an instance of `RecursiveSinglyLinkedList` and perform various operations such as adding, searching, removing nodes, and sorting the list.

```python
from sll import RecursiveSinglyLinkedList, SLLNode

# Create a new linked list
sll = RecursiveSinglyLinkedList()

# Add elements to the list
sll.add(3)
sll.add(1)
sll.add(2)

# Print the list
print(sll)

# Sort the list
sll.insertion_sort()
print(sll)

# Search for a value
print(sll.search(2))

# Remove a value
sll.remove(1)
print(sll)

# Remove duplicates
sll.remove_duplicates(sll.head)
print(sll)
