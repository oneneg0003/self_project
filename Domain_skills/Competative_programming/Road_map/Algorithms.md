# 🧠 ALGORITHMS MASTER LIST — PART 1 / MANY
# Core + Searching + Sorting + Selection + Basic Enumeration + Scanning
# (Algorithms + common variations; research-leaning included where standard)

====================================================================
A. SEARCH / DECISION / QUERY ALGORITHMS
====================================================================

- Linear Search
  - Sentinel Linear Search
  - Linear Search with Early Exit
  - Linear Search on Linked List
  - Linear Search on Unsorted Array
  - Linear Search with Predicate

- Binary Search (on sorted domain or monotone predicate)
  - Classic Binary Search (find key)
  - Lower Bound (first >= x)
  - Upper Bound (first > x)
  - First True (monotone predicate)
  - Last True (monotone predicate)
  - Binary Search on Answer (decision → optimization)
  - Binary Search on Real Numbers (epsilon termination)
  - Binary Search on Integers (lo/hi convergence)
  - Binary Search with Invariants (lo feasible / hi infeasible)
  - Parallel Binary Search (offline multiple queries)
  - Fractional Cascading + Binary Search (advanced query accel)
  - Binary Search in Rotated Sorted Array
  - Binary Search in Bitonic Array
  - Binary Search with Duplicates (first/last occurrence)
  - Exponential + Binary (unbounded search)

- Ternary Search (unimodal)
  - Integer Ternary Search (discrete unimodal)
  - Continuous Ternary Search (real-valued)
  - Golden Section Search (continuous alternative)
  - Hill Climbing on Discrete Unimodal (neighbor compare)

- Exponential Search
  - Doubling Range then Binary Search
  - Galloping Search (merge optimization)

- Fibonacci Search
- Interpolation Search (uniformly distributed keys)
- Jump Search (block jumping)
- Uniform Binary Search (variant)

- Parametric Search (advanced)
  - Megiddo Parametric Search (theory)
  - Aliens Trick (Lagrangian parametric DP) (CP-advanced)
  - Parametric Maxflow/Min-cut (advanced)

- Order Statistics / Selection Queries (algorithmic)
  - Selection by Sorting (baseline)
  - Quickselect
    - Randomized Quickselect
    - 3-way partition Quickselect
  - Median of Medians (BFPRT deterministic selection)
  - Introselect (hybrid)
  - nth_element (library concept)
  - Online Median Maintenance (heap-based algorithmic pattern)

====================================================================
B. ENUMERATION / GENERATION ALGORITHMS
====================================================================

- Subset Enumeration
  - Enumerate all subsets (0..(2^n-1))
  - Enumerate subsets by size (k-combinations)
  - Enumerate subsets in Gray Code order
  - Enumerate subsets via recursion/backtracking
  - Enumerate subsets with pruning (constraint propagation)

- Submask Enumeration (bitmask tricks)
  - Enumerate all submasks of mask
  - Enumerate all supermasks of mask (via complements)
  - Enumerate submasks in descending order (sub = (sub-1)&mask)
  - SOS-style supermask loops (algorithmic pattern)

- Permutation Generation
  - Next Permutation (lexicographic)
  - Prev Permutation
  - Heap’s Algorithm (permutation generation)
  - Steinhaus–Johnson–Trotter (adjacent swaps)
  - Factoradic / Lehmer code unranking
  - Ranking/unranking permutations

- Combination Generation
  - Gosper’s Hack (k-set bitmasks)
  - Lexicographic combination generation
  - Recursive k-combination generation
  - Combinatorial number system unranking

- Partition Generation
  - Integer partitions generation
  - Set partitions generation (advanced)
  - Restricted partitions generation (bounded parts)

- Gray Code Generation
  - Binary-reflected Gray code
  - k-ary Gray codes (advanced)

- Cartesian Product Enumeration
  - Mixed radix enumeration
  - DFS over product space
  - BFS over product space (rare)

- Meet-in-the-Middle Enumeration
  - Split array into halves; enumerate sums
  - Sort-and-two-pointer merge of partial results
  - Hash partial sums for membership
  - Enumerate XOR sums (bitwise MITM)
  - Enumerate subset products (log transform sometimes)

====================================================================
C. SCANNING / TWO-POINTER / WINDOW ALGORITHMS
====================================================================

- Two Pointers
  - Opposite-direction (l++, r--)
  - Same-direction (slow/fast)
  - Fix-one + move-other
  - Two pointers on sorted arrays (two-sum)
  - Two pointers on merged arrays
  - Two pointers with counting duplicates
  - Two pointers with invariant maintenance

- Sliding Window
  - Fixed-size window scan
  - Variable-size window (expand/shrink)
  - Sliding window with frequency table
  - Sliding window with hash map
  - Sliding window with monotonic queue (min/max)
  - Sliding window for distinct count
  - Sliding window for at-most / exactly-K technique
  - Sliding window for minimal subarray meeting constraint
  - Sliding window for maximal subarray meeting constraint

- Sweep Line (1D/2D event scanning)
  - Sort events by coordinate
  - Process add/remove events
  - Maintain active set (ordered structure)
  - Difference-array sweep (offline prefix accumulation)
  - Line sweep with coordinate compression
  - Offline interval stabbing queries (events + BIT/segment tree)
  - Rectangle union area sweep (advanced geometry crossover)
  - Closest pair sweep (balanced tree) (advanced)

====================================================================
D. SORTING ALGORITHMS (WITH VARIATIONS)
====================================================================

- Bubble Sort
  - Optimized Bubble (early stop)
- Selection Sort
- Insertion Sort
  - Binary Insertion Sort
- Shell Sort
  - Shell gap sequences variants
- Merge Sort
  - Top-down Merge Sort
  - Bottom-up Merge Sort
  - Natural Merge Sort
  - Merge Sort with Inversion Counting
  - External Merge Sort (disk-based)
- Quick Sort
  - Randomized Quick Sort
  - 3-way Quick Sort (Dutch partition)
  - Dual-pivot Quick Sort (library)
  - Quick Sort with tail recursion elimination
- Heap Sort
- Counting Sort
  - Stable Counting Sort
- Radix Sort
  - LSD Radix Sort
  - MSD Radix Sort
  - Radix sort on strings
- Bucket Sort
- Tree Sort (BST-based)
- TimSort (library hybrid)
- IntroSort (Quick + Heap + Insert)
- Patience Sorting (LIS-related)
- Bitonic Sort (parallel / theory)
- Odd-even Sort (parallel)
- Pancake Sort (novelty)
- BogoSort (joke / baseline)
- Smoothsort (advanced heap variant)

====================================================================
E. PARTITIONING / SELECTION / MEDIANS
====================================================================

- Partition (array)
  - Lomuto partition scheme
  - Hoare partition scheme
  - Dutch National Flag partition (3-way)
- Selection
  - Quickselect
  - BFPRT (Median of Medians)
  - Median-of-three pivot selection
  - Tukey ninther pivot selection (advanced)
- Medians
  - Streaming median via two heaps
  - Median in sorted arrays (two-array median) method
  - Weighted median (advanced)

====================================================================
F. BASIC NUMERICAL / BIT ALGORITHMS
====================================================================

- Euclidean Algorithm (GCD)
  - Binary GCD (Stein’s algorithm)
- Extended Euclidean Algorithm
- LCM via GCD
- Fast Exponentiation
  - Binary exponentiation (pow)
  - Modular exponentiation
  - Fast doubling method (Fibonacci)
- Modular Arithmetic Utilities (algorithmic)
  - Modular inverse via extended Euclid
  - Modular inverse via Fermat (prime mod)
  - Modular division via inverse
- Bit Manipulation Algorithms
  - Popcount (Hamming weight)
  - Bit length (MSB position)
  - Lowbit extraction (x & -x)
  - Enumerate set bits loop
  - Submask iteration loop
  - Gray code transform (x ^ (x>>1))
  - Bit reversal (bit tricks)
  - Fast parity computation (xor fold)
  - SWAR bit hacks (advanced)
- Randomization Utilities (algorithmic)
  - Fisher–Yates Shuffle
  - Reservoir Sampling (stream sampling)
  - Rejection Sampling (basic)
  - Alias Method (discrete sampling) (advanced)

====================================================================
G. BASIC GRAPH ALGORITHMS (TRAVERSAL / BUILDING BLOCKS)
====================================================================

- DFS
  - Recursive DFS
  - Iterative DFS (explicit stack)
  - DFS preorder/postorder timestamps
  - DFS tree classification (tree/back/cross edges)
  - DFS on implicit graph (state transitions)
- BFS
  - Standard BFS
  - Multi-source BFS
  - BFS on grid (4-neighbor / 8-neighbor)
  - BFS with parent reconstruction
  - BFS with level arrays
  - 0-1 BFS (deque-based)
  - BFS on implicit state graph
- Topological Sorting (DAG)
  - Kahn’s algorithm (indegree queue)
  - DFS finish-order topo
- Connected Components
  - BFS-based components
  - DFS-based components
- Bipartite Check
  - BFS 2-coloring
  - DFS 2-coloring

====================================================================
H. BASIC SET / MAP / FREQUENCY ALGORITHMS
====================================================================

- Frequency counting (hash map)
- Sorting + frequency compression (run-length encoding)
- Coordinate compression
  - Sort unique mapping
  - Compression with stable indexing
- Deduplication
  - Sort + unique
  - Hash-set filtering
- Two-sum / three-sum patterns (algorithmic)
  - Hash-based two-sum
  - Sort + two-pointer two-sum
  - Fix-one + two-pointer three-sum
  - k-sum recursion (advanced)
- Prefix sums
  - 1D prefix sum
  - 2D prefix sum (integral image)
- Difference arrays
  - 1D difference array
  - 2D difference array (imos method)

====================================================================
I. BASIC STRING / SEQUENCE ALGORITHMS (FOUNDATIONAL)
====================================================================

- Naive substring search
- Prefix function computation (KMP table) (as algorithmic primitive)
- Z-function computation (as algorithmic primitive)
- Rolling hash prefix computation
- Palindrome check by two pointers
- Run-length encoding (RLE)
- Longest common prefix by scanning
- Edit distance (basic DP algorithm) (listed deeper later)
- Minimal rotation (Booth) (advanced but common in CP)

====================================================================
J. BASIC COMPUTATIONAL GEOMETRY (FOUNDATIONAL PRIMITIVES)
====================================================================

- Orientation test (ccw) using cross product
- Dot product distance comparison
- Segment intersection (orientation-based)
- Line intersection (analytic)
- Polygon area (shoelace)
- Point-in-rectangle / bounding box tests
- Point-in-polygon (ray casting)
- Angle sorting (atan2-based) (careful)
- Distance computations
  - Euclidean distance
  - Squared distance optimization
- Convex hull (named algorithms are later; primitives here)

====================================================================
K. BASIC PROBABILITY / RANDOMIZED ALGORITHMS (FOUNDATIONAL)
====================================================================

- Monte Carlo estimation (sampling)
- Randomized pivot selection (QuickSort/Quickselect)
- Random hashing (probabilistic collision avoidance)
- Las Vegas retry-until-success pattern
- Random walk simulation (basic)

====================================================================
L. BASIC COMBINATORIAL GENERATION (FOUNDATIONAL)
====================================================================

- Factorial precompute
- nCr via factorial/inverse factorial (mod) (method + algorithmic routine)
- Pascal triangle DP for binomial coefficients
- Catalan numbers via DP
- Stirling numbers via DP (rare)
- Inclusion–exclusion subset loop (structure; full later)

