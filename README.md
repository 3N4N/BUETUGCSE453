# CSE453: High Performance Database System

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
  - Shared disk : SAN, fault tolerance
  - Shared nothing
  - Hierarchical
  - Non-Uniform Memory Architecture (NUMA)
  - Remote Direct Memory Access (RDMA)


### Slide 2: [Parallel and Distributed Architecture](https://raw.githubusercontent.com/3N4N/BUETUGCSE453/master/slides/01_Introduction.pdf)

- IO parallelism
  - Horizontal partitioning
  - Vertical partitioning
- Partitioning techniques
  - Round robin
  - Hash partitioning
  - Range partitioning
- Types of skew
  - Data-distributed skew
    - Attribute-value skew
  - Partition skew
  - Execution skew
- Balanced range-partitioning vectors
- Static vs Dynamic partitioning
- Histograms
  - Equi-width
  - Equi-depth


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

  1. Full fraction of T can be executed in parallel (p =1)
  2. No fraction of T can be executed in parallel (p =0)
  3. A fraction of T can be executed in parallel (0 < p <1)

- **2-4**:

  Explain scaleup as per Gustafson’s law for the following cases:

  1. Full fraction of T can be executed in parallel (p =1)
  2. No fraction of T can be executed in parallel (p =0)

- **3-1**:

  Discuss comparative advantages and Disadvantages of BUS, Mesh, Hypercube, and
  Tree topology.

- **3-2**:

  Show the hierarchical architecture with top level be a shared-disk
  system and each node of the system being a shared-memory system.



### Slide 2: [Answers](https://raw.githubusercontent.com/3N4N/BUETUGCSE453/master/cw-notes/1605023_CSE453_WEEK2.pdf)

- 4-1:

  Explain how tuples will be distributed into the nodes using round-robin
  technique.

- 4-2:

  Explain how tuples will be distributed into the nodes using hash partitioning
  technique using a. NID b. Street, city, district.

- 4-3

  In a data center, Nodes N0…N9 in Rack 1 Nodes N20…N19 in Rack 2 Total nodes
  N=20 Student(Id, name, DOB, street, city, district) The tuples are: T0, T1,
  T2, T3, . . . T399 Id ranges from 202105001 to 202105400

  - Design a partition vector on Id for storage of student relation
  - Find partitions P0, P1, P19.

- 4-4:

  Person(NID, Name, Thana, District, Age), parents(m-NID, f-NID, c-NID, f-age)
  process the query1: SELECT * FROM person r, parents s WHERE r.age = s.f-age

  - Explain how query 1 will be executed using 4 nodes?
  - Comments on speed-up and scale-up for the system

- 5-1:

  Explain the performance of Round robin partitioning technique for

  - Scanning the entire relation
  - Point query
  - Range query

- 5-2:

  Explain the performance of hash partitioning technique for

  - Scanning the entire relation
  - Point query
  - Range query

- 5-3:

  Explain the performance of range partitioning technique for

  - Scanning the entire relation
  - Point query
  - Range query

- 6-1:

  Explain the various reasons and types of skews in
  - Hash partitioning
  - Range partitioning

- 6-2:

  - What is the type of the given histogram?
  - Define an approximate partition vector using the histogram for a parallel
    system with nodes N0, N1, N2 and N3.
  - Draw the approximate histogram of your partition vector.
