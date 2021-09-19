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
  - Coarse-grain parallel machine
  - Massively parallel or fine grain parallel machine
- Performance measures
  - Throughput
  - Response time
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


### Slide 2: [Parallel and Distributed Architecture](https://raw.githubusercontent.com/3N4N/BUETUGCSE453/master/slides/02_Parallel-DB-Storage.pdf)

- IO parallelism: 21.2
  - Horizontal partitioning
  - Vertical partitioning
- Partitioning techniques: 21.2.1
  - Round robin
  - Hash partitioning
  - Range partitioning
- Types of skew: 21.3
  - Data-distributed skew
    - Attribute-value skew
    - Partition skew
  - Execution skew
- Balanced range-partitioning vectors: 21.3.1
  - Through sorting and repartitioning
  - Using histogram and virtual partitioning
- Static vs Dynamic partitioning
- Histograms: 16.3.1, 21.3.2
  - Equi-width
  - Equi-depth

### Slide 3: [Parallel and Distributed Architecture](https://raw.githubusercontent.com/3N4N/BUETUGCSE453/master/slides/03_Parallel-DB-Storage.pdf)

- Virtual node partitioning: 21.3.2
- Dynamic repartitioning: 21.3.3
- Tablets: 21.3.3
- Routing of queries
  - Master node
  - Consistent hashing
  - Distributed hash table
- Replication: : 21.4
- Distributed file system: 21.6
- Metadata: 21.6
- Hadoop Distributed File System (HDFS)
- Google File System (GFS)
- Sharding: 26.7.1
- Data Storage Systems vs Databases

### Slide 4: [Parallel Database Query Processing](https://raw.githubusercontent.com/3N4N/BUETUGCSE453/master/slides/04_Parallel-DB_Query-Processing.pdf)

- Parallel query processing
  - Interquery parallelism
  - Intraquery parallelism
    - Intraoperation parallelism
      - Sorting
        - External sorting using sort-merge
        - Parallel sort: 22.2
          - Range-partition sort
          - Parallel external sort-merge
    - Interoperator parallelism
      - Pipeline parallelism
      - Independent parallelism
- Other relational operators: 22.4.1
  - Selection
  - Duplicate elimination
  - Projection

### Slide 5: [Parallel Database Query Processing](https://raw.githubusercontent.com/3N4N/BUETUGCSE453/master/slides/05_Parallel-DB_Query-Processing.pdf)

- Grouping / Aggregation
- Intraoperation Parallelism
  - Parallel join: 22.3
  - Parallel sort: 22.2
- Interoperation Parallelism: 22.5.1
  - Pipeline parallelism
  - Independent parallelism
- Exchange operator model: 22.5.2
- Fragment-and-replicate join: 22.3.2
  - Broadcast join
- Parallel query execution and optimization
- Parallel query plan space: 22.7.1
- Cost of parallel query execution: 22.7.2
  - Resource consumption cost model
  - Response time cost model
- Choosing query plans: 22.7.3
  - Sequential plan
  - Parallel plan

### Slide 6: [Data Analytics](https://raw.githubusercontent.com/3N4N/BUETUGCSE453/master/slides/06_Data-analytics.pdf)

- Use cases: 11
  - Mining: 11.4
  - DSS
- Steps in data analysis: 11
  - ETL: extract-transform-load
  - ELT: extract-load-transform
  - OLAP: Online analytical processing systems: 11.3
- Predictive models
- BI: business intelligence
- Decision support
- FDBS: federated database system: 20.5
- Wrapper
- Mediator systems
- Data warehouse: 11.2
- Multidimensional data: 11.2.2
  - Fact tables
    - Dimension attributes
    - Measure attributes
  - Dimension tables
- Star schema
- Cross tabulation / pivot table
- Data cube
- Hierarchy on dimension attributes
- Cross tabulation with hierarchy: 11.3
  - Drill down
  - Roll up

### Slide 7: [Distributed Database](https://raw.githubusercontent.com/3N4N/BUETUGCSE453/master/slides/07_Distributed-DBMS_Overview.pdf)