# End of Part 1
# Next parts will expand: full graph (SCC/bridges/MST/shortest paths/flows/matching),
# DP full (optimizations), strings full (suffix/automata), number theory full (MR/PR/NTT),
# geometry full (hulls/sweep/HPI), combinatorics full (GF/Polya), linear algebra full, etc.




# 🧠 ALGORITHMS MASTER LIST — PART 2 / MANY
# Graph Algorithms (Core → ICPC → Advanced → Research-Leaning)
# (Algorithms + common variations)

====================================================================
A. GRAPH CONNECTIVITY / COMPONENTS / DECOMPOSITION
====================================================================

- Connected Components (CC)
  - CC via DFS
  - CC via BFS
  - CC via DSU (offline edge additions)

- Disjoint Set Union (DSU) Algorithms
  - DSU Union-by-rank + Path compression
  - DSU Union-by-size + Path compression
  - DSU for offline connectivity queries
  - DSU for Kruskal MST
  - Rollback DSU (persistent-like)
  - DSU with time-travel via divide-and-conquer on time (offline dynamic connectivity)
  - DSU on Tree (a.k.a. Sack / small-to-large) (tree aggregation algorithm)

- Strongly Connected Components (SCC)
  - Kosaraju algorithm (2-pass DFS)
  - Tarjan SCC (lowlink stack)
  - Gabow SCC (stack-based)
  - Condensation DAG construction (SCC graph)
  - SCC + DP on condensation (common ICPC pattern)

- Bridges / Articulation / Biconnected
  - Bridges in undirected graph (Tarjan lowlink)
  - Articulation points (Tarjan)
  - Edge-biconnected components
  - Vertex-biconnected components
  - Block-cut tree construction
  - Bridge tree construction (2-edge-connected contraction)

- Topological Structure
  - Topological sort (Kahn)
  - Topological sort (DFS postorder)
  - Detect cycle in directed graph (DFS colors)
  - Detect cycle in undirected graph (parent check)
  - Condensation DAG topological ordering

- Bipartite / Coloring Basics
  - Bipartite check (BFS/DFS 2-color)
  - Odd cycle detection via BFS levels
  - Greedy coloring (heuristic)
  - 2-coloring on components (multi-component)

- Planarity / Special Decompositions (advanced / rare)
  - SPQR tree decomposition (biconnected planar structure)
  - Block decomposition (already above)
  - Ear decomposition (rare)
  - Planar dual construction (rare / geometry crossover)

====================================================================
B. GRAPH TRAVERSAL & PATH ALGORITHMS
====================================================================

- BFS Family
  - BFS shortest path (unweighted)
  - Multi-source BFS
  - BFS with parent reconstruction
  - BFS on grid (4-neighbor, 8-neighbor)
  - BFS on state space (implicit graph)
  - BFS for minimum edges with constraints (layered BFS)
  - 0–1 BFS (deque)
  - BFS on complement graph (advanced trick)
  - BFS in DAG by topological order (special case)

- DFS Family
  - DFS reachability
  - DFS tree edge classification
  - DFS for cycle detection
  - DFS for topological sort
  - DFS for subtree sizes / tin-tout (tree algorithms foundation)

- Shortest Paths (Single-Source)
  - Dijkstra (nonnegative weights)
    - Dijkstra with binary heap
    - Dijkstra with pairing heap (advanced)
    - Dijkstra with Fibonacci heap (theoretical)
  - Dial’s algorithm (small integer weights)
  - 0–k BFS (small bounded weights) (generalization)
  - Bellman–Ford (handles negative weights)
  - SPFA (queue relaxation; worst-case bad)
  - DAG shortest paths (topological DP)
  - Johnson reweighting (for APSP with negative edges but no negative cycles)
  - Difference constraints shortest path (Bellman-Ford modeling)
  - A* (admissible heuristic) (rare in ICPC)
  - Bidirectional Dijkstra (rare; specialized)

- Shortest Paths (All-Pairs)
  - Floyd–Warshall (O(n^3))
  - Johnson APSP (sparse)
  - Repeated Dijkstra (n times) (sparse)
  - Min-plus matrix multiplication APSP (theoretical)

- Special Path Problems
  - k-shortest paths (Yen’s algorithm) (rare)
  - Edge-disjoint shortest paths (Suurballe) (rare)
  - Longest path in DAG (topological DP)
  - Longest path in tree (diameter)
  - Second shortest path (state-augmented Dijkstra)

====================================================================
C. MINIMUM SPANNING STRUCTURES
====================================================================

- Minimum Spanning Tree (MST)
  - Kruskal algorithm
  - Prim algorithm
  - Borůvka algorithm
  - Reverse-delete MST (rare)
  - MST on geometric graphs (Delaunay trick) (advanced / rare)

- Variants / Extensions
  - Minimum Spanning Forest (disconnected graphs)
  - Second-best MST (exchange edges; LCA max-edge queries)
  - Dynamic MST (advanced / research; rarely needed)

====================================================================
D. TREE ALGORITHMS (CORE → ADVANCED)
====================================================================

- Rooting / Traversals
  - Root a tree at r (parent/depth)
  - Euler tour (tin/tout)
  - Subtree size computation
  - Heavy child computation

- LCA (Lowest Common Ancestor)
  - Binary lifting LCA
  - Euler tour + RMQ LCA (Sparse table)
  - Tarjan offline LCA (DSU + DFS) (rare)
  - LCA with parent pointers (naive)

- Path / Distance Queries
  - Distance via depths + LCA
  - K-th ancestor via binary lifting
  - Jump pointers for ancestor queries

- Tree Diameter / Centers
  - Diameter via 2 BFS / 2 DFS
  - Tree center extraction
  - Tree centroid extraction

- Heavy-Light Decomposition (HLD) Algorithms
  - Path queries via HLD + segment tree
  - Subtree queries via Euler tour flattening
  - HLD for path updates/range queries

- Centroid Decomposition Algorithms
  - Centroid decomposition build
  - Distance queries using centroid tree
  - Update/query on marked nodes via centroid tree

- DSU on Tree (Small-to-large) Algorithms
  - “Keep heavy” subtree aggregation
  - Frequency counting in subtree
  - Answer queries per subtree offline

- Rerooting Algorithms
  - Rerooting DP (all roots answers)
  - Rerooting with prefix/suffix child contributions

- Virtual Tree Algorithms
  - Build virtual tree from subset of nodes + LCA
  - Solve DP on virtual tree (subset queries)

- Advanced Dynamic Trees (rare / research)
  - Link-cut tree operations (dynamic trees)
  - Euler tour tree dynamic connectivity (advanced)
  - Top tree (advanced)

====================================================================
E. FLOW / CUT ALGORITHMS
====================================================================

- Max Flow
  - Ford–Fulkerson (DFS augment)
  - Edmonds–Karp (BFS augment)
  - Dinic (level graph + blocking flow)
  - Push–Relabel (preflow)
    - Highest-label push–relabel
    - Relabel-to-front
    - Gap heuristic (optimization)
    - Global relabel heuristic

- Min Cut
  - s-t min cut from max flow residual
  - Global min cut (Stoer–Wagner)

- Flow Modeling Tricks (algorithmic routines)
  - Node-splitting (vertex capacities)
  - Edge lower bounds → circulation transform
  - Super source/sink construction
  - Multiple sources/sinks consolidation
  - Capacity scaling (advanced)

- Min-Cost Flow
  - Successive shortest augmenting path (SSAP)
  - SPFA-based potentials (careful)
  - Dijkstra with potentials (Johnson) (standard)
  - Cycle canceling (rare)
  - Min-cost max-flow (MCMF)

- Circulation
  - Circulation with demands (lower/upper bounds)
  - Feasibility check with super source/sink
  - Recover flow assignment from feasible circulation

- Advanced / Rare Flow Algorithms
  - Gomory–Hu tree (all-pairs min cut)
  - Parametric maxflow (advanced)
  - Min-cut in planar graphs via dual (advanced / rare)

====================================================================
F. MATCHING ALGORITHMS
====================================================================

- Bipartite Matching
  - Kuhn algorithm (DFS augment)
  - Hopcroft–Karp (BFS layers + DFS)
  - Weighted bipartite matching
    - Hungarian algorithm (assignment)

- General Graph Matching
  - Blossom algorithm (Edmonds) (general matching)
  - Gabow implementation variants (advanced)

- Derived Problems via Matching (algorithmic reductions)
  - Min vertex cover in bipartite (via max matching)
  - Max independent set in bipartite (via min vertex cover)
  - Min path cover in DAG (via bipartite matching)
  - Dilworth decomposition (posets → matching) (advanced)

====================================================================
G. CUTS / CONNECTIVITY ADVANCED
====================================================================

- Global Min Cut
  - Stoer–Wagner algorithm

- All-Pairs Min Cut (advanced)
  - Gomory–Hu tree construction

- Edge Connectivity / Vertex Connectivity (advanced)
  - K-edge-connected decomposition (conceptual; rarely implemented)
  - K-vertex-connected (advanced; rare)

====================================================================
H. DAG / SCC-DAG DP ALGORITHMS
====================================================================

- DP on DAG (Topological)
  - Longest path in DAG
  - Count paths in DAG
  - Min path cost in DAG

- SCC Condensation DP
  - Condense SCCs to DAG
  - DP on SCC DAG for reachability/counting/optimization

====================================================================
I. GRAPH GAMES / SPECIAL STRUCTURES (ICPC-rare but possible)
====================================================================

- Game on Graph
  - Winning states in directed graph (DP on DAG or retrograde BFS)
  - Draw detection via cycles
  - Grundy on DAG (impartial games)

- Euler / Hamilton (algorithmic)
  - Eulerian path/circuit (Hierholzer algorithm)
  - Hamiltonian path in DAG (DP/topo)
  - Hamiltonian path via bitmask DP (small n)

# End of Part 2
# Next: Part 3 will cover FULL DP (all variants + optimizations) at large scale.


# 🧠 ALGORITHMS MASTER LIST — PART 3
# Dynamic Programming — Complete Spectrum (Core → ICPC → Advanced → Research-Leaning)

====================================================================
A. CLASSIC 1D / 2D DP PROBLEMS
====================================================================

- Fibonacci DP
  - Iterative bottom-up
  - Fast doubling method
  - Matrix exponentiation Fibonacci

- Climbing Stairs
- Min Cost Climbing Stairs
- House Robber (linear DP)
- House Robber II (circular DP)
- Kadane’s Algorithm (maximum subarray)
- Maximum Subarray with constraints
- Maximum Product Subarray
- Longest Increasing Subsequence
  - O(n^2) DP
  - O(n log n) patience sorting method
- Longest Non-decreasing Subsequence
- Longest Bitonic Subsequence
- Longest Common Subsequence (LCS)
- Longest Common Substring
- Edit Distance (Levenshtein)
- Delete Operation Distance
- Interleaving Strings DP
- Palindrome Partitioning
- Longest Palindromic Subsequence
- Palindromic Substring DP
- Matrix Chain Multiplication
- Optimal Binary Search Tree (DP formulation)
- Partition Equal Subset Sum
- Subset Sum
- Target Sum (signed subset)
- Coin Change (minimum coins)
- Coin Change (count ways)
- Rod Cutting
- Integer Break
- Egg Dropping Problem
- Word Break DP
- Decoding Ways DP
- Catalan DP
- Derangement DP
- Staircase DP (variants)
- Decode Digit String (digit DP light)

====================================================================
B. KNAPSACK FAMILY
====================================================================

