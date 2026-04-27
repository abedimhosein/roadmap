## Part 1: Sorting & Searching (The Basics)
1. Binary Search – The quintessential divide-and-conquer search for sorted arrays.
2. Bubble Sort – Terrible for real work, but the classic "first sort" to understand swapping.
3. Insertion Sort – Best for tiny or nearly-sorted datasets (used in Timsort).
4. Selection Sort – Simple but inefficient; good for understanding in-place algorithms.
5. Merge Sort – Stable, predictable O(n log n), foundation of external sorting.
6. Quicksort – The fastest practical in-place sort (but beware worst-case).
7. Heap Sort – In-place, O(n log n) but not stable; uses a heap data structure.
8. Counting Sort – Non-comparison integer sort (linear time!).
9. Radix Sort – Sorts by digit/character position; great for fixed-length keys.
10. Timsort – Python's default sort; hybrid of merge & insertion.
---
## Part 2: Data Structure Algorithms
11. Array Rotation / Reversal – Classic two-pointer trick.
12. Two-Pointer Technique – For pairs, triplets, or palindrome checking.
13. Sliding Window – For substring or subarray statistics (O(n) instead of O(n²)).
14. Fast & Slow Pointer (Cycle Detection) – Floyd’s algorithm for linked lists.
15. Union-Find (Disjoint Set) – For connected components, Kruskal’s, and dynamic connectivity.
16. Binary Heap Operations – heapify, push, pop, decrease-key.
17. LRU Cache Algorithm – Usually implemented with a hash map + doubly linked list.
18. Reservoir Sampling – Randomly select k items from a stream of unknown length.
19. Bloom Filter – Probabilistic set membership (space-efficient, false-positive possible).
---
## Part 3: Graph Algorithms
20. Breadth-First Search (BFS) – Shortest path in unweighted graphs, web crawling.
21. Depth-First Search (DFS) – Topological sorting, cycle detection, maze generation.
22. Dijkstra’s Algorithm – Single-source shortest path (non-negative weights).
23. Bellman-Ford – Handles negative weights; detects negative cycles.
24. Floyd-Warshall – All-pairs shortest paths (dense graphs).
25. A* Search – Graph search with heuristics (pathfinding in games/GPS).
26. Topological Sort – Task scheduling, dependency resolution.
27. Kruskal’s Algorithm – Minimum spanning tree (uses union-find).
28. Prim’s Algorithm – Minimum spanning tree (uses a priority queue).
29. Tarjan’s SCC (Strongly Connected Components) – Finds cycles in directed graphs.
30. Kosaraju’s SCC – Another approach to SCCs (two-pass DFS).
---
## Part 4: Dynamic Programming (Optimization)
31. Fibonacci with Memoization – The canonical DP example.
32. Knapsack Problem (0/1 & Unbounded) – Resource allocation, subset sum.
33. Longest Common Subsequence (LCS) – Diff tools, version control.
34. Longest Increasing Subsequence (LIS) – Useful in routing and data analysis.
35. Edit Distance (Levenshtein) – Spell checkers, DNA sequence alignment.
36. Rod Cutting / Coin Change – Classic unbounded knapsack relatives.
37. Matrix Chain Multiplication – Optimizes order of operations (parenthesization).
38. Maximum Subarray (Kadane’s Algorithm) – O(n) solution for largest sum.
39. House Robber / Stock Trading – State-machine DP problems.
40. Staircase Climbing (Ways to reach step n) – Combines DP & combinatorics.
---
## Part 5: Hashing, Strings & Cryptography
41. Rolling Hash (Rabin-Karp) – String search in O(n) average time.
42. Knuth-Morris-Pratt (KMP) – Linear-time substring search using prefix function.
43. Z-Algorithm – Another linear-time pattern matching.
44. Trie (Prefix Tree) – Autocomplete, IP routing, word games.
45. Aho-Corasick – Multiple pattern matching (virus scanners, spam filters).
46. Consistent Hashing – For distributed caches & databases (avoid rehashing all keys).
47. SHA Family & MD5 (understanding, not using) – Cryptographic hash basics.
48. RSA (concept & modular exponentiation) – Public-key cryptography.
49. Base64 Encoding – Binary-to-text encoding for emails, JSON, etc.
50. Levenshtein Automaton – Fast fuzzy string matching (beyond simple DP).