- Centralized database
- Distributed database: 20.5
  - Centralized db on a network
  - Distributed DBMS environment
    - Homogeneous distributed DB
    - Heterogeneous distributed DB (= FDBS)
- Transparency
  - Network transparency
  - Replication transparency
  - Fragmentation transparency
    - Horizontal fragmentation: selection
    - Horizontal fragmentation: projection
    - Hybrid
- Reliability through distributed transaction
- Distributed DBMS issues
  - Distributed DB design
  - Query processing
  - Concurrency control
  - Reliability

### Slide 8: [Parallel and Distributed Transaction](https://raw.githubusercontent.com/3N4N/BUETUGCSE453/master/slides/08_Parallel-and-Distributed-Transaction.pdf)

- Required properties of a transaction
  - ACID: 17.2
- Transaction state: 17.4
- Distributed transaction
  - Local
    - Transaction manager
  - Global
    - Transaction coordinator
- System failure modes: 23.1.2
- Commit protocols: 23.2
  - Fail-stop model
    - 2PC
    - 3PC
    - Consensus
- Handling of failures: 23.2.1.2
  - Site failure
  - Coordinator failure
- In-doubt transactions: 23.2.1.3
- Avoid blocking with consensus protocol: 23.2.2
- Persistent Messaging: 23.2.3

### Slide 9: [Concurrency Control](https://raw.githubusercontent.com/3N4N/BUETUGCSE453/master/slides/09_PandD_Transaction-Concurrency.pdf)

- Atomicity: 17.4
- Lock-based protocols: 18.1
  - Pitfalls
- Two-phase locking protocol: 18.1
- Schedule
- Serializability: 17.6
  - Conflict serializability
  - View serializability
- Automatic acquisition of locks
- Single lock manager approach: 23.3.1
  - Advantages
  - Disadvantages
- Concurrency control with replicas: 23.4.2
  - Primary protocol
  - Majority protocol
  - Biased protocol
  - Quorum consensus protocol

### Slide 10: [Deadlock Handling](https://raw.githubusercontent.com/3N4N/BUETUGCSE453/master/slides/10_PandD_Transaction-Processing.pdf)

- Deadlock detection: 18.2
- Wait-for graphs
  - Global
  - Local
- False cycles: 23.3
- Timestamp-based protocol: 18.5
- Slow local clock: 23.3.5

### Slide 11: [Complex Data Types](https://raw.githubusercontent.com/3N4N/BUETUGCSE453/master/slides/11_Complex-Datatype.pdf)

- semi-structured data
- noSQL
  - what, why, and when
  - characteristics
  - data models
    - Key-value
    - Document
    - Column family
    - Graph

### Slide 12: [Complex Data Types](https://raw.githubusercontent.com/3N4N/BUETUGCSE453/master/slides/12_Complex-Datatype.pdf)

- JSON
- XML
- object-relational data model
- object-oriented data model
- inheritance
  - type
  - table
- reference types
  - user generated
  - system generated
- object-relational mapping (ORM)
  - advantages
- information retrieval system
- relevance of a document
  - TF-IDF
  - proximity
  - stop words
- hyperlinks
  - page rank
  - random walk model
- retrieval effectiveness
  - precision
  - recall
- spatial database
  - geographic data
  - geometric data
  - raster data
  - vector data
- spatial queries
  - region queries
  - nearness queries
  - nearest neighbour queries
  - spatial graph queries

### Slide 13: [Performance Tuning](https://raw.githubusercontent.com/3N4N/BUETUGCSE453/master/slides/13_Performance-Tuning.pdf)

- Raid levels
  - 1
  - 5
- Choice of raid level

### Slide 14: [Performance Tuning](https://raw.githubusercontent.com/3N4N/BUETUGCSE453/master/slides/14_Performance-Tuning.pdf)

- tuning DB design
  - schema tuning
    - normalization
    - denormalization
  - index tuning
  - materialized views
  - improving set orientation
  - bulk loads
  - bulk updates
