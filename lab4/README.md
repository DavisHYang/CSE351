## Lab 4 - Caches and Cache-Friendly Code

### Learning Objectives
- Given a provided cache, determine the cache size, block size, and associativity.
- Explain how the different cache parameters impact cache performance.
- Given a set of cache parameters and a task requiring frequent memory accesses, devise a function to complete the task with as few cache misses as possible.
- Given two functions performing the same task in different ways, compare and contrast how each method will perform as a result cache properties.

### Part 1 - Inferring Mystery Cache Geometries
Your job is to complete the 3 functions in `cache-test-skel.c` that have `/* YOUR CODE GOES HERE */` comments in them, which, when linked with one of these cache object files, will determine and then output the (1) block size, (2) cache size, and (3) associativity. You will use the functions above to perform cache accesses and use your observations of which ones hit and miss to determine the parameters of four mystery caches.

- You can assume that all of the caches have sizes that are powers of 2 and use a least recently used (LRU) replacement policy.
- You cannot assume anything else about the cache parameters except what you can infer from the cache size.

### Part 2 - Optimising Matrix Transpose
Your job in Part 2 is to write a function, called `transpose_submit`, that minimizes the number of cache misses across different sized matrices on a simulated cache with parameters s = 5 (index bits), E = 1 (associativity), k = 5 (offset bits)

- Your transpose function may not use recursion or any variant of `malloc`.
- Your transpose function may not modify array A. You may, however, do whatever you want with the contents of array B.
- You are allowed to define at most 12 local variables of type `int` per transpose function. This means 12 variables in scope at once.
- You are permitted to use int arrays, but arrays DO count towards your 12 local `ints`.
- If you choose to use helper functions, you may not have more than 12 local variables on the stack at a time between your helper functions and your top-level transpose function.
- You are not allowed to side-step the previous rule by using any variables of type `long` or by using any bit tricks to store more than one value to a single variable.

Full details at [Lab 4 Overview Page](https://courses.cs.washington.edu/courses/cse351/24sp/labs/lab4.html).
