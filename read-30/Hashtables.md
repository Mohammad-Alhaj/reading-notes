# Hashtables

## What is a Hashtable?
Terminology:

Hash - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.
Buckets - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.
Collisions - A collision is what happens when more than one key gets hashed to the same location of the hashtable.
Why do we use them?
Hold unique values
Dictionary
Library
What Are they
Hashtables are a data structure that utilize key value pairs. This means every Node or Bucket has both a key, and a value.

The basic idea of a hashtable is the ability to store the key into this data structure, and quickly retrieve the value. This is done through what we call a hash. A hash is the ability to encode the key that will eventually map to a specific location in the data structure that we can look at directly to retrieve the value.


## Insertion and Deletion
Best Case
The hash key is calculated in O(1) time complexity as always, and the required location is accessed in O(1).
Insertion: In the best case, the key indicates a vacant location and the element is directly inserted into the hash table. So, overall complexity is O(1).
Deletion: In the best case, the element to be deleted is found at the key index itself and is directly deleted. This is achieved in constant O(1) complexity.

## Average Case
The hash key is calculated in O(1) time complexity and the required location is accessed in O(1).
Insertion: Like we saw in searching earlier, in the average case,all chains are of equal length and so, the last node of the chain is reached in constant time complexity. Here, the new node is created and appended to the list. Overall time complexity is O(1).
Deletion: The node to be deleted can be reached in constant time in the average case, as all the chains are of roughly equal length. Deletion takes place in O(1) complexity.

## Worst Case
In the worst cases, both insertion and deletion take O(n) complexity. This is because all nodes are attached to the same linked list due to collision.
Insertion: The entire list of n elements must be traversed to reach the end and then, the new node is appended.
Deletion: The entire list is searched and in the worst case, the element to be deleted is found at the very last node in the last.


## Space complexity
In all cases of open addressing, space complexity for hash map remains O(n) where