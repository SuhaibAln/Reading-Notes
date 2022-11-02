# Hash Table

The number one use case for Hash Tables is storing data that needs fast lookups, insertions, and deletion. Hash tables use a { key: value } pair in order to retrieve data efficiently. The key acts as an identifier that tells our program where the value is stored in memory.
# MEMORY
Hash tables use hash functions to determine the location where information should be stored. This function takes a key as input and returns the memory address as output.
Different keys might receive the same memory address, which means the same location will store more than one value - this is known as a collision.
There are several strategies for dealing with collisions, e.g.:
• Linear probing: put the collided value in the next available memory spot (may cause clustering)
• Chaining: Use a linked list to store all items in that memory address (retrieval will be O(n) where n is the no. elements in the location)
# INSERTION, DELETION and SEARCH
• Even if some memory addresses contain a linked list with multiple items, the time complexity for search, insertion, deletion and retrieval averages to 0(1).
The key part of this data structure is the hash function.
There is no perfect solution as most of the time we don't know beforehand how much data we're storing. However, a good hash function should achieve a balanced distribution.
Hash tables should not be used for ordered data or when we plan to retrieve bulk data