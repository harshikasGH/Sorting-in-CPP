Sorting in C++

Aim  
To study and implement **Sorting algorithms in C++**, including **Bubble Sort, Selection Sort, Insertion Sort, Merge Sort, Quick Sort, Heap Sort, and Bucket Sort**, and to compare their efficiency, time complexity, and use cases.

Theory  
Sorting is the process of arranging data in a particular order (ascending or descending). Efficient sorting is crucial for optimizing search algorithms and data processing.

Characteristics of Sorting Algorithms  
- **Stability**: Maintains the relative order of equal elements.  
- **In-place vs. Out-of-place**: Whether extra memory is required.  
- **Time Complexity**: Efficiency in best, worst, and average cases.  
- **Comparison-based vs. Non-comparison-based**: Most classical algorithms are comparison-based.  

Types of Sorting Algorithms  
1. **Bubble Sort** → Repeatedly swaps adjacent elements if they are in the wrong order.  
2. **Selection Sort** → Repeatedly selects the minimum element and places it at the correct position.  
3. **Insertion Sort** → Builds the sorted array one element at a time by inserting into the correct position.  
4. **Merge Sort** → Divide-and-conquer algorithm that splits the array and merges sorted halves.  
5. **Quick Sort** → Divide-and-conquer algorithm that partitions around a pivot.  
6. **Heap Sort** → Builds a max heap and repeatedly extracts the maximum element.  
7. **Bucket Sort** → Distributes elements into buckets, sorts each bucket individually, and then concatenates them. Works best when input is uniformly distributed.  

Algorithms  
Bubble Sort  
1. Start  
2. Input array of size `n`.  
3. Repeat for `i = 0` to `n-1`:  
   - For `j = 0` to `n-i-2`:  
     - If `arr[j] > arr[j+1]`, swap them.  
4. End  

 Selection Sort  
1. Start  
2. Input array of size `n`.  
3. Repeat for `i = 0` to `n-1`:  
   - Set `minIndex = i`.  
   - For `j = i+1` to `n-1`:  
     - If `arr[j] < arr[minIndex]`, update `minIndex = j`.  
   - Swap `arr[i]` and `arr[minIndex]`.  
4. End  

Insertion Sort  
1. Start  
2. Input array of size `n`.  
3. Repeat for `i = 1` to `n-1`:  
   - Set `key = arr[i]`, `j = i-1`.  
   - While `j >= 0` and `arr[j] > key`:  
     - Shift `arr[j]` to `arr[j+1]`.  
     - Decrement `j`.  
   - Insert `key` at `arr[j+1]`.  
4. End  

Merge Sort  
1. Start  
2. If array has more than one element:  
   - Divide array into two halves.  
   - Recursively sort both halves.  
   - Merge the two sorted halves.  
3. End  

Quick Sort  
1. Start  
2. If array has more than one element:  
   - Choose a pivot element.  
   - Partition array into two subarrays:  
     - Left: elements smaller than pivot.  
     - Right: elements greater than pivot.  
   - Recursively apply quick sort on left and right subarrays.  
3. End  

Heap Sort  
1. Start  
2. Build a max heap from the array.  
3. Repeat until heap size > 1:  
   - Swap root (max element) with last element.  
   - Reduce heap size by 1.  
   - Heapify the root.  
4. End  

Bucket Sort  
1. Start  
2. Input array of size `n`.  
3. Create `k` empty buckets.  
4. Distribute elements into buckets based on a mapping function (e.g., `index = value * k`).  
5. Sort each bucket individually (using insertion sort or another algorithm).  
6. Concatenate all buckets in order to form the sorted array.  
7. End  

Time Complexity Comparison  

| Algorithm       | Best Case | Worst Case | Average Case | Space Complexity | Stable |
|-----------------|-----------|------------|--------------|------------------|--------|
| Bubble Sort     | O(n)      | O(n²)      | O(n²)        | O(1)             | Yes    |
| Selection Sort  | O(n²)     | O(n²)      | O(n²)        | O(1)             | No     |
| Insertion Sort  | O(n)      | O(n²)      | O(n²)        | O(1)             | Yes    |
| Merge Sort      | O(n log n)| O(n log n) | O(n log n)   | O(n)             | Yes    |
| Quick Sort      | O(n log n)| O(n²)      | O(n log n)   | O(log n)         | No     |
| Heap Sort       | O(n log n)| O(n log n) | O(n log n)   | O(1)             | No     |
| Bucket Sort     | O(n+k)    | O(n²)      | O(n+k)       | O(n+k)           | Yes    |

Applications  
- **Bubble Sort** → Educational purposes, small datasets.  
- **Selection Sort** → When memory writes are costly.  
- **Insertion Sort** → Small or nearly sorted datasets.  
- **Merge Sort** → Large datasets, external sorting, stable sorting.  
- **Quick Sort** → General-purpose sorting, efficient in practice.  
- **Heap Sort** → Priority queues, scheduling algorithms.  
- **Bucket Sort** → Uniformly distributed data (e.g., floating-point numbers, percentages).  

Conclusion  
- **Bubble, Selection, and Insertion Sort** are simple but inefficient for large datasets.  
- **Merge Sort and Quick Sort** are efficient divide-and-conquer algorithms widely used in practice.  
- **Heap Sort** is useful when constant space and guaranteed O(n log n) performance are required.  
- **Bucket Sort** is highly efficient for uniformly distributed data, achieving near-linear performance.  
- Mastering sorting algorithms is essential for **data organization, searching optimization, and algorithm design**.
