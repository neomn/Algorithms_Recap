# Sorting Algorithms
This is a list of common sorting algorithms with a brief description of how they work.
- Bubble Sort
- Insertion Sort
- Selection Sort
- Merge Sort
- Quicksort
- Heapsort
- Counting Sort
- Radix Sort
- Bucket Sort
- Shellsort

## Bubble Sort
![bubble_sort](./assets/bubble_sort.gif)
Bubble sort repeatedly steps through a list, compares adjacent elements, and swaps them if they are in the wrong order.
+ Worst case performance: O(n^2)
+ Best case performance: O(n)
+ Average performance: O(n^2)


## Insertion Sort
![insertion_sort](./assets/insertion_sort.gif)
 Insertion sort builds a sorted list by inserting each element into its correct position in the final sorted list.
+ Worst case performance: O(n^2)
+ Best case performance: O(n)
+ Average performance: O(n^2)

## Selection Sort
![selection_sort](./assets/selection_sort.gif)
Selection sort finds the minimum element in the unsorted list, swaps it with the first element, and repeats for the remainder of the list.
+ Worst case performance: O(n^2)
+ Best case performance: O(n^2)
+ Average performance: O(n^2)

## Merge Sort
![merge_sort](./assets/merge_sort.png)
Merge sort recursively divides a list into sublists until each sublist has 1 element, then merges the sublists back together in sorted order. Uses divide-and-conquer.
+ Worst case performance: O(n log n)
+ Best case performance: O(n log n)
+ Average performance: O(n log n)

## Quicksort
![quick_sort](./assets/quick_sort.gif)

Quick Sort is a widely used sorting algorithm that follows the divide-and-conquer strategy to sort an array or list of elements.
1- Choose a Pivot Element: The first step in Quick Sort is to select a pivot element from the array. The pivot element is used as a reference
    point to partition the array.
2- Partition the Array: Rearrange the elements in the array such that all elements less than the pivot are on the left side of the pivot,
    and all elements greater than the pivot are on the right side. The pivot itself is in its final sorted position. 
    This process is called "partitioning."
3- Recursively Sort Sub-arrays: After partitioning, you have two sub-arrays: one containing elements less than the pivot and one containing 
    elements greater than the pivot. Recursively apply the Quick Sort algorithm to these sub-arrays.
4- Combine Sorted Sub-arrays: Once the sub-arrays are sorted, combine them with the pivot element in the middle to form the final 
    sorted array. The pivot, by definition, is already in its correct position.
5- Base Case: The base case of the recursion is when an array contains 0 or 1 element. In such cases, the array is considered sorted, 
    and no further action is needed.
6- Repeat: Continue this process of selecting a pivot, partitioning, and sorting sub-arrays recursively until the entire array is sorted.
    The key to the efficiency of Quick Sort lies in the choice of the pivot and the partitioning process. An efficient choice
    of pivot (e.g., the middle element or a randomly selected element) can lead to a balanced partition, which ensures good performance in most cases.

    Quick Sort is known for its average-case time complexity of O(n log n), making it one of the fastest general-purpose sorting algorithms. However, 
    in the worst case (e.g., when the pivot is always the smallest or largest element), it can degrade to O(n^2) time complexity.
    
+ Worst case performance: O(n^2)
+ Best case performance: O(n log n)
+ Average performance: O(n log n)

## Heapsort
![heap_sort](./assets/heap_sort.gif)
Heapsort converts the list into a max heap, where each node is larger than its children. Extracts each element in descending order by swapping the root with the last leaf.
+ Worst case performance: O(n log n)
+ Best case performance: O(n log n)
+ Average performance: O(n log n)

## Counting Sort
![counting_sort](./assets/counting_sort.gif)
Counting sort counts the number of elements with each distinct key value, then uses these counts to position elements in the output list. Works for integers only.
+ Worst case performance: O(n+k)
+ Best case performance: O(n+k)
+ Average performance: O(n+k)

## Radix Sort
![radix_sort](./assets/radix_sort.gif)
Radix sort sorts integers by digit (least to most significant) using counting sort on each digit.
+ Worst case performance: O(nk)
+ Best case performance: O(nk)
+ Average performance: O(nk)

## Bucket Sort
![bucket_sort](./assets/bucket_sort.gif)
Bucket sort divides elements into "buckets" based on value ranges, sorts each bucket, and concatenates final output.
+ Worst case performance: O(n^2)
+ Best case performance: O(n+k)
+ Average performance: O(n+k)

## Shellsort
![shell_sort](./assets/shell_sort.gif)
Shellsort is an in-place comparison sort that improves on insertion sort by comparing elements separated by a "gap." The gap is reduced over iterations.
+ Worst case performance: O(n^2)
+ Best case performance: O(n log n)
+ Average performance: depends on gap sequence