- 0/1 Knapsack
- Unbounded Knapsack
- Bounded Knapsack
- Multiple Knapsack (binary splitting)
- Group Knapsack
- Dependent Knapsack
- Knapsack with Constraints
- Meet-in-the-Middle Knapsack
- Bitset Knapsack Optimization
- Value-based Knapsack (DP by value)
- Multidimensional Knapsack
- Fractional Knapsack (greedy contrast)

====================================================================
C. INTERVAL / RANGE DP
====================================================================

- Interval DP (l,r)
  - Matrix chain multiplication
  - Optimal BST
  - Polygon triangulation
  - Burst balloons
- Palindrome partitioning DP
- Merge stones DP
- Optimal merging pattern DP
- Game interval DP (two-player)

====================================================================
D. TREE DP
====================================================================

- Subtree size DP
- Count nodes in subtree
- Tree diameter DP
- Maximum independent set in tree
- Tree vertex cover DP
- Tree coloring DP
- Tree knapsack DP
- Tree rerooting DP
- DP on rooted tree (postorder)
- DP on tree with states (include/exclude)
- Count paths in tree DP
- Distance sum in tree DP
- DP with parent state propagation
- DP on tree with heavy child optimization

====================================================================
E. DAG DP
====================================================================

- Longest path in DAG
- Shortest path in DAG (topo)
- Count paths in DAG
- DP on condensed SCC DAG
- DP with multiple sources
- DP with constraints on topological order

====================================================================
F. BITMASK / STATE COMPRESSION DP
====================================================================

- Traveling Salesman Problem (TSP) DP
- Assignment DP (bitmask)
- DP over subsets (2^n)
- DP over submasks
- DP over supermasks
- SOS DP (Sum over Subsets)
- Fast Zeta Transform
- Fast Möbius Transform
- Subset convolution DP
- DP for Hamiltonian path
- DP for partition into k subsets
- DP for Steiner tree (small k)
- Profile DP (grid tiling)
- Broken Profile DP
- Bitmask DP with transitions by removing bits

====================================================================
G. DIGIT DP
====================================================================

- Count numbers with constraints
- Sum of digits constraints
- Digit DP with tight flag
- Digit DP with leading zero handling
- Digit DP for divisibility
- Digit DP for forbidden patterns
- Digit DP for palindrome count
- Digit DP for bit constraints
- Digit DP for counting distinct digits
- Digit DP for monotone numbers

====================================================================
H. PROBABILITY / EXPECTED VALUE DP
====================================================================

- Expected number of steps DP
- Probability of reaching state DP
- Markov chain DP
- Absorbing states DP
- DP with fractional transitions
- DP on DAG with probabilities
- Linear equation solve for expectation (Gaussian elimination crossover)

====================================================================
I. DP OPTIMIZATION TECHNIQUES (ALGORITHMIC FORMS)
====================================================================

- Divide and Conquer DP Optimization
- Knuth Optimization
- Convex Hull Trick DP
- Li Chao Tree DP
- Monotonic Queue Optimization
- Quadrangle Inequality Optimization
- Monge Array Optimization
- SMAWK algorithm for totally monotone matrices
- Alien Trick (Lagrangian DP)
- Bitset Optimization
- Rolling Array Optimization
- Sparse State DP (map-based)
- Memory compression DP
- Precompute transitions DP

====================================================================
J. STRING DP
====================================================================

- Edit distance DP
- Longest palindromic subsequence DP
- LCS DP
- Distinct subsequences DP
- Regular expression matching DP
- Wildcard matching DP
- DP on prefix-function states
- DP on automaton (Aho-Corasick DP)
- DP with suffix automaton transitions

====================================================================
K. ADVANCED / RARE DP
====================================================================

- Digit DP with automaton
- Profile DP for 2D tiling
- Bitmask DP with inclusion-exclusion
- DP with meet-in-the-middle merge
- DP on tree decomposition (rare)
- DP with polynomial transitions
- DP with matrix exponentiation
- DP on compressed state graph
- DP with min-plus convolution
- DP with convolution (FFT accelerated)

====================================================================
L. GAME THEORY DP
====================================================================

- Grundy DP
- Mex computation DP
- Sprague-Grundy theorem DP
- Nim sum evaluation
- Game DP on graph
- Winning states DP
- Misère Nim handling
- Take-and-break DP
- DP for impartial combinatorial games

====================================================================
M. PARTITION / COUNTING DP
====================================================================

- Integer partition DP
- Bell numbers DP
- Stirling numbers DP
- Counting tilings DP
- Counting matchings DP
- Counting paths DP
- Counting colorings DP
- Counting bracket sequences DP

====================================================================
N. LINEAR RECURRENCE / MATRIX DP
====================================================================

- Matrix exponentiation for recurrence
- Fast doubling recurrence
- Transition matrix DP
- Exponentiation by squaring for DP transitions
- State transition via matrix multiplication
- Linear recurrence via characteristic polynomial (advanced)

====================================================================
O. ADVANCED DP + ALGEBRA CROSSOVER
====================================================================

- Polynomial DP
- Generating function DP
- Convolution-based DP
- Subset convolution DP
- Walsh-Hadamard transform DP
- Min-plus convolution DP
- DP with NTT acceleration
- DP with FWT acceleration

# End of Part 3
# Next: Part 4 — Strings (Full), Number Theory (Full), Combinatorics (Full), Geometry (Full)


# 🧠 ALGORITHMS MASTER LIST — PART 4
# Strings + Number Theory + Combinatorics (Deep Expansion)

====================================================================
A. STRING ALGORITHMS — PATTERN MATCHING
====================================================================

- Naive Pattern Matching
- Knuth–Morris–Pratt (KMP)
  - Prefix Function computation
  - Pattern matching via prefix function
- Z-Algorithm
  - Z-array construction
  - Pattern search using Z
- Rabin–Karp
  - Single hash
  - Double hash
  - Rolling polynomial hash
- Boyer–Moore (rare in CP but classical)
  - Bad character heuristic
  - Good suffix heuristic
- Aho–Corasick Automaton
  - Trie construction
  - Failure link construction
  - Multi-pattern search
- Suffix Automaton (SAM)
  - Online construction
  - Count distinct substrings
  - Longest common substring via SAM
- Suffix Array
  - Doubling algorithm
  - SA-IS (advanced linear time)
  - Radix-based doubling
- LCP Array
  - Kasai algorithm
- Suffix Tree
  - Ukkonen algorithm
  - Naive suffix tree build (educational)
- Manacher Algorithm
  - Odd-length palindromes
  - Even-length palindromes
- Booth Algorithm
  - Lexicographically minimal rotation
- Duval Algorithm
  - Lyndon factorization
- Burrows–Wheeler Transform
- FM-Index (advanced / research)
- Z-function for border detection
- Prefix-function for periodicity detection
- Border chain traversal
- Rolling hash substring compare
- String hashing with mod primes
- Hash collision reduction via double mod
- Substring equality via prefix hash
- Longest repeating substring via binary search + hash
- String isomorphism detection
- Wildcard matching DP
- Regular expression matching DP
- Palindromic Tree (Eertree)
- Minimal string rotation via doubling
- K-th lexicographic substring (suffix structures)
- Longest repeated substring (suffix array + LCP)
- Lexicographically k-th substring (advanced)
- Suffix automaton path counting
- Online substring query via automaton
- Longest common subsequence DP (relisted)
- Edit distance (relisted)

====================================================================
B. NUMBER THEORY ALGORITHMS — CORE
====================================================================

- Euclidean Algorithm (GCD)
- Binary GCD
- Extended Euclidean Algorithm
- LCM computation
- Modular exponentiation
- Modular inverse (extended Euclid)
- Modular inverse (Fermat)
- Sieve of Eratosthenes
- Linear Sieve
- Smallest Prime Factor Sieve
- Prime factorization via SPF
- Trial division factorization
- Miller–Rabin Primality Test
- Pollard Rho Factorization
- Chinese Remainder Theorem (CRT)
- Garner’s Algorithm (CRT implementation)
- Euler Totient function computation
- Totient sieve
- Möbius function computation
- Möbius inversion
- Divisor enumeration
- Divisor sum function
- Multiplicative function sieve
- Fast doubling Fibonacci
- Power tower modulo reduction (Euler theorem)
- Discrete Logarithm (Baby-step Giant-step)
- Primitive root finding
- Modular combinatorics precomputation
- Lucas Theorem
- Wilson’s theorem usage
- Legendre formula (power of prime in factorial)
- Counting trailing zeros in factorial
- Catalan number formula via nCr
- Binomial coefficient modulo composite
- Polynomial multiplication via NTT
- Chinese remainder reconstruction for NTT
- Fast exponentiation of polynomials
- Binomial transform
- Inclusion–Exclusion via mask iteration
- Floor sum algorithm (advanced CP trick)
- Linear congruence solver
- Diophantine equation solver
- Extended CRT
- Fast factorial modulo prime (advanced)
- Lagrange interpolation (mod prime)
- Newton’s method for polynomial inverse
- Polynomial derivative and integral (NTT context)

====================================================================
C. COMBINATORICS ALGORITHMS
====================================================================

- Pascal Triangle DP
- Precompute factorial and inverse factorial
- nCr computation modulo prime
- nPr computation
- Stars and Bars computation
- Inclusion–Exclusion subset algorithm
- Counting derangements
- Catalan DP
- Stirling numbers DP
- Bell numbers DP
- Partition number DP
- Burnside’s Lemma implementation
- Pólya Enumeration (rare)
- Counting permutations with constraints
- Counting arrangements with fixed points
- Counting subsets with constraints
- Counting paths in grid DP
- Counting paths with obstacles
- Counting colorings via DP
- Counting independent sets in tree (DP)
- Counting matchings in tree
- Counting spanning trees (Kirchhoff’s theorem)
- Kirchhoff matrix-tree theorem
- Determinant computation (Gaussian elimination)
- Subset convolution
- Fast Walsh–Hadamard Transform (FWT)
  - XOR convolution
  - AND convolution
  - OR convolution
- Zeta transform
- Möbius transform
- Polynomial convolution via FFT
- Polynomial convolution via NTT
- Polynomial exponentiation
- Formal power series inversion
- Lagrange inversion formula (rare)
- Combinatorial DP on subsets
- Meet-in-the-middle combinatorial count
- Derangement formula usage
- Counting binary strings without consecutive ones
- Counting with bit DP
- Counting cyclic structures
- Counting arrangements with symmetry

====================================================================
D. ADVANCED NUMBER THEORY / ALGEBRA (RESEARCH-LEANING)
====================================================================

- Fast Fourier Transform (FFT)
- Number Theoretic Transform (NTT)
- Bluestein FFT
- Polynomial multiplication via Karatsuba
- Karatsuba multiplication (big integers)
- Toom-Cook multiplication
- Polynomial division via NTT
- Polynomial GCD
- Berlekamp–Massey algorithm (linear recurrence)
- Berlekamp algorithm (factor polynomials) (rare)
- Cantor–Zassenhaus factorization (rare)
- Chinese remainder with multiple mod primes
- Hensel lifting (rare)
- Fast subset convolution (FWT)
- Multipoint polynomial evaluation
- Polynomial interpolation (Lagrange)
- Newton iteration for power series
- Modular square root (Tonelli–Shanks)
- Discrete root computation (advanced)
- Lucas theorem extension
- Primitive root enumeration
- Order of element modulo prime
- Baby-step giant-step discrete log
- Pollard Rho discrete log (rare)

# End of Part 4
# Next: Part 5 — Computational Geometry (Full), Advanced Graph + Flow Variants,
# Advanced Data Structure Algorithms, Offline/Query Algorithms, Randomized + Research.


# 🧠 ALGORITHMS MASTER LIST — PART 5
# Computational Geometry + Advanced Graph Variants + Data-Structure-Driven Algorithms

