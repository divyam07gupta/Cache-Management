Splay Tree Cache Management
This project implements a cache management system using Splay Trees, enabling efficient retrieval, insertion, and eviction of key-value pairs based on the Least Recently Used (LRU) policy.

Features:

Fixed Capacity Cache: Manages a cache with a set capacity.
Efficient Retrieval: Quickly retrieves values based on keys.
Insertion: Adds new key-value pairs.
Eviction: Removes the least recently used entry when the cache is full.
Single and Multithreaded Implementation: Supports both environments.

Issues with Initial Single-Threaded Implementation:

Concurrency Conflicts: Concurrent splaying operations by multiple threads can lead to inconsistent tree structures or incorrect results.
Balancing Trade-off: Frequent reorganization is needed for optimal performance, but excessive reorganization in a multi-threaded environment can negatively impact performance due to synchronization.
Contention: Frequent modifications by multiple threads can lead to contention for access to critical nodes, causing slowdowns.

Key Terms:

Cache Block: The basic unit for cache storage, containing multiple bytes/words of data.
Cache Line: Same as a cache block, not to be confused with a “row” of cache.
Cache Set: A “row” in the cache, with the number of blocks per set determined by the cache layout.
Tag: A unique identifier for a group of data, used to differentiate between different memory regions mapped into a block.

Dependencies

C++ compiler supporting C++11 or higher
Standard Template Library (STL)
ctime library for timestamp management
thread, mutex, chrono, and condition_variable libraries for handling multithreaded environments

Getting Started:

Clone the repository or download the source code files.
Compile the source code using a C++ compiler.
Run the compiled executable.

Usage

The program provides a command-line interface for interacting with the cache, supporting the following operations:
Add an Entry: Add a new key-value pair to the cache.
Retrieve an Entry: Retrieve the value associated with a given key.
Remove an Entry: Remove a key-value pair from the cache.
Print Cache Contents: Display the current contents of the cache.
Exit: Terminate the program.
