# Sorting-in-C-Plus-Plus

Aim: To study different sorting techniques in C++ and implement programs to sort elements of an array.

Tools Used: VS Code or Programiz online compiler.

# Theory

# Sorting Algorithms in C++
Sorting algorithms are techniques used to arrange elements of a data structure, such as an array or vector, in a specific order, usually ascending or descending. Sorting is an important operation because it helps in efficient searching, data organization, and analysis. In C++, sorting can be implemented manually through custom algorithms or by using built-in functions like sort() from the <algorithm> header. The efficiency of a sorting algorithm is measured by its time complexity, space complexity, and stability. Choosing the right sorting method depends on the size of the dataset, whether the data is partially sorted, and memory constraints. Properly sorted data improves the performance of other algorithms, especially searching and data processing tasks.

## Types of Sorting
1. **Bubble Sort –** This is a simple sorting algorithm that repeatedly compares adjacent elements and swaps them if they are in the wrong order. The process continues until the array is completely sorted. It is easy to implement but inefficient for large datasets, with a time complexity of O(n²).

2. **Selection Sort –** This algorithm repeatedly selects the minimum (or maximum) element from the unsorted portion of the array and places it in its correct position. It requires fewer swaps than bubble sort but still has a time complexity of O(n²).

3. **Quick Sort –** This is an efficient divide-and-conquer algorithm. It picks a pivot element, partitions the array into two halves (elements less than pivot and greater than pivot), and recursively sorts the halves. Quick sort has an average time complexity of O(n log n), making it much faster for large datasets compared to bubble and selection sort.

# Program-1: Selection Sort
This C++ program demonstrates the Selection Sort algorithm, which is a simple sorting technique used to arrange elements in ascending order. The selectionSort() function works by dividing the array into a sorted and unsorted portion. In each iteration, it selects the minimum element from the unsorted portion and swaps it with the first element of that portion, gradually expanding the sorted portion of the array.

In the main() function, the program takes the size of the array and its elements as input from the user. After calling selectionSort(), it prints the sorted array. Selection sort has a time complexity of O(n²) in all cases and requires constant extra space, making it an in-place sorting algorithm. It is easy to implement but not suitable for very large datasets due to its relatively low efficiency.

--> Algorithm:

1. Start
2. Input the number of elements, size, and the array elements.
3. For each index i from 0 to size - 2:
  --Set minIndex = i.
  --For each index j from i + 1 to size - 1:
    -If arr[j] < arr[minIndex], update minIndex = j.
  --If minIndex != i, swap arr[i] and arr[minIndex].
4. Repeat the process until the entire array is sorted.
5. Print the sorted array.
6. End

# Program-2: Bubble Sort
This C++ program demonstrates the Bubble Sort algorithm, which is a simple sorting method used to arrange elements in ascending order. The bubbleSort() function works by repeatedly comparing adjacent elements of the array and swapping them if they are in the wrong order. Each pass through the array “bubbles” the largest unsorted element to its correct position at the end of the array.

In the main() function, the program takes the size of the array and its elements as input from the user. After calling bubbleSort(), it prints the sorted array. Bubble sort has a time complexity of O(n²) in the worst and average cases and requires constant extra space, making it an in-place sorting algorithm. Although easy to implement, it is inefficient for large datasets and primarily used for educational purposes or small arrays.

--> Algorithm:

1. Start
2. Input the number of elements, size, and the array elements.
3. For each index i from 0 to size - 2:
  --For each index j from 0 to size - i - 2:
    -If arr[j] > arr[j + 1], swap arr[j] and arr[j + 1].
4. Repeat the process until all elements are in ascending order.
5. Print the sorted array.
6. End

# Program-3: Quick Sort
This C++ program demonstrates the Quick Sort algorithm, which is an efficient divide-and-conquer sorting method used to arrange elements in ascending order. The quickSort() function works by selecting a pivot element (here, the last element of the array) and partitioning the array such that all elements less than the pivot are on its left, and all elements greater are on its right. After partitioning, the pivot is in its correct sorted position. The function then recursively sorts the left and right subarrays until the entire array is sorted.

In the main() function, the program takes the size of the array and its elements as input from the user. After calling quickSort(), it prints the sorted array. Quick Sort has an average time complexity of O(n log n) and is highly efficient for large datasets. It is an in-place sorting algorithm but not stable. Quick Sort is widely used in applications requiring fast sorting and optimized performance.

--> Algorihm:

1. Start
2. Input the number of elements, `size`, and the array elements.
3. Call `quickSort(arr, 0, size - 1)`.
4. QuickSort(arr, low, high):

   * If `low < high`:

     1. Select the pivot element (here, `arr[high]`).
     2. Initialize `i = low - 1`.
     3. For each `j` from `low` to `high - 1`:

        * If `arr[j] < pivot`, increment `i` and swap `arr[i]` with `arr[j]`.
     4. Swap `arr[i + 1]` with `arr[high]` to place the pivot in its correct position.
     5. Let `pi = i + 1`.
     6. Recursively call `quickSort(arr, low, pi - 1)` for the left subarray.
     7. Recursively call `quickSort(arr, pi + 1, high)` for the right subarray.
5. Repeat until the array is fully sorted.
6. Print the sorted array.
7. End

# Conclusion
These programs demonstrate the implementation of different sorting algorithms in C++. The Selection Sort program arranges elements by repeatedly selecting the minimum element from the unsorted portion and placing it in its correct position, making it an in-place but less efficient algorithm for large datasets. The Bubble Sort program sorts elements by repeatedly comparing and swapping adjacent elements, “bubbling” the largest unsorted element to its correct position in each pass; it is simple but also inefficient for large arrays. The Quick Sort program uses the divide-and-conquer approach, selecting a pivot, partitioning the array, and recursively sorting subarrays; it is highly efficient with average time complexity of O(n log n) and suitable for large datasets. Together, these programs illustrate how different sorting techniques vary in efficiency, complexity, and suitability, helping understand the choice of algorithm based on dataset size and performance requirements.