====================================================================
A. COMPUTATIONAL GEOMETRY — CORE
====================================================================

-- Primitives --

- Orientation test (cross product sign)
- Dot product computation
- Vector addition / subtraction
- Vector scaling
- Norm / length computation
- Squared distance optimization
- Projection of point onto line
- Distance from point to line
- Distance from point to segment
- Angle computation via atan2
- Compare angles without atan2 (cross product trick)

-- Line / Segment Algorithms --

- Line intersection (2 lines)
- Segment intersection test
- Proper segment intersection
- Collinear segment overlap detection
- Ray-segment intersection
- Half-line intersection

-- Polygon Algorithms --

- Polygon area (shoelace formula)
- Polygon orientation (CW/CCW)
- Convex polygon check
- Point in convex polygon (binary search)
- Point in polygon (ray casting)
- Winding number method
- Polygon centroid computation
- Polygon perimeter computation

-- Convex Hull --

- Graham Scan
- Andrew Monotone Chain
- Jarvis March (Gift wrapping)
- QuickHull (rare)
- Divide and Conquer Convex Hull

-- Rotating Calipers --

- Diameter of convex polygon
- Minimum width of convex polygon
- Maximum distance pair
- Antipodal pairs

-- Closest Pair of Points --

- Divide and conquer O(n log n)
- Sweep line closest pair
- Randomized incremental closest pair (rare)

-- Line Sweep Algorithms --

- Sweep line for segment intersection detection
- Sweep line for rectangle union area
- Sweep line for overlapping intervals
- Sweep line for skyline problem
- Event sorting + active structure

-- Circle Algorithms --

- Circle-line intersection
- Circle-circle intersection
- Tangents between circles
- Smallest enclosing circle (Welzl algorithm)
- Inscribed circle of triangle
- Circumcircle of triangle

-- Advanced Geometry --

- Half-plane intersection
- Minkowski sum
- Convex polygon intersection
- Convex hull trick (geometry dual)
- Line container optimization
- Delaunay triangulation (rare)
- Voronoi diagram (rare)
- Plane sweep for polygon intersection
- Pick’s theorem usage
- Lattice point counting
- 3D convex hull (rare)
- 3D orientation test

====================================================================
B. ADVANCED GRAPH ALGORITHMS (ICPC-RARE BUT POSSIBLE)
====================================================================

-- Advanced Shortest Paths --

- Multi-criteria shortest path
- Lexicographically smallest shortest path
- Shortest path with state augmentation
- Shortest path with constraints (DP + graph)
- Min-max path (bottleneck path)
- Widest path algorithm
- K shortest paths (Eppstein) (advanced)

-- Advanced Tree / Graph Decomposition --

- Tree centroid decomposition queries
- Link-cut tree (dynamic connectivity)
- Euler tour tree (dynamic)
- Top tree (advanced dynamic trees)
- Dynamic LCA (rare)
- Dynamic connectivity offline
- Bridge-finding dynamic update (advanced)

-- Advanced Matching / Flow Variants --

- Maximum closure problem (flow reduction)
- Flow with lower bounds
- Flow with node capacities (node-splitting)
- Circulation with demands
- Multi-commodity flow (theoretical)
- Min cut tree (Gomory-Hu)
- Parametric flow
- Min cost circulation
- Maximum density subgraph (flow-based)

-- Advanced Graph Theory Algorithms --

- Hamiltonian path DP (bitmask)
- Eulerian path (Hierholzer)
- Feedback vertex set (rare)
- Feedback edge set
- Minimum path cover in DAG
- Maximum independent set in bipartite
- Maximum independent set (general graph small n DP)
- Graph coloring backtracking (small n)
- Bron–Kerbosch maximal clique
- Maximum clique (branch and bound)
- Treewidth DP (rare)
- Planarity testing (Hopcroft–Tarjan) (rare)

====================================================================
C. DATA STRUCTURE DRIVEN ALGORITHMS
====================================================================

-- Fenwick Tree (Binary Indexed Tree) --

- Point update + prefix sum
- Range update + point query
- Range update + range query
- 2D Fenwick Tree
- Fenwick for inversion counting
- Fenwick for order statistics (binary lifting on tree)

-- Segment Tree --

- Build segment tree
- Point update
- Range query
- Lazy propagation
- Range update + range query
- Implicit segment tree
- Persistent segment tree
- Dynamic segment tree
- Segment tree beats (advanced)
- Merge sort tree
- Order statistic tree via segment tree
- 2D segment tree

-- Sparse Table --

- RMQ preprocessing
- Range GCD queries
- Idempotent queries
- Static range minimum

-- Balanced BST Algorithms --

- Treap (randomized BST)
- Implicit treap (sequence)
- Split and merge operations
- Order statistics tree
- AVL tree operations
- Red-black tree operations
- Splay tree (self-adjusting)
- Rope (sequence)
- Skip list

-- Advanced DS Algorithms --

- Li Chao Tree (dynamic convex hull trick)
- Convex hull trick (monotonic)
- Wavelet tree
- Persistent DSU
- Rollback DSU
- Square root decomposition
- Mo’s algorithm
- Mo’s with updates
- Coordinate compression
- Small-to-large merging maps
- Ordered set operations
- Multiset maintenance
- K-th order statistic (tree-based)
- Offline queries via sorting + BIT
- CDQ divide and conquer for dominance
- Persistent segment tree for K-th in range
- Euler tour flatten tree
- BIT for 2D offline queries

====================================================================
D. OFFLINE / QUERY PROCESSING ALGORITHMS
====================================================================

- Offline queries sorted by R
- Offline prefix queries
- Offline sweep with events
- Mo’s algorithm (sqrt decomposition)
- Mo’s with modifications
- CDQ divide and conquer
- Parallel binary search
- Offline dynamic connectivity (divide on time)
- Offline K-th smallest queries
- Offline inversion count queries
- Offline rectangle sum queries
- Coordinate compression + offline BIT

====================================================================
E. RANDOMIZED / PROBABILISTIC ALGORITHMS
====================================================================

- Randomized QuickSort
- Randomized QuickSelect
- Monte Carlo primality test
- Las Vegas algorithm retry
- Randomized hashing
- Random pivot partitioning
- Random sampling
- Reservoir sampling
- Random walk simulation
- Simulated annealing (heuristic)
- Randomized balancing trees
- Randomized incremental geometry

====================================================================
F. LINEAR ALGEBRA ALGORITHMS
====================================================================

- Gaussian elimination
- Gauss–Jordan elimination
- Determinant computation
- Matrix multiplication
- Fast matrix exponentiation
- Solve linear recurrence via matrix
- XOR basis insertion
- Rank computation
- Kirchhoff matrix-tree theorem
- Solve system of linear equations mod p
- Linear independence test
- Basis over GF(2)

====================================================================
G. ADVANCED / RESEARCH-LEANING ALGORITHMS
====================================================================

- Fast Walsh–Hadamard Transform
- XOR convolution
- AND convolution
- OR convolution
- Subset convolution
- Min-plus convolution
- Fast multipoint polynomial evaluation
- Polynomial inversion via Newton method
- Polynomial logarithm / exponential (advanced)
- Berlekamp–Massey
- Lagrange interpolation
- FFT over complex numbers
- NTT over finite fields
- Karatsuba multiplication
- Toom–Cook multiplication
- Discrete logarithm (Baby-step Giant-step)
- Pollard Rho discrete log
- Tonelli–Shanks modular sqrt
- Chinese remainder with large mod
- Fast floor sum algorithm
- Alien trick DP optimization
- SMAWK algorithm
- Monge array optimization
- Parametric search technique
- Min-cost circulation with potentials
- Link-cut tree dynamic operations
- Euler tour tree dynamic connectivity
- Persistent data structure queries
- Retroactive data structures (theoretical)

# End of Part 5
# Remaining expansion would cover:
# - Even deeper algebraic algorithms
# - Computational geometry in 3D
# - Advanced combinatorial generation
# - Game theory full expansion
# - Heuristic / NP-hard approximation algorithms
# - Parallel / distributed algorithms (theoretical)
# - Approximation algorithms
# - Randomized rounding
# - Submodular optimization

# 🧠 ALGORITHMS MASTER LIST — PART 6
# Game Theory + Approximation + NP-Hard + Heuristics + Advanced / Research Domains

====================================================================
A. GAME THEORY ALGORITHMS (COMBINATORIAL GAMES)
====================================================================

-- Impartial Games --

- Nim evaluation (xor of heaps)
- Grundy number computation
- Sprague–Grundy theorem
- Mex (minimum excluded value) computation
- Game on DAG (topological Grundy)
- Game on graph with cycles (detect draw states)
- Nim with multiple piles
- Nim with restricted moves
- Subtraction games DP
- Take-and-break games
- Kayles game DP
- Turning-toads / graph-based games
- Misère Nim handling
- Misère quotient (advanced / rare)
- Moore’s Nim variant
- Wythoff’s game (Beatty sequence solution)
- Fibonacci Nim

-- Partisan Games --

- Minimax algorithm
- Alpha-beta pruning
- Negamax
- Retrograde analysis
- Sprague–Grundy for impartial only (contrast)
- Game tree DP
- Grundy on tree
- Graph pursuit games (rare)

-- Stochastic Games --

- Expectimax
- Markov decision process (MDP)
- Value iteration (rare)
- Policy iteration (rare)

====================================================================
B. NP-HARD / EXACT EXPONENTIAL ALGORITHMS
====================================================================

-- Exact Exponential --

- Traveling Salesman Problem (TSP) via DP (Held–Karp)
- TSP via branch and bound
- TSP via meet-in-the-middle
- Maximum clique via branch-and-bound (Bron–Kerbosch)
- Maximum independent set (small n DP)
- Vertex cover via branching
- Set cover via backtracking
- Hamiltonian path via DP (bitmask)
- Subset sum meet-in-the-middle
- Steiner tree DP (small k)
- Exact cover (Algorithm X + Dancing Links)
- SAT solver (DPLL basic)
- 2-SAT via implication graph + SCC
- k-SAT backtracking (rare)
- Graph coloring via backtracking
- Partition into k subsets DP

-- Parameterized Algorithms (FPT style) --

- Vertex cover via branching (k parameter)
- Feedback vertex set (k parameter)
- Treewidth DP (small treewidth)
- Kernelization (conceptual)
- Meet-in-the-middle for small k
- Inclusion–exclusion exponential optimization

====================================================================
C. APPROXIMATION ALGORITHMS
====================================================================

- Greedy set cover (log n approx)
- 2-approx vertex cover
- MST-based TSP 2-approx
- Christofides TSP 1.5-approx (rare)
- Primal-dual approximation (rare)
- Local search for max cut
- Randomized rounding
- LP relaxation rounding
- PTAS concept (theoretical)
- Submodular greedy approximation

====================================================================
D. RANDOMIZED & PROBABILISTIC ALGORITHMS (ADVANCED)
====================================================================

- Randomized QuickSort
- Randomized QuickSelect
- Randomized primality test (Miller–Rabin)
- Monte Carlo estimation
- Las Vegas algorithm (retry until correct)
- Randomized incremental convex hull
- Randomized incremental Delaunay triangulation
- Random sampling for geometric problems
- Karger’s Min Cut algorithm
- Karger–Stein Min Cut
- Randomized matching (rare)
- Randomized rounding for LP
- Bloom filter construction
- Count-min sketch
- HyperLogLog
- MinHash for similarity

====================================================================
E. ADVANCED COMPUTATIONAL GEOMETRY (3D / RESEARCH-LEANING)
====================================================================

