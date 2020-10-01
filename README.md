# sorting-algorithms

This project has the objective of studying sorting algorithms and C++.

It is a simple program that prompts the user to input the number of elements that will be stored in a dynamically allocated array, to input the way that it is ordered (i.e. Crescent, Decrescent or Random) and to input the sorting algorithm.

Finally the program outputs the time consumed just to sort the array. Avery useful project.

## Currently included sorting algorithms:
- [bubble sort](https://en.wikipedia.org/wiki/Bubble_sort)


Bubble sort algorithm starts by comparing the first two elements of an array and swapping if necessary, i.e., if you want to sort the elements of array in ascending order and if the first element is greater than second then, you need to swap the elements but, if the first element is smaller than second, you mustn't swap the element. Then, again second and third elements are compared and swapped if it is necessary and this process go on until last and second last element is compared and swapped. This completes the first step of bubble sort.

If there are n elements to be sorted then, the process mentioned above should be repeated n-1 times to get required result. But, for better performance, in second step, last and second last elements are not compared because, the proper element is automatically placed at last after first step. Similarly, in third step, last and second last and second last and third last elements are not compared and so on.

- [insertion sort](https://en.wikipedia.org/wiki/Insertion_sort)

A simple sorting algorithm that builds the sorted array one element at a time, creating a sorted list every iteration before adding a new element.

- [selection sort](https://en.wikipedia.org/wiki/Selection_sort)

Another simple in-place comparison sort, creating a sorted list every iteration and then finding  the smallest (or largest, depending on sorting order) element in the unsorted sublist to insert in the sorted iteration.
Selection sort algorithm starts by compairing first two elements of an array and swapping if necessary, i.e., if you want to sort the elements of array in ascending order and if the first element is greater than second then, you need to swap the elements but, if the first element is smaller than second, leave the elements as it is. Then, again first element and third element are compared and swapped if necessary. This process goes on until first and last element of an array is compared. This completes the first step of selection sort.

If there are n elements to be sorted then, the process mentioned above should be repeated n-1 times to get required result. But, for better performance, in second step, comparison starts from second element because after first step, the required number is automatically placed at the first (i.e, In case of sorting in ascending order, smallest element will be at first and in case of sorting in descending order, largest element will be at first.). Similarly, in third step, comparison starts from third element and so on.


- [quicksort](https://en.wikipedia.org/wiki/Quicksort)

Quicksort is an algorithm used to quickly sort items within an array no matter how big the array is. It is quite scalable and works relatively well for small and large data sets, and is easy to implement with little time complexity. It does this through a divide-and-conquer method that divides a single large array into two smaller ones and then repeats this process for all created arrays until the sort is complete.

The quicksort algorithm is performed as follows:

A pivot point is chosen from the array.

The array is reordered so that all values smaller than the pivot are moved before it and all values larger than the pivot are moved after it, with values equaling the pivot going either way. When this is done, the pivot is in its final position.

The above step is repeated for each subarray of smaller values as well as done separately for the subarray with greater values.
This is repeated until the entire array is sorted.

- [Pigeonhole Sort](https://en.wikipedia.org/wiki/Pigeonhole_sort)

Pigeonhole sorting is a sorting algorithm that is suitable for sorting lists of elements where the number of elements (n) and the length of the range of possible key values (N) are approximately the same. It requires O(n + N) time. It is similar to counting sort, but differs in that it "moves items twice: once to the bucket array and again to the final destination [whereas] counting sort builds an auxiliary array then uses the array to compute each item's final destination and move the item there."

The pigeonhole algorithm works as follows:

    1.Given an array of values to be sorted, set up an auxiliary array of initially empty "pigeonholes," one pigeonhole for each key through the range of the original array.
    2.Going over the original array, put each value into the pigeonhole corresponding to its key, such that each pigeonhole eventually contains a list of all values with that key.
    3.Iterate over the pigeonhole array in order, and put elements from non-empty pigeonholes back into the original array.


- [radixsort](https://en.wikipedia.org/wiki/Radix_sort)

Radix sort is a non-comparative integer sorting algorithm that sorts data with integer keys by grouping keys by the individual digits which share the same significant position and value.  
The lower bound for Comparison based sorting algorithm (Merge Sort, Heap Sort, Quick-Sort .. etc) is Ω(nLogn), i.e., they cannot do better than nLogn.
Counting sort is a linear time sorting algorithm that sort in O(n+k) time when elements are in range from 1 to k.

What if the elements are in range from 1 to n2?
We can’t use counting sort because counting sort will take O(n2) which is worse than comparison based sorting algorithms. Can we sort such an array in linear time?
Radix Sort is the answer. The idea of Radix Sort is to do digit by digit sort starting from least significant digit to most significant digit. Radix sort uses counting sort as a subroutine to sort.

The Radix Sort Algorithm
1) Do following for each digit i where i varies from least significant digit to the most significant digit.
………….a) Sort input array using counting sort (or any stable sort) according to the i’th digit.

Example:
Original, unsorted list:

170, 45, 75, 90, 802, 24, 2, 66
Sorting by least significant digit (1s place) gives: [*Notice that we keep 802 before 2, because 802 occurred before 2 in the original list, and similarly for pairs 170 & 90 and 45 & 75.]
170, 90, 802, 2, 24, 45, 75, 66




Sorting by next digit (10s place) gives: [*Notice that 802 again comes before 2 as 802 comes before 2 in the previous list.]

802, 2, 24, 45, 66, 170, 75, 90
Sorting by most significant digit (100s place) gives:

2, 24, 45, 66, 75, 90, 170, 802

- [MergeSort](https://en.wikipedia.org/wiki/Merge_sort)

A divide and conquer based Sorting technique, preserves the input order of equal elements in the sorted output(stable).
using a divide and conquer strategy as a way to improve the performance of sorting algorithms. The first algorithm we will study is the merge sort. Merge sort is a recursive algorithm that continually splits a list in half. If the list is empty or has one item, it is sorted by definition (the base case). If the list has more than one item, we split the list and recursively invoke a merge sort on both halves. Once the two halves are sorted, the fundamental operation, called a merge, is performed. Merging is the process of taking two smaller sorted lists and combining them together into a single, sorted, new list.

- [Heapsort](https://en.wikipedia.org/wiki/Heapsort)

A comparison-based sorting algorithm that divides its input into a sorted and an unsorted region, and it iteratively shrinks the unsorted region by extracting the largest element and moving that to the sorted region. The improvement consists of the use of a heap data structure rather than a linear-time search to find the maximum
Heap Sort is a popular and efficient sorting algorithm in computer programming. Learning how to write the heap sort algorithm requires knowledge of two types of data structures - arrays and trees.

The initial set of numbers that we want to sort is stored in an array e.g. [10, 3, 76, 34, 23, 32] and after sorting, we get a sorted array [3,10,23,32,34,76]

Heap sort works by visualizing the elements of the array as a special kind of complete binary tree called heap.
