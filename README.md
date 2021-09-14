

## Topics

### Slide 1: [Introduction](https://raw.githubusercontent.com/3N4N/BUETUGCSE453/master/slides/01_Introduction.pdf)

- Physical Storage Media
  - Volatile
  - Non-volatile
- Storage hierarchy
- DBMS system architecture
  - Main-memory
  - Disk-based
- Parallel DB system architecture
  - Tree-like / Fat-tree topology
- Parallel systems
  - coarse-grain parallel machine
  - massively parallel or fine grain parallel machine
- Performance measures
  - throughput
  - response time
- Speed up
- Scale up
- Amdahl's law
- Gustafson's law
- Factors limiting Speedup and Scaleup
  - Inference
  - Skew
- Interconnected network architectures
  - Bus
  - Mesh
  - Hypercube
  - Tree-like / Fat-tree topology
- Parallel DB architecture
  - Shared memory
  - Shared disk (SAN)
  - Shared nothing
  - Hierarchical



## Questions and Answers

### Slide 1: [Answers](https://raw.githubusercontent.com/3N4N/BUETUGCSE453/master/cw-notes/1605023_CSE453_WEEK1.pdf)

- **1-1**:

  Explain the implications of storage to MMDBMS and Disk-based DBMS.

- **2-1**:

  A server system has 1 node (small system) and elapsed to solve problem P is 10ms.

  1. The number of node has been increased to 2. The time to solve P is 5ms
  2. The number of node has been increased to 3. The time to solve P is 4ms
  3. The number of node has been increased to 4. The time to solve P is 3ms

  Find the type of speedup graph for the above system and explain

- **2-2**:

  A server system has 1 node (small system) and elapsed to solve problem P is
  10ms.

    1. The number of node has been increased to 4. The size of the problem = 4p,
       elapsed time is 40ms
    2. The number of node has been increased to 8. The size of the problem = 8p,
       elapsed time is 80ms

    Find type of scale up graph for the above system and explain

- **2-3**:

  Explain speedup as per Amdahl’s law for the following cases:

  Case 1: Full fraction of T can be executed in parallel (p =1)
  Case 2: No fraction of T can be executed in parallel (p =0)
  Case 3: A fraction of T can be executed in parallel (0 < p <1)

- **2-4**:

  Explain scaleup as per Gustafson’s law for the following cases:

  Case 1: Full fraction of T can be executed in parallel (p =1)
  Case 2: No fraction of T can be executed in parallel (p =0)

- **3-1**:

  Discuss comparative advantages and Disadvantages of BUS, Mesh, Hypercube, and
  Tree topology.

- **3-2**:

  Show the hierarchical architecture with top level be a shared-disk
  system and each node of the system being a shared-memory system.