- 3D orientation test
- 3D convex hull (incremental)
- QuickHull 3D
- Delaunay triangulation
- Voronoi diagram construction
- Line-plane intersection
- Plane-plane intersection
- Convex polyhedron volume
- Ray tracing intersection tests
- Half-space intersection in 3D
- Rotating calipers in higher dimensions (rare)

====================================================================
F. ADVANCED ALGEBRA / POLYNOMIAL / TRANSFORMS
====================================================================

- FFT (Cooley–Tukey)
- Iterative FFT
- Recursive FFT
- NTT (Number Theoretic Transform)
- Bluestein FFT
- Chirp-Z transform
- Fast Walsh–Hadamard Transform
  - XOR convolution
  - AND convolution
  - OR convolution
- Subset convolution
- Min-plus convolution
- Polynomial multiplication (Karatsuba)
- Toom–Cook multiplication
- Polynomial division
- Polynomial inversion (Newton iteration)
- Polynomial logarithm
- Polynomial exponential
- Lagrange interpolation
- Fast multipoint evaluation
- Berlekamp–Massey
- Linear recurrence solver
- Chinese Remainder Theorem (large mods)
- Hensel lifting (rare)
- Cantor–Zassenhaus polynomial factorization

====================================================================
G. ADVANCED DATA STRUCTURES (ALGORITHMIC OPERATIONS)
====================================================================

- Persistent segment tree (kth order statistics)
- Persistent treap
- Rollback DSU
- Link-cut tree
- Euler tour tree
- Top tree
- Splay tree operations
- Rope operations
- Order statistic tree
- Interval tree
- Fenwick 2D / 3D
- Segment tree beats
- Merge sort tree
- Wavelet tree
- KD-tree
- Range tree
- R-tree (rare)
- Treap with implicit keys
- Skip list operations
- Cache-oblivious B-tree (theoretical)
- Van Emde Boas tree (advanced)
- X-fast trie
- Y-fast trie

====================================================================
H. INFORMATION THEORY / ADVANCED CONCEPTUAL
====================================================================

- Entropy computation
- Huffman coding
- Shannon-Fano coding
- Arithmetic coding
- Data compression basics
- Suffix array compression (BWT-based)
- FM-index
- LZ77 / LZ78 (conceptual)
- Run-length encoding (basic)

====================================================================
I. PARALLEL / DISTRIBUTED (THEORETICAL)
====================================================================

- Parallel prefix sum (scan)
- Parallel BFS (concept)
- MapReduce word count (concept)
- Distributed hash table (concept)
- Chord protocol (concept)
- Kademlia routing (concept)

====================================================================
J. NUMERICAL METHODS (ADVANCED / RARE IN ICPC)
====================================================================

- Newton–Raphson method
- Binary search root finding
- Bisection method
- Simpson’s rule integration
- Numerical differentiation
- Gaussian elimination (floating point)
- LU decomposition
- QR decomposition (concept)
- Eigenvalue power iteration (concept)
- Matrix exponentiation large power

====================================================================
K. HEURISTICS / METAHEURISTICS (RARE BUT POSSIBLE)
====================================================================

- Simulated annealing
- Genetic algorithm (conceptual)
- Local search hill climbing
- Tabu search (conceptual)
- Greedy randomized adaptive search
- Beam search
- Iterative deepening A*
- Heuristic pruning search

====================================================================
L. ADVANCED GRAPH THEORY (RARE / RESEARCH)
====================================================================

- Planarity testing (Hopcroft–Tarjan)
- Graph isomorphism (VF2 concept)
- Tree isomorphism (AHU)
- Maximum flow with scaling
- Parametric max flow
- Submodular minimization (rare)
- Gomory–Hu tree
- Maximum closure problem
- Minimum feedback arc set (heuristic)
- K-core decomposition
- Degeneracy ordering
- Dominator tree (flow graphs)

====================================================================
M. ADDITIONAL SPECIALIZED ALGORITHMS
====================================================================

- Skyline problem (heap + sweep)
- Sliding window maximum (deque)
- Next greater element (stack)
- Histogram largest rectangle (stack)
- Trapping rain water (two pointers / stack)
- Convex hull trick DP
- Li Chao tree
- Alien trick DP
- Divide and conquer DP optimization
- Knuth optimization
- SMAWK optimization
- Mo’s algorithm with updates
- Parallel binary search
- CDQ divide and conquer
- Bitset convolution optimization
- Fast I/O buffered algorithm (implementation-level)

# End of Part 6

# This concludes a very broad sweep from basics → ICPC → advanced → research-level algorithms.
# If you want to go even deeper, we can now:
#  - Expand any single domain into 100+ more granular algorithmic sub-variants
#  - Create a fully indexed master taxonomy
#  - Convert this into a learning roadmap
#  - Map algorithms to paradigms and strategies

# 🧠 ALGORITHMS MASTER LIST — PART 7
# Ultra-Advanced / Rare / Cross-Domain / Theoretical Algorithms
# (Deep expansion for completeness beyond ICPC core)

====================================================================
A. ADVANCED GRAPH THEORY & STRUCTURAL ALGORITHMS
====================================================================

-- Structural Graph Algorithms --

- K-Core Decomposition
- Degeneracy Ordering
- Maximum Clique via Bron–Kerbosch with pivot
- Maximum Clique via branch-and-bound
- Chordal Graph Recognition (MCS algorithm)
- Perfect Elimination Ordering
- Maximum Cardinality Search
- Tree Decomposition (nice tree decomposition DP)
- Treewidth DP
- Pathwidth algorithms (rare)
- Feedback Vertex Set (branching FPT)
- Feedback Edge Set
- Minimum Cycle Basis
- Johnson’s Simple Cycles Algorithm
- Directed Minimum Spanning Tree (Edmonds’ algorithm)
- Arborescence algorithms
- Dominator Tree (Lengauer–Tarjan)
- Strong orientation of graph
- K-edge-connected components
- K-vertex-connected components (advanced)
- Planarity Testing (Hopcroft–Tarjan)
- Planar Separator Theorem algorithm (conceptual)
- Dual graph construction (planar graphs)
- Gomory–Hu Tree construction
- Maximum Density Subgraph (flow reduction)
- Minimum Mean Cycle (Karp’s algorithm)

====================================================================
B. ADVANCED FLOW / MATCHING VARIANTS
====================================================================

- Capacity Scaling Max Flow
- Dinic with capacity scaling
- Push–Relabel with gap heuristic
- Highest label push–relabel
- Min-Cost Flow with potentials
- Successive shortest path with Dijkstra + potentials
- Cycle canceling algorithm
- Min-Cost Circulation
- Lower bound flow transformation
- Parametric max flow
- Multi-source multi-sink max flow
- Maximum closure problem (flow reduction)
- Maximum bipartite matching via flow
- Weighted matching (Hungarian)
- Blossom V (improved general matching)
- Maximum matching in general graph (Mical algorithm variant)

====================================================================
C. ADVANCED TREE / DYNAMIC GRAPH ALGORITHMS
====================================================================

- Link-Cut Tree operations (splay-based)
- Euler Tour Tree dynamic connectivity
- Top Tree dynamic operations
- Dynamic MST (conceptual)
- Dynamic connectivity via divide-and-conquer on time
- Persistent tree path queries
- Centroid path decomposition
- Rerooting via prefix-suffix merging
- Tree isomorphism (AHU)
- Subtree hashing
- Heavy-light with segment tree for path updates
- DSU rollback with time segments
- Offline dynamic LCA

====================================================================
D. ADVANCED STRING / TEXT PROCESSING
====================================================================

- Ukkonen Suffix Tree (linear-time)
- SA-IS suffix array construction
- DC3 (Skew algorithm) suffix array
- Suffix automaton with topological ordering
- LZ77 compression (conceptual)
- LZ78 compression
- Z-algorithm with modifications
- Palindromic tree (Eertree) full implementation
- KMP automaton construction
- Aho–Corasick failure automaton DP
- String matching with wildcards
- Longest common substring via suffix array
- Longest common substring via suffix automaton
- Lexicographically minimal rotation (Booth)
- Lyndon factorization (Duval)
- Burrows–Wheeler transform
- FM-index compressed search
- Suffix automaton substring count
- Suffix automaton DP on paths
- String hashing with polynomial rolling hash
- Double hashing collision control
- Palindrome checking with hashing
- Substring comparison via prefix hash
- Minimal absent word detection (advanced)

====================================================================
E. ADVANCED GEOMETRY (FULL EXPANSION)
====================================================================

-- Convex Hull Variants --

- Graham Scan
- Monotone Chain
- QuickHull
- Chan’s Algorithm (output-sensitive)
- Divide-and-conquer convex hull

-- 3D Geometry --

- 3D Convex Hull
- 3D Orientation Test
- Line-plane intersection
- Plane-plane intersection
- Polyhedron volume computation
- Ray casting in 3D
- Delaunay triangulation (2D)
- Voronoi diagram construction

-- Advanced Geometric Techniques --

- Half-plane intersection
- Minkowski sum
- Rotating calipers for width
- Closest pair (divide-and-conquer)
- Line sweep intersection detection
- Bentley–Ottmann algorithm
- KD-tree nearest neighbor search
- Range tree (orthogonal range queries)
- Segment tree for rectangle union
- Polygon triangulation
- Ear clipping triangulation
- Pick’s theorem
- Lattice point counting via geometry
- Convex polygon intersection
- Geometric duality transformation

====================================================================
F. ADVANCED NUMBER THEORY / ALGEBRA
====================================================================

- FFT (Cooley–Tukey)
- Iterative FFT
- Bluestein FFT
- NTT (mod prime)
- CRT-based NTT for large mod
- Karatsuba multiplication
- Toom–Cook multiplication
- Polynomial division via NTT
- Polynomial GCD
- Fast multipoint evaluation
- Newton iteration for polynomial inverse
- Formal power series exponentiation
- Formal power series logarithm
- Berlekamp–Massey (linear recurrence)
- Cantor–Zassenhaus polynomial factorization
- Hensel lifting
- Tonelli–Shanks modular sqrt
- Baby-step Giant-step discrete log
- Pollard Rho discrete log
- Chinese Remainder Theorem extended
- Fast floor sum
- Lucas theorem
- Legendre formula
- Wilson theorem usage
- Primitive root search
- Multiplicative function sieve
- Dirichlet convolution
- Möbius inversion
- Zeta transform
- Walsh–Hadamard transform
- Subset convolution

====================================================================
G. ADVANCED COMBINATORICS / COUNTING
====================================================================

- Burnside’s Lemma
- Pólya Enumeration
- Kirchhoff’s Matrix Tree Theorem
- Determinant via Gaussian elimination
- Stirling numbers DP
- Bell numbers DP
- Partition number DP
- Inclusion–Exclusion over subsets
- Combinatorial DP with bitmask
- Subset convolution DP
- Counting independent sets in tree
- Counting spanning trees
- Counting matchings
- Counting Hamiltonian paths (DP)
- Counting tilings DP
- Counting colorings DP
- Counting labeled trees (Cayley’s formula)

====================================================================
H. RANDOMIZED / PROBABILISTIC (FULLER)
====================================================================

- Karger’s Min Cut
- Karger–Stein Min Cut
- Randomized incremental convex hull
- Reservoir sampling
- Random sampling with weights
- Monte Carlo primality test
- Las Vegas algorithm framework
- Randomized pivot quicksort
- Randomized balancing BST
- Bloom filter
- Count-min sketch
- HyperLogLog
- MinHash
- Randomized rounding
- Simulated annealing
- Genetic algorithm (conceptual)
- Local search heuristic
- Tabu search (conceptual)

