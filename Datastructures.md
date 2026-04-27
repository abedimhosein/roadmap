## Part 1: The Absolute Essentials (The "CS 101" Tier)
`If you only learn 10, learn these.`

1. Array (Static) – Contiguous memory, O(1) random access.
2. Dynamic Array (ArrayList / Vector) – Resizable array with amortized O(1) appends.
3. Singly Linked List – Sequential access, O(1) insert/delete at head.
4. Doubly Linked List – Allows traversal backwards (used in LRU caches).
5. Stack (LIFO) – Function calls, undo systems, DFS.
6. Queue (FIFO) – Task scheduling, BFS, message passing.
7. Hash Map (Dictionary) – O(1) average lookups/inserts. The workhorse of software.
8. Hash Set – Uniqueness testing without storing values.
9. Binary Tree – Root, left, right. Foundation for BSTs and heaps.
10. Binary Search Tree (BST) – In-order traversal gives sorted order.
---

## Part 2: Advanced Trees & Hierarchies
`For databases, compilers, and file systems.`

11. AVL Tree – Self-balancing BST (height difference ≤ 1). Strict balance.
12. Red-Black Tree – Self-balancing BST (looser rules). Used in C++ std::map and Java TreeMap.
13. Segment Tree – Answers range queries (sum/min/max) and updates in O(log n).
14. Fenwick Tree (Binary Indexed Tree) – Simpler than segment tree; does prefix sums & point updates.
15. Binary Heap – Complete binary tree for priority queues (fastest extract-min).
16. Binomial Heap – Supports efficient merge operations.
17. Fibonacci Heap – Very fast decrease-key; used in advanced Dijkstra implementations.
18. Treap (Tree + Heap) – Randomized BST with heap priorities; simpler to code than AVL.
19. Splay Tree – Recently accessed elements move to root (cache-friendly).
20. B-Tree – Balanced tree with many children per node. The backbone of SQL databases.
21. B+ Tree – B-Tree variant; all data in leaves (used by MySQL/PostgreSQL indexes).
22. Trie (Prefix Tree) – Stores strings by prefix. Autocomplete, IP routing.
23. Radix Tree (Patricia Trie) – Space-optimized Trie (compresses single-child nodes).
24. Suffix Tree – Contains every suffix of a string. Used for DNA sequencing & plagiarism detection.
25. Suffix Array – More space-efficient alternative to a suffix tree.
---

## Part 3: Graphs (Connected Data)
`Networks, social media, and maps.`

26. Adjacency Matrix – O(1) edge lookup, O(V²) space. Good for dense graphs.
27. Adjacency List – O(1) vertex iteration, O(V+E) space. Standard for most graphs.
28. Edge List – Simple array of (u,v) pairs. Used in Kruskal's algorithm.
29. Directed Graph – Edges have direction (Twitter follows).
30. Undirected Graph – Edges are bidirectional (Facebook friends).
31. Weighted Graph – Edges have costs/distances (maps).
32. DAG (Directed Acyclic Graph) – No cycles. Used for scheduling & version control (Git).
---

## Part 4: Specialized & Probabilistic
`For caching, networking, and large-scale systems.`

33. Bloom Filter – Probabilistic membership test (false positives, no false negatives). Used by Cassandra & HBase.
34. Count-Min Sketch – Frequency estimation of events in a data stream (heavy hitters).
35. HyperLogLog – Approximate cardinality (count distinct values) using very little memory.
36. Cuckoo Hash Table – Guarantees O(1) worst-case lookup (uses two hash functions).
37. Robin Hood Hash Table – Reduces variance in probe lengths.
38. Consistent Hash Ring – Minimizes rehashing when servers are added/removed. Used by Dynamo, Redis Cluster.
39. Rendezvous (HRW) Hashing – Alternative to consistent hashing; lower memory overhead.
---

## Part 5: Disjoint Sets & Unions
`For clustering and connectivity.`

40. Disjoint Set (Union-Find) – Tracks partitions of a set. Critical for Kruskal's MST and image segmentation.
---
## Part 6: Caches & Memory Management
`Speed vs. space tradeoffs.`

41. LRU Cache (Least Recently Used) – Evicts oldest used item. Implemented with HashMap + Doubly Linked List.
42. LFU Cache (Least Frequently Used) – Evicts least popular item (more complex than LRU).
43. ARC (Adaptive Replacement Cache) – Self-tuning cache (ZFS file system).
---
## Part 7: Spatial & Geometric
`For games, GIS, and robotics.`

44. Quadtree – 2D spatial subdivision (game collision detection).
45. Octree – 3D spatial subdivision (3D rendering).
46. K-d Tree (K-Dimensional Tree) – Organizes points in K-dimensional space (nearest neighbor search).
47. R-Tree – For bounding boxes & geospatial queries (PostGIS, GIS databases).
48. Interval Tree – Finds all intervals that overlap with a given point or interval.
---

## Part 8: Strings & Text
49. Rope – Binary tree where leaves are strings. Efficient insert/delete in text editors.`
50. String Builder (Rope variant) – Amortized efficient string concatenation (avoiding Schlemiel the Painter).----

