# Parallel-Computing-System-Recs

# Parallel Sum Reduction Algorithm in OpenMP
In this algorithm, the program is implemented such that rather than a simple linear summation of array values, the summation is done as in the below algorithm:

Step 1: A “slider” value is calculated as (veryLongArraySize/2). Step 2: An array value at (i)th location is added with an array value of (i+slider)th location and stored back to (i)th location. Now half the array values are processed stored. So now this half should be processed again. Step 3: Reduce array size, veryLongArraySize, by 2 and continue with step 1. If array size is 1 go to step 4. Step 4: Value at veryLongArray[0] gives the sum of the very large array values.

This algorithm was implemented in OpenMP framework. This program shows the results for normal linear summation, parallel sum reduction algorithm without any OpenMP constructs and parallel sum reduction algorithm with parallel for construct.

It can be observed from the results that parallel sum reduction algorithm is not suited for OpenMP framework. The results shows that the algorithm takes more time than serial summation.

For OpenMP framework and very large array sizes, above 2^30 array size, Parallel For construct is best.