====================================================================
I. APPROXIMATION & OPTIMIZATION (THEORETICAL)
====================================================================

- Greedy Set Cover
- 2-Approx Vertex Cover
- Christofides TSP (1.5-approx)
- Primal-Dual approximation
- Local search Max-Cut
- LP relaxation rounding
- Submodular greedy
- PTAS concept
- FPTAS knapsack
- Randomized rounding
- Dual fitting technique

====================================================================
J. PARALLEL / DISTRIBUTED (THEORETICAL)
====================================================================

- Parallel prefix sum
- Parallel BFS
- MapReduce word count
- Distributed hash table
- Chord protocol
- Kademlia routing
- Paxos (conceptual)
- Raft (conceptual)

====================================================================
K. NUMERICAL METHODS (RARE)
====================================================================

- Newton–Raphson
- Bisection method
- Secant method
- Simpson integration
- Numerical differentiation
- LU decomposition
- QR decomposition
- Eigenvalue via power iteration
- Jacobi method

====================================================================
L. META / STRUCTURAL ALGORITHMIC PATTERNS
====================================================================

- Divide and conquer
- Greedy construction
- Dynamic programming
- Meet-in-the-middle
- State compression
- Binary search on answer
- Two pointers
- Sliding window
- Sweep line
- Rerooting
- Offline processing
- Parametric search
- Small-to-large merging
- Convex hull trick
- CDQ divide-and-conquer
- Mo’s algorithm
- Parallel binary search
- DSU rollback

# End of Part 7

# At this point, we have covered:
# - Core
# - Graph (full)
# - DP (full)
# - Strings (full)
# - Number theory (full)
# - Combinatorics (full)
# - Geometry (full)
# - Flow / Matching
# - Advanced data structures
# - Randomized
# - Approximation
# - Research-level concepts


# 🧠 ALGORITHMS MASTER LIST — PART 8
# Offline / Range Query / Decomposition / Transform / Special-Purpose Advanced Algorithms

====================================================================
A. RANGE QUERY / OFFLINE QUERY ALGORITHMS (VERY IMPORTANT IN ICPC)
====================================================================

- Prefix Sum Algorithms
  - 1D prefix sums
  - 2D prefix sums (integral image)
  - 3D prefix sums (rare)
  - Prefix XOR arrays
  - Prefix min/max arrays (monotone prefix)

- Difference Array Algorithms
  - 1D difference for range add
  - 2D difference (imos) for rectangle updates
  - Difference + prefix rebuild
  - Event-based difference sweeps

- Static Range Query Algorithms
  - Sparse Table (RMQ)
  - Disjoint Sparse Table
  - Cartesian tree + RMQ
  - Fischer–Heun RMQ (succinct RMQ) (advanced)
  - Range GCD queries (sparse table)
  - Range min/max queries (sparse table)
  - Range AND/OR queries (idempotent ops)

- Fenwick/BIT Query Algorithms
  - BIT prefix sum
  - BIT range update point query
  - BIT range update range query
  - BIT order statistics (find kth via BIT binary lifting)
  - 2D BIT point update rectangle sum query
  - BIT for inversion counting
  - BIT for offline counting (sweep line + BIT)

- Segment Tree Query Algorithms
  - Segment tree point update range query
  - Segment tree range update lazy propagation
  - Implicit segment tree (coordinate sparse)
  - Dynamic segment tree
  - Persistent segment tree (versioned queries)
  - Segment tree beats (advanced min/max constraints)
  - Segment tree for order statistics (kth)
  - Segment tree for offline coordinate compression
  - 2D segment tree (rare)
  - Segment tree of vectors (merge sort tree build/query)

- Merge Sort Tree Algorithms
  - Build merge sort tree
  - Query count <= x in range
  - Query kth in range (with binary search)

- Wavelet Tree Algorithms (advanced)
  - Build wavelet tree
  - Range kth query
  - Range count <= x query
  - Range frequency query

- Offline Query Reordering
  - Sort queries by right endpoint
  - Sort by left endpoint
  - Sweep line with events (add/remove)
  - Offline prefix processing
  - Offline coordinate compression

- Mo’s Algorithm Family
  - Standard Mo’s algorithm (static array)
  - Mo’s with modifications (time dimension)
  - Mo’s on trees (Euler tour + Mo’s)
  - Mo’s on graphs (rare)
  - Hilbert order Mo’s (optimization)

- Parallel Binary Search (offline)
  - Parallel BS for kth / threshold queries
  - Parallel BS with DSU (connectivity thresholds)
  - Parallel BS with BIT/segment tree

- CDQ Divide & Conquer (offline)
  - CDQ dominance counting (2D/3D)
  - CDQ on time (updates + queries)
  - CDQ + BIT/segment tree integration

- Offline Dynamic Connectivity
  - Divide on time segments + rollback DSU
  - Segment tree over time intervals + rollback DSU
  - Offline edge add/remove queries

====================================================================
B. DECOMPOSITION FRAMEWORK ALGORITHMS
====================================================================

- Sqrt Decomposition (block decomposition)
  - Block rebuild strategy
  - Offline block processing
  - Mo’s as sqrt-decomposition

- Heavy-Light Decomposition (HLD)
  - Path query via segment tree
  - Path update via lazy segtree
  - LCA integrated HLD

- Centroid Decomposition
  - Build centroid tree
  - Distance query updates
  - Color/activate node queries

- DSU on Tree (Small-to-large)
  - Keep heavy child contributions
  - Merge light child contributions
  - Answer subtree queries

- Rerooting DP
  - Prefix/suffix contributions per node
  - Reroot with accumulator transfer

- Graph Decompositions (advanced)
  - Block-cut tree decomposition
  - Bridge tree decomposition
  - SPQR decomposition (rare)

====================================================================
C. BITSET / SUBSET TRANSFORMS / FAST TRANSFORMS (EXPANDED)
====================================================================

- SOS DP (Sum Over Subsets)
  - Zeta transform over subsets
  - Möbius transform over subsets
  - SOS max/min variants (advanced)
  - SOS for DP transitions

- Fast Walsh–Hadamard Transform (FWT)
  - XOR convolution FWT
  - AND convolution FWT
  - OR convolution FWT
  - Subset XOR basis convolution patterns

- Subset Convolution
  - O(n^2 2^n) subset convolution
  - Fast subset convolution (advanced)
  - Convolution by popcount layers

- Bitset Accelerated DP
  - Bitset knapsack (shift-or)
  - Bitset reachability transitive closure (small n)
  - Bitset BFS on dense graphs
  - Bitset convolution tricks for DP

====================================================================
D. SPECIAL GRAPH ALGORITHMS (MORE)
====================================================================

- Minimum Mean Cycle
  - Karp’s minimum mean cycle algorithm

- Assignment / Transportation
  - Hungarian algorithm (assignment)
  - Min-cost max-flow for assignment variant
  - Successive shortest augmenting path for assignment

- Matroid Algorithms (rare / research)
  - Matroid greedy (when applicable)
  - Matroid intersection (advanced)
  - Matroid parity (research-level)

- Shortest Paths Specialized
  - Johnson’s APSP
  - Dial’s for small weights
  - 0-k BFS generalization
  - Min-plus convolution shortest path (theoretical)

- Dominators
  - Lengauer–Tarjan dominator tree algorithm

====================================================================
E. ADVANCED NUMBER THEORY / COMPUTATIONAL ALGEBRA (MORE)
====================================================================

- Modular Square Root
  - Tonelli–Shanks algorithm

- Discrete Log
  - Baby-step Giant-step (BSGS)
  - Pohlig–Hellman (requires factorization) (advanced)
  - Pollard Rho for discrete log (rare)

- Primality / Factorization
  - Miller–Rabin deterministic bases (implementation detail)
  - Pollard Rho factorization
  - Brent’s cycle detection variant (Pollard)
  - Fermat factorization (rare)
  - Pollard p-1 method (rare)

- Polynomial Algorithms (expanded)
  - Polynomial multiplication (FFT/NTT)
  - Polynomial division
  - Polynomial inversion (Newton)
  - Polynomial sqrt (Newton) (advanced)
  - Polynomial log/exp (advanced)
  - Multipoint evaluation (advanced)
  - Multipoint interpolation (advanced)
  - Berlekamp–Massey (linear recurrence)
  - Kitamasa algorithm (linear recurrence) (CP-advanced)

- CRT Variants
  - Standard CRT
  - CRT for non-coprime mod (general CRT)
  - Garner’s algorithm (CRT reconstruction)

====================================================================
F. ADVANCED GEOMETRY ALGORITHMS (MORE)
====================================================================

- Bentley–Ottmann sweep line (segment intersection reporting)
- Half-plane intersection (HPI)
- Convex polygon intersection
- Minkowski sum
- Delaunay triangulation (rare)
- Voronoi diagram construction (rare)
- KD-tree nearest neighbor
- Range tree orthogonal queries
- Point location in planar subdivision (rare)
- 3D convex hull (incremental) (rare)

# End of Part 8

# 🧠 ALGORITHMS MASTER LIST — PART 9
# Linear Algebra + Exact Exponential + Parameterized + Advanced Optimization

====================================================================
A. LINEAR ALGEBRA ALGORITHMS (COMPLETE EXPANSION)
====================================================================

-- Gaussian Elimination Variants --

- Gaussian elimination (floating point)
- Gaussian elimination (mod prime)
- Gaussian elimination (mod composite with CRT)
- Gauss–Jordan elimination
- Reduced row echelon form (RREF)
- Rank computation via elimination
- Determinant via elimination
- Solve Ax = b system
- Solve multiple RHS systems
- Sparse Gaussian elimination (conceptual)

-- Matrix Algorithms --

- Matrix multiplication O(n^3)
- Strassen matrix multiplication (advanced)
- Fast matrix exponentiation
- Binary exponentiation for matrices
- Matrix exponentiation for DP transitions
- Matrix exponentiation for linear recurrence
- Matrix exponentiation for adjacency powers (path counting)
- Min-plus matrix multiplication
- Boolean matrix multiplication (bitset accelerated)

-- Decompositions (theoretical but useful knowledge) --

- LU decomposition
- LUP decomposition
- Cholesky decomposition (positive definite)
- QR decomposition
- Eigenvalue power iteration
- Fast exponentiation of linear operators

-- Finite Field Linear Algebra --

- Solve linear system mod p
- Solve linear system mod 2 (XOR basis)
- XOR basis construction
- XOR basis maximize value query
- XOR basis k-th smallest query (advanced)
- Linear independence test over GF(2)
- Gaussian elimination over GF(2)

-- Combinatorial Linear Algebra --

- Kirchhoff Matrix Tree Theorem
- Determinant mod p for spanning tree count
- Rank-nullity applications
- Solve system for probability transitions
- Solve expectation equations via linear algebra

====================================================================
B. EXACT EXPONENTIAL / MEET-IN-THE-MIDDLE FAMILY
====================================================================

-- Meet-in-the-Middle Techniques --

- Subset sum MITM
- Partition equal sum MITM
- Knapsack MITM
- Counting subset sums MITM
- XOR subset MITM
- 4-sum via MITM
- Balanced partition MITM

-- Branch & Bound Algorithms --

- TSP branch and bound
- Maximum clique branch and bound
- Maximum independent set branch and bound
- Graph coloring branch and bound
- Set cover branch and bound

-- Inclusion–Exclusion Exponential --

- Count permutations with constraints
- Count surjections
- Count graph colorings
- Count subsets with forbidden cond

# 🧠 ALGORITHMS MASTER LIST — PART 10
# Ultra-Granular Variants + Specialized + Theoretical Expansions

