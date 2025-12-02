# Intrduction

The Multiset I am going to design is a player inventory that stores the string item names and their count value (if the all the item appear multiple times there count will increse by 1) and I will implementing this using the HashTable. Each unique will be the key and the value will count the number of times that key appears. This structure would be fast for inserting, removing and even for looking up the items.

Example: "potion": 3

potion is the key and 3 is the value/count i.e the number of potions he have in the inventory. Adding 1 more potions will increse the value to 4 and so on.

# Design Philosophy

Efficiency: The operations such as adding or removing items will occur in O(1) time complexity because of the hash table structure.

Simplicity: This focuses on the game-relevant operations (add, remove, count, contains).

Extensibility: 

Redability: Clear method semantics, consistent handling of edge cases and well-defined invariants ensure that developers or other game-system modules can safely interact with the MultiSet.

Clients and Users:

Client: Game module such as inventory management of games.

User: Players those are playing the game and interact with inventories through the game mechanics.

# Core Operations

* Add(item, count)
  Concept: Adds count copies of item to the player inventory.
  Average Time Complexity: O(1)
  Edge Cases: Adding items more than available space will handle the error.
  HashTable support: Key lookup ,inseration or remove using pseudo-random probing that ensures the fast access. 

* Remove(item, count)
  Concept: Removes the count by 1 everytime if remove occures and if reaches 0 removes the Key.
  Average Time Complexity: O(1)
  Edge Cases: Removing the non-existent item returns 0 and also removal of more than present items in the Multiset counts to 0.
  HashTable Support: Efficient lookup and update, with slot marked empty upon deletion.

* Count(item)
  Concept: Returns the count of individual item in the inventory.
  Average Time Complexity: O(1)
  Edge Cases: False for missing keys/item.

* totalCount()
  Concept: Returns the total number of items in the inventoy by summing up all the counts of every item.
  Time Complexity: O(1) 
  Edge Case: At the starting totalCount would be 0.

* distinctSize()
  Concept: Counts up all the unique items in the inventory.
  Time Complexity: O(1)
  Edge Case: At the starting totalCount would be 0.



