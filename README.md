# HPC Assignment - 3

## Binary Search Tree (BST) Test

This repository features code designed to evaluate the concurrent behavior of a Binary Search Tree (BST) using multithreading. It enables assessment of the BST's performance with multiple 
threads concurrently executing operations such as insertion, deletion, and search within the tree structure.

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

~~~
java ConBST_Test <num_threads> <prefill_size> <workload>
~~~

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

#### Example Output:

 BST_Test:num_threads:<num_threads>:totalOps:<totalOps>:throughput: ops/s


#### Conclusion

 This code offers a flexible means of concurrently testing a binary search tree's behavior, enabling users to customize thread count, initial tree size, and workload distribution for tailored 
 performance assessments in multi-threaded scenarios.

 ### Graphs plotted against throughput by varying no.of threads for different locks

 ##### TAS Lock:

 ![image](https://github.com/ganeshvarmapotturi/HPC_Assignment-3/assets/69681358/2e2469ac-05a7-4722-8108-41198b0f63d7)

 #### A Lock:

![image](https://github.com/ganeshvarmapotturi/HPC_Assignment-3/assets/69681358/55f11d91-26e7-4de2-a625-d9428774ba76)

 #### TTAS Lock:

![image](https://github.com/ganeshvarmapotturi/HPC_Assignment-3/assets/69681358/bd1444fd-88b1-41ba-974b-c2bf9f92ee94)

 #### MCS Lock:

![image](https://github.com/ganeshvarmapotturi/HPC_Assignment-3/assets/69681358/7995d7e6-73db-414e-b283-52a9718e844b)

 #### CLH Lock:

 ![image](https://github.com/ganeshvarmapotturi/HPC_Assignment-3/assets/69681358/17716569-0aef-45a7-a79a-1b9d52bfd9df)

 #### TTAS With Backoff Lock

![image](https://github.com/ganeshvarmapotturi/HPC_Assignment-3/assets/69681358/4d764a75-2ce8-4bfd-9bb9-4d6c563d23a9)


