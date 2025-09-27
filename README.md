# *Divide-and-Conquer Algorithms - Report*

*1. Architecture Notes**

- *Merge Sort*: Uses a reusable buffer and insertion sort for small arrays. Recursion depth is **O(log n)**.
- *Quick Sort*: Randomized pivot, recurses on the smaller partition, iterates on the larger one. Average recursion depth is **O(log n)**.
- *Deterministic Select*: Divides into groups of 5, uses median-of-medians as pivot. Recursion depth is **O(log n)**.
- *Closest Pair*: Divide-and-conquer with a strip array to find pairs near the dividing line. Recursion depth is **O(log n)**.

*2. Recurrence Analysis*

| Algorithm                | Recurrence                               | Θ Complexity     |
|--------------------------|-----------------------------------------|------------------|
| *Merge Sort*             | \( T(n) = 2T(n/2) + O(n) \)             | Θ(n log n)       |
| *Quick Sort (average)*   | \( T(n) = 2T(n/2) + O(n) \)             | Θ(n log n)       |
| *Quick Sort (worst)*     | \( T(n) = T(n-1) + O(n) \)              | Θ(n²)            |
| *Deterministic Select*   | \( T(n) = T(n/5) + T(7n/10) + O(n) \)   | Θ(n)             |
| *Closest Pair*           | \( T(n) = 2T(n/2) + O(n) \)             | Θ(n log n)       |

*3. Summary*

- *MergeSort* and *QuickSort* performed as expected, with *O(n log n)* in average case and *O(n²)* for QuickSort in the worst case.
- *Deterministic Select* consistently ran in **O(n)** time, confirming its theoretical efficiency.
- *Closest Pair* followed its *O(n log n)* time complexity.

*Conclusion*:
The theoretical time complexities were confirmed by measurements, with *Deterministic Select* being the most efficient in terms of time complexity. *MergeSort* and *QuickSort* showed solid performance, but QuickSort had edge cases where performance degraded.