- tuning of transaction
  - read-write contention
  - write-write contention
    - exhaust lock space
    - exhaust log space
- mini-batch transactions
- performance measures
    - Throughput / tps
    - Response time
    - Availability
- performance benchmarks
  - avg.
  - harmonic mean: 25.2.1
- database application classes
  - OLTP: online transaction processing
  - Decision support applications
    - OLAP: online analytical processing
- benchmark suites
  - TPC: Transaction Processing Council
    - TPC-A
    - TPC-B
    - TPC-C
    - TPC-D
    - TPC-H
    - TPC-R
    - TPC-W
- TPC performance measures
  - transactions-per-second with specified constraints on response time
  - transactions-per-second-per-dollar accounts for cost of owning system
- TPC-H and TPC-R Performance measure
  - Power test
  - Throughput test
  - Composite query per hour metric
  - Composite price/performance metric





## Questions and Answers

### Slide 1: [Answers](https://raw.githubusercontent.com/3N4N/BUETUGCSE453/master/cw-notes/1605023_CSE453_WEEK1.pdf)

- 1-1:

  Explain the implications of storage to MMDBMS and Disk-based DBMS.

- 2-1:

  A server system has 1 node (small system) and elapsed to solve problem P is 10ms.

  1. The number of node has been increased to 2. The time to solve P is 5ms
  2. The number of node has been increased to 3. The time to solve P is 4ms
  3. The number of node has been increased to 4. The time to solve P is 3ms

  Find the type of speedup graph for the above system and explain

- 2-2:

  A server system has 1 node (small system) and elapsed to solve problem P is
  10ms.

    1. The number of node has been increased to 4. The size of the problem = 4p,
       elapsed time is 40ms
    2. The number of node has been increased to 8. The size of the problem = 8p,
       elapsed time is 80ms

    Find type of scale up graph for the above system and explain

- 2-3:

  Explain speedup as per Amdahl’s law for the following cases:

  1. Full fraction of T can be executed in parallel (p =1)
  2. No fraction of T can be executed in parallel (p =0)
  3. A fraction of T can be executed in parallel (0 < p <1)

- 2-4:

  Explain scaleup as per Gustafson’s law for the following cases:

  1. Full fraction of T can be executed in parallel (p =1)
  2. No fraction of T can be executed in parallel (p =0)

- 3-1:

  Discuss comparative advantages and Disadvantages of BUS, Mesh, Hypercube, and
  Tree topology.

- 3-2:

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


### Slide 3: [Answers](https://raw.githubusercontent.com/3N4N/BUETUGCSE453/master/cw-notes/1605023_CSE453_WEEK3.pdf)

- 7-1:

  Explain how data distribution skew and execution skew can be handled using
  virtual node partitioning.

- 7-2:

  Explain how a query is executed in parallel storage system with dynamic
  partitioned storage of a relation. The query and the partitioning is on the
  same attribute.

- 8-1:

  Write advantages and disadvantages of replication.

- 8-2:

  Using 64MB block size, how can you store a file named “YourId_HDFS” of size
  10GB in Hadoop file system?


### Slide 7: [Answers](https://raw.githubusercontent.com/3N4N/BUETUGCSE453/master/cw-notes/1605023_CSE453_WEEK7.pdf)

- 19-1:

  Compare homogeneous and heterogeneous DDBMS in terms of storage, querying, and
  transaction.

- 19-2:

  Explain the challenges in data transparency and transactional reliability in
  DDBMS.

### Slide 14: [Answers](https://raw.githubusercontent.com/3N4N/BUETUGCSE453/master/cw-notes/1605023_CSE453_WEEK14.pdf)

- 38-1:

  - Lock space is exhausted in Long update transactions. Explain.
  - Log space is exhausted in Long update transactions. Explain.
  - Recovery time is increased in Long update transactions. Explain

- 39-2:
  - Why TPC-H queries emphasises on aggregation?
  - Why TPC-H prohibits materialized view?