====================================================================
A. ADVANCED SHORTEST PATH VARIANTS
====================================================================

- Shortest path with exactly k edges
- Shortest path with at most k edges
- Shortest path with forbidden nodes
- Shortest path with forbidden edges
- Constrained shortest path (budget constraint)
- Multi-layer graph modeling shortest path
- Lexicographically smallest shortest path
- Shortest path with color constraints
- Shortest path with parity constraints
- Shortest alternating path (color alternating)
- Time-expanded graph shortest path
- Shortest path in dynamic graph (offline)
- Minimum bottleneck path
- Maximum capacity path (widest path)
- Shortest path avoiding cycles (DP on DAG)
- Shortest path with state compression
- K-th shortest path (Yen)
- Eppstein’s K-shortest paths (advanced)
- Replacement paths problem
- All shortest path edges detection
- Shortest cycle detection
- Girth computation
- Minimum mean weight cycle (Karp)

====================================================================
B. ADVANCED TREE ALGORITHMS (MORE VARIANTS)
====================================================================

- Tree flattening via Euler tour
- Subtree query via Euler interval
- Binary lifting for k-th ancestor
- Binary lifting for weighted jump
- Distance queries via LCA
- Virtual tree construction
- Tree DP with bitmask
- Tree knapsack DP
- Counting paths with given sum
- Path sum with prefix hash
- Heavy-light for path updates
- Centroid decomposition for distance queries
- Rerooting with prefix/suffix accumulation
- Tree DP for maximum matching
- Tree DP for independent set
- Tree DP for vertex cover
- Tree DP for subtree diameter
- Subtree isomorphism hashing
- Tree canonical form computation
- Prüfer code encoding
- Prüfer code decoding

====================================================================
C. ADVANCED MATCHING & COVER PROBLEMS
====================================================================

- Maximum bipartite matching (Hopcroft–Karp)
- Minimum vertex cover (bipartite via König)
- Maximum independent set (bipartite)
- Minimum path cover in DAG
- Assignment via Hungarian
- General matching via Blossom
- Weighted matching
- Maximum weighted matching (general graph)
- Dilworth decomposition (posets)
- Hall’s theorem check (constructive)

====================================================================
D. ADVANCED FLOW SPECIAL CASES
====================================================================

- Max flow with node capacities
- Flow with lower bounds
- Circulation with demands
- Feasible flow detection
- Min cut extraction
- Global min cut (Stoer–Wagner)
- All pairs min cut (Gomory–Hu)
- Parametric max flow
- Maximum closure problem
- Minimum cut in directed graph
- Maximum density subgraph
- Project selection problem (flow modeling)

====================================================================
E. ADVANCED DP MICRO-VARIANTS
====================================================================

- DP with bitmask and transitions via submask
- DP with profile compression
- DP with monotonic queue optimization
- DP with convex hull trick
- DP with divide-and-conquer optimization
- DP with knuth optimization
- DP with quadrangle inequality
- DP with bitset acceleration
- DP with meet-in-the-middle merge
- DP with rolling hash states
- DP on compressed state graph
- DP on automaton (AC automaton DP)
- DP with polynomial convolution
- DP via matrix exponentiation
- DP via linear recurrence solver (Kitamasa)
- DP with digit constraints
- DP with inclusion–exclusion
- DP over subsets by popcount

====================================================================
F. ADVANCED STRING MICRO-ALGORITHMS
====================================================================

- Prefix function border tree
- Z-function periodicity detection
- Border chain traversal
- Minimal period detection
- Longest border detection
- Substring hashing with double mod
- Rolling hash sliding window
- Lexicographically minimal substring
- Count distinct substrings (SAM)
- Count distinct substrings (SA + LCP)
- Longest common substring (SAM)
- Longest common substring (SA)
- Palindromic tree (Eertree)
- Manacher odd/even separation
- KMP automaton building
- Aho–Corasick DP over states
- Suffix automaton endpos sets
- Suffix automaton link tree traversal
- Suffix array LCP sparse table queries
- RMQ over LCP array
- Lexicographic k-th substring

====================================================================
G. ADVANCED NUMBER THEORY MICRO-ALGORITHMS
====================================================================

- Fast exponentiation with overflow protection
- Fast modular multiplication (128-bit reduction)
- Barrett reduction
- Montgomery multiplication
- Miller–Rabin deterministic base selection
- Pollard Rho with Brent cycle detection
- Fast divisor counting
- Fast sigma function computation
- Multiplicative function sieve
- Möbius inversion application
- Dirichlet convolution computation
- Fast floor sum (AtCoder library trick)
- Lucas theorem for nCr mod prime
- Lucas theorem generalized
- Chinese Remainder Theorem merge
- Garner algorithm
- Tonelli–Shanks sqrt mod p
- Primitive root search
- Order of element mod p
- Baby-step giant-step discrete log
- Pohlig–Hellman (factor p-1)

====================================================================
H. ADVANCED GEOMETRY MICRO-ALGORITHMS
====================================================================

- Cross product orientation test
- Dot product projection
- Segment-segment intersection
- Line intersection
- Ray casting point-in-polygon
- Winding number point-in-polygon
- Convex hull monotone chain
- Rotating calipers diameter
- Closest pair divide and conquer
- Sweep line event handling
- Half-plane intersection
- Minkowski sum of convex polygons
- Convex polygon intersection
- Smallest enclosing circle (Welzl)
- KD-tree nearest neighbor
- Rectangle union area via sweep
- Skyline problem via sweep + heap

====================================================================
I. ADVANCED BITWISE / TRANSFORM ALGORITHMS
====================================================================

- Submask iteration
- Supermask iteration
- SOS DP
- Fast zeta transform
- Fast Möbius transform
- Walsh–Hadamard transform (XOR)
- Walsh–Hadamard transform (AND)
- Walsh–Hadamard transform (OR)
- Subset convolution
- Bitset convolution optimization
- XOR basis insertion
- XOR basis query max

====================================================================
J. STRUCTURAL / META ALGORITHMIC PATTERNS (COMPLETE)
====================================================================

- Divide and conquer
- Greedy choice property
- Dynamic programming
- State compression
- Meet-in-the-middle
- Binary search on answer
- Two pointers
- Sliding window
- Sweep line
- Rerooting
- Offline processing
- Parametric search
- Small-to-large merging
- Convex hull trick
- CDQ divide-and-conquer
- Mo’s algorithm
- Parallel binary search
- Rollback data structure
- Lazy propagation
- Persistent data structures
- Randomized balancing
- Backtracking + pruning
- Branch and bound
- Inclusion–exclusion
- Coordinate compression
- Difference array
- Prefix sum transformation
- Euler tour flattening
- Topological DP
- Graph condensation
- State augmentation
- Modeling via reduction
- Transform domain convolution
- Generating functions
- Matrix exponentiation modeling
- Automaton modeling
- Time expansion modeling
- Multi-layer graph modeling
- Flow reduction modeling
- Dual graph modeling
- Potential reweighting trick
- Reparameterization (Alien trick)

# End of Part 10


# 🧠 ALGORITHMS MASTER LIST — PART 11
# External Memory + Streaming + Succinct + Advanced Graph + Advanced Geometry + Advanced Algebra

====================================================================
A. EXTERNAL MEMORY / I/O-EFFICIENT ALGORITHMS (RARE IN ICPC, RESEARCH-LEVEL)
====================================================================

- External Merge Sort (multiway merge)
- Replacement Selection (run generation)
- Multiway Merge (k-way heap merge)
- Buffer Tree (I/O-efficient range updates) (advanced)
- Bε-tree update-friendly indexing (advanced)
- Cache-oblivious algorithms (family)
  - Cache-oblivious matrix transpose
  - Cache-oblivious B-tree / vEB layout
  - Cache-oblivious sorting (funnel sort) (advanced)
- Funnel Sort (cache-oblivious) (advanced)
- External Memory BFS (conceptual)
- External Memory MST (conceptual)
- External Memory Priority Queue (conceptual)

====================================================================
B. STREAMING / SKETCHING / APPROXIMATE ALGORITHMS
====================================================================

- Bloom Filter construction
  - Standard Bloom filter
  - Counting Bloom filter
- Cuckoo Filter
- Quotient Filter
- Count-Min Sketch
  - Conservative update variant
- HyperLogLog
- KMV / K-minimum values sketch
- MinHash signatures
- Theta sketch (conceptual)
- Reservoir Sampling
  - Reservoir sampling (k samples)
  - Weighted reservoir sampling (advanced)
- Misra–Gries heavy hitters
- SpaceSaving heavy hitters
- Flajolet–Martin (historical cardinality)
- Sliding window streaming (conceptual)
- AMS sketch (frequency moments) (advanced)
- Count sketch (advanced)
- LSH (locality-sensitive hashing) (conceptual)

====================================================================
C. SUCCINCT / COMPRESSED DATA STRUCTURE ALGORITHMS
====================================================================

- Rank/Select on bitvectors (succinct primitives)
- Succinct RMQ (Fischer–Heun)
- Wavelet Tree
  - Range count
  - Range kth
  - Range quantile
- Compressed Suffix Array (CSA) (advanced)
- FM-index
- Burrows–Wheeler Transform (BWT)
- LOUDS encoding of trees (succinct) (advanced)
- Balanced parentheses representation of trees (advanced)
- Elias–Fano encoding (advanced)
- Succinct graph representations (conceptual)

====================================================================
D. ADVANCED GRAPH ALGORITHMS (RESEARCH-LEANING)
====================================================================

-- Min-Cut / Connectivity / Structure --

- Karger min-cut (randomized)
- Karger–Stein min-cut (improved randomized)
- Stoer–Wagner global min-cut (deterministic)
- Gomory–Hu tree (all-pairs min-cut)
- Nagamochi–Ibaraki min-cut (advanced / rare)

-- Shortest Paths Advanced --

- Contraction Hierarchies (road networks) (research)
- Hub Labeling shortest path (research)
- Thorup shortest path (integer weights) (theoretical)
- APSP via min-plus convolution (theoretical)

-- Graph Structure / Minors (rare) --

- Treewidth approximation (concept)
- Separator-based algorithms (planar/sparse) (concept)
- Graph minor decomposition (research concept)

-- Dominators / Flow Graphs --

- Lengauer–Tarjan dominator tree
- Dominator tree applications (control-flow / reachability)

-- Matchings Advanced --

- Maximum matching in general graphs (Edmonds blossom)
- Weighted matching (general) (advanced)
- Matroid intersection (advanced / research)
- Matroid parity (research)

====================================================================
E. ADVANCED PLANAR GRAPH ALGORITHMS (RARE)
====================================================================

- Planarity testing (Hopcroft–Tarjan)
- Planar embeddings construction (concept)
- Dual graph construction (planar)
- Planar shortest paths (specialized; research)
- Planar min-cut via dual (advanced)
- Planar separator applications (concept)

====================================================================
F. ADVANCED COMPUTATIONAL GEOMETRY (MORE SPECIALIZED)
====================================================================

-- Arrangements / Intersection Reporting --

- Bentley–Ottmann sweep line (segment intersection reporting)
- Arrangement of lines (concept)
- Point location in planar subdivision (advanced)
- Trapezoidal map (randomized) (advanced)

-- Voronoi / Delaunay --

- Fortune’s algorithm for Voronoi (advanced)
- Delaunay triangulation incremental
- Delaunay triangulation divide-and-conquer
- Voronoi diagram from Delaunay (dual)

-- Convex / Halfspace --

- Half-plane intersection (2D)
- Halfspace intersection (3D) (advanced)
- Linear programming in fixed dimension (Seidel randomized LP) (advanced)

-- Nearest Neighbor / Range Searching --

