# hpc_assignment-3

## Binary Search Tree (BST) Test
This repository features code designed to evaluate the concurrent behavior of a Binary Search Tree (BST) using multithreading. It enables assessment of the BST's performance with multiple threads concurrently executing operations such as insertion, deletion, and search within the tree structure.

### Overview
The code consists of the following components:

#### ConBST_Test.java:
 1. Serves as the main orchestrator for testing the BST with multiple threads.
 2. Accepts command-line arguments for thread count, initial tree size, and workload distribution.
 3. Spawns threads to perform operations like contains, insert, and delete based on defined workload percentages.
 4. Records and reports the throughput of these operations.

#### ThreadID.java: 
 A utility class used to obtain unique thread identifiers.
 
#### Counter.java:
 A simple counter utility class used to count thread operations.
 
#### Running the Test:
 Execute the program by compiling and running ConBST_Test.java. Command-line arguments specify the number of threads, initial tree size, and workload (expressed as a percentage of "C-I-D"). 
 Where:
 "C" -> Contains
 "I" -> Inserts
 "D" -> Deletes
 
##### Example command to run the program:

'''
java ConBST_Test <num_threads> <prefill_size> <workload>
'''

Replace <num_threads>, <prefill_size>, and <workload> with appropriate values.

#### Testing Approach:
 1. Initializes a Binary Search Tree (BST) with a specified number of nodes.
 2. Prefills the tree with random values.
 3. Utilizes multiple threads to concurrently perform operations based on defined workload percentages.
 4. Measures and reports the throughput of these operations.

#### Output Metrics:
The program generates reports containing:

 1. num_threads: The number of threads involved in testing.
 2. totalOps: The overall count of operations executed.
 3. throughput: The throughput, expressed in operations per second (ops/s).


Example Output
BST_Test:num_threads:<num_threads>:totalOps::throughput: ops/s

Conclusion
This code facilitates concurrent testing of a binary search tree (BST) to evaluate its behavior with various workloads and analyze its performance in multi-threaded scenarios. Users can customize the number of threads, prefill size, and workload to assess the BST's suitability for specific use cases.