- KD-tree nearest neighbor
- Ball tree (metric) (concept)
- Range tree (orthogonal)
- Segment tree stabbing queries
- Interval tree
- R-tree (spatial indexing) (concept)

-- Motion / Kinetic (research) --

- Kinetic data structures (concept)
- Dynamic closest pair (concept)
- Dynamic convex hull (research)

====================================================================
G. ADVANCED ALGEBRA / POLYNOMIAL / EXACT ARITHMETIC (EXPANDED)
====================================================================

-- Polynomial Algorithms --

- FFT (iterative / recursive)
- NTT (iterative / recursive)
- Bluestein FFT (arbitrary length)
- CRT combination for convolution
- Polynomial division (Newton/NTT)
- Polynomial inverse (Newton iteration)
- Polynomial square root (Newton) (advanced)
- Polynomial logarithm (FPS)
- Polynomial exponential (FPS)
- Polynomial power (FPS)
- Multipoint evaluation (segment tree method)
- Multipoint interpolation (segment tree method)
- Kitamasa algorithm (linear recurrence)
- Berlekamp–Massey (linear recurrence)
- Bostan–Mori algorithm (advanced generating functions) (research-leaning)

-- Exact Integer / Modular Arithmetic Acceleration --

- Barrett reduction
- Montgomery multiplication
- Fast modular multiply (128-bit)
- CRT for big integer reconstruction
- Garner reconstruction

-- Polynomial Factorization (rare) --

- Berlekamp factorization (finite fields) (rare)
- Cantor–Zassenhaus (finite fields) (rare)
- Hensel lifting (rare)

====================================================================
H. ADVANCED COMBINATORICS / ENUMERATION (MORE SPECIALIZED)
====================================================================

- Pólya enumeration theorem (implementation-heavy)
- Burnside lemma counting
- Inclusion–exclusion on constraints (high-dimensional)
- Principle of DP-by-subset-size layering
- Subset convolution counting
- Fast zeta/mobius transforms for combinatorics
- Matrix-tree theorem (Kirchhoff)
- BEST theorem for Euler tours counting (advanced)
- Counting perfect matchings in bipartite via determinant (advanced) (rare)
- Permanent approximation (research; rare)

====================================================================
I. ADVANCED NUMERICAL / OPTIMIZATION (THEORY-LEANING)
====================================================================

- Linear programming in fixed dimension (Seidel randomized) (advanced)
- Simplex method (concept)
- Interior point methods (concept)
- Min-cost circulation with potentials
- Submodular function minimization (research)
- Convex optimization (conceptual)
- Gradient methods (conceptual)

====================================================================
J. CRYPTO / HASH / FINGERPRINTING (CP-USEFUL TRICKS)
====================================================================

- Polynomial rolling hash
- Double hashing
- SplitMix64 hash (anti-hack)
- Universal hashing (concept)
- Randomized fingerprinting for equality (e.g., polynomial identity) (advanced trick)
- Rabin–Karp as fingerprinting
- Hash-based cycle detection

# End of Part 11

# 🧠 ALGORITHMS MASTER LIST — PART 12
# Hyper-Granular Expansion: Micro-Variants, Reductions, Modeling Tricks, Rare Theoretical Tools

====================================================================
A. GRAPH REDUCTION / MODELING ALGORITHMS
====================================================================

- Node-splitting for vertex capacity
- Edge splitting for transformation modeling
- Time-expanded graph construction
- Multi-layer graph construction
- Parity-state graph modeling
- Color-state layered graph
- Bitmask-state layered graph
- Product graph construction
- Dual graph construction (planar)
- Complement graph traversal trick
- Reweighting via Johnson potentials
- Flow reduction for assignment
- Flow reduction for closure problem
- Matching reduction for path cover
- 2-SAT implication graph modeling
- Difference constraints → Bellman-Ford
- Circulation modeling with super source/sink
- Binary lifting modeling for jump queries
- Euler tour flattening modeling
- Virtual tree modeling for subset queries
- Coordinate compression modeling
- Discretization of continuous domain
- Prefix sum modeling for subarray sums
- Difference array modeling for range updates
- Convex hull trick modeling for DP
- Matrix exponentiation modeling for recurrence
- Automaton modeling for pattern constraints
- Digit DP modeling for numeric constraints
- Inclusion–exclusion modeling for forbidden states
- Meet-in-the-middle modeling for exponential split
- Bitmask compression modeling
- Slope trick modeling (convex DP)
- Lagrangian relaxation modeling (Alien trick)
- Parametric search modeling
- Reduction to bipartite matching
- Reduction to max flow
- Reduction to min cut
- Reduction to MST
- Reduction to shortest path
- Reduction to 2-SAT
- Reduction to linear algebra (Kirchhoff / XOR basis)

====================================================================
B. ADVANCED SEARCH / STATE SPACE ALGORITHMS
====================================================================

- BFS with state compression
- BFS with pruning via visited hash
- BFS with heuristic ordering
- Bidirectional BFS
- Iterative deepening DFS (IDDFS)
- Iterative deepening A* (IDA*)
- A* with admissible heuristic
- Beam search (heuristic)
- Best-first search
- Uniform cost search
- Branch and bound with priority queue
- State hashing with Zobrist hash
- Transposition table (game search)
- Cycle detection in implicit state graph
- Floyd cycle detection (tortoise-hare)
- Brent cycle detection
- BFS on bitmask graph
- BFS on grid with dynamic obstacles
- BFS with teleport edges, modeling
- BFS with time dimension
- DFS with pruning bounds
- Backtracking with constraint propagation
- Backtracking with forward checking
- DPLL SAT search
- Alpha-beta pruning
- Negamax framework
- Expectimax (probabilistic search)

====================================================================
C. ADVANCED BITWISE / LOW-LEVEL ALGORITHMIC TRICKS
====================================================================

- Fast popcount via builtin
- Parity via xor folding
- Bit reversal (for FFT)
- Count trailing zeros
- Count leading zeros
- Extract lowest set bit (x & -x)
- Enumerate subsets (sub = (sub-1)&mask)
- Enumerate supermasks
- Bitmask DP with popcount layering
- Precompute bitmask transitions
- XOR basis insertion
- XOR basis maximize query
- XOR basis count combinations
- Gray code generation
- Bit DP on binary representation
- Subset DP with bitsets
- Bit-parallel DP (e.g., bitset LCS optimization)

====================================================================
D. ADVANCED RANGE / QUERY MICRO-VARIANTS
====================================================================

- Persistent segment tree for k-th order statistics
- Persistent segment tree for version rollback
- Rollback DSU for offline queries
- Segment tree with lazy propagation for range assign
- Segment tree for range chmin/chmax (beats)
- Merge sort tree with binary search
- Wavelet tree with dynamic queries (advanced)
- Fenwick tree for inversion counting
- Fenwick tree for offline rectangle sum
- Sparse table for idempotent ops
- Disjoint sparse table
- RMQ via Cartesian tree
- Sliding window minimum via deque
- Monotonic stack for NGE
- Largest rectangle in histogram (stack)
- Trapping rain water (two pointers/stack)
- Mo’s algorithm with Hilbert order
- Mo’s algorithm on tree
- CDQ divide-and-conquer dominance
- Parallel binary search with DSU

====================================================================
E. ADVANCED PROBABILITY / STOCHASTIC ALGORITHMS
====================================================================

- Expected value DP via linear equations
- Absorbing Markov chain solve
- Gambler’s ruin probability
- Random walk hitting probability
- Monte Carlo simulation
- Randomized rounding
- Simulated annealing schedule
- Genetic algorithm (selection/crossover)
- Local search with restart
- Probabilistic primality (Miller–Rabin)
- Randomized min cut (Karger)
- Randomized incremental Delaunay
- Reservoir sampling (k)
- Weighted reservoir sampling
- Bloom filter insertion/query
- Count-min sketch query
- HyperLogLog cardinality estimate

====================================================================
F. ADVANCED GAME THEORY MICRO-VARIANTS
====================================================================

- Grundy computation via mex set
- Grundy memoization DP
- Game on tree (postorder Grundy)
- Game on graph with cycle detection
- Nim with move restrictions
- Misère Nim special-case handling
- Wythoff pair detection
- Kayles DP recurrence
- Turning-toads DP
- Retrograde analysis on graph
- Alpha-beta pruning optimization
- Transposition table usage
- Zobrist hashing for board state

====================================================================
G. ADVANCED ALGEBRAIC MODELING TRICKS
====================================================================

- Linear recurrence via matrix exponentiation
- Linear recurrence via Kitamasa
- Berlekamp–Massey recurrence detection
- Lagrange interpolation mod prime
- Fast power series inversion
- Formal power series exp/log
- Subset convolution
- Fast Walsh–Hadamard transform
- Min-plus convolution
- Zeta transform
- Möbius inversion
- Dirichlet convolution
- Multiplicative function sieve
- Chinese remainder merging
- Garner reconstruction
- Montgomery multiplication
- Barrett reduction
- Tonelli–Shanks sqrt mod p
- Baby-step giant-step discrete log
- Pollard Rho factorization

====================================================================
H. ADVANCED GEOMETRY MICRO-VARIANTS
====================================================================

- Orientation test with long long
- Segment intersection collinearity case
- Line projection formula
- Closest pair strip merge logic
- Convex hull collinear handling
- Rotating calipers antipodal pairs
- Smallest enclosing circle randomized
- Half-plane intersection sorting by angle
- Minkowski sum merge hulls
- KD-tree splitting heuristics
- Range tree build
- Rectangle union via event sweep
- Skyline via heap sweep
- Polygon triangulation (ear clipping)
- Delaunay triangulation incremental

====================================================================
I. ADVANCED PARADIGM-CROSSING TECHNIQUES
====================================================================

- Hybrid DP + segment tree
- Hybrid DP + convex hull trick
- Hybrid DP + bitset
- Hybrid flow + shortest path
- Hybrid matching + DP
- Hybrid inclusion–exclusion + DP
- Hybrid binary search + DP
- Hybrid divide-and-conquer + BIT
- Hybrid offline + rollback DSU
- Hybrid tree decomposition + DP
- Hybrid automaton + DP
- Hybrid matrix exponentiation + DP
- Hybrid meet-in-the-middle + pruning
- Hybrid sweep line + segment tree
- Hybrid geometry + binary search

====================================================================
J. COMPLEXITY / PERFORMANCE TECHNIQUES (ALGORITHM-LEVEL)
====================================================================

- Amortized analysis (potential method)
- Lazy propagation amortization
- Small-to-large merging amortization
- Union-by-rank + path compression amortization
- Randomized balancing amortization
- Cache-friendly loop ordering
- Bitset acceleration for O(n^2/word)
- Precomputation trade-offs
- Memory compression DP
- Loop unrolling (micro-optimization)
- Fast I/O buffering
- Avoid recursion stack overflow (iterative rewrite)
- Avoid overflow via 128-bit arithmetic
- Early pruning bounds
- Meet-in-the-middle to cut 2^n → 2^(n/2)
- Replace map with vector + compression
- Use static arrays over dynamic allocation
- Replace recursion with explicit stack
- Inline small functions

====================================================================
K. STRUCTURAL COMPLETENESS NOTES
====================================================================

- Every graph problem reducible to:
  - Traversal
  - Shortest path
  - Flow
  - Matching
  - DP on DAG
- Every counting problem reducible to:
  - DP
  - Inclusion–exclusion
  - Generating functions
  - Transform convolution
- Every optimization problem reducible to:
  - Greedy
  - DP
  - Flow / cut
  - Convex optimization trick
  - Parametric search

# End of Part 12

