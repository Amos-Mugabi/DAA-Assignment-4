

Merge Sort 
Is a popular and efficient sorting algorithm that follows the divide and conquer paradigm.
It works by dividing the unsorted list into n sub-lists, each containing one element, and then repeatedly
merging sub-lists to produce new sorted sub-lists until there is only one sub-list remaining, which is the sorted list.


diagram to illustrate merge sort.
c:\Users\Mugabi\Desktop\new\Merge img.png

Merge Sort: Explanation

Divide: The unsorted list is divided into n sub-lists, each containing one element. 
This is the base case for the recursive algorithm.

Conquer: The sub-lists are recursively sorted using merge sort.

Combine (Merge): The sorted sub-lists are merged to produce new sorted sub-lists until there is only one sub-list remaining. 
The merging process combines two smaller sorted arrays into a larger sorted array



Analysis of Merge Sort:

Time Complexity: Merge Sort has a time complexity of (log)
O(nlogn) for all cases (worst, average, and best). T
his is because the list is always divided into two halves, and each half is sorted separately and then merged. 
The merge operation takes ()O(n) time.

Space Complexity: Merge Sort has a space complexity of ()O(n) because it requires additional space to store the 
two halves of the array during the sorting process.

Stability: Merge Sort is a stable sort, meaning that the order of equal elements is preserved in the sorted output.

Adaptivity: Merge Sort is not adaptive. 
The time complexity remains (log) O(nlogn) even if the input list is partially sorted. 






Insertion Sort. 

Is a simple sorting algorithm that builds the final sorted array one item at a time. 
It is much less efficient on large lists than more advanced algorithms such as quicksort, heapsort, or merge sort.
However, it has several advantages, including its simplicity and efficiency for small data sets or nearly sorted data.


Algorithm of Insertion Sort.

Start: The algorithm starts with the second element of the array (assuming the first element is already sorted).
Insertion: Compare the current element with the previous elements in the sorted subarray. If the current element is smaller, shift the larger elements to the right until you find the correct position for the current element.
Repeat: Repeat this process for all elements in the array, extending the sorted subarray with each iteration


Diagram to illustrate an insertion sort.
c:\Users\Mugabi\Desktop\new\insertion img.png


Explanation:

The outer loop of the algorithm iterates from the second element to the last element of the input list.
The current element being considered is stored in the variable key.
The inner loop compares key with the elements in the sorted subarray (from index 0 to i - 1) and moves the larger 
elements one position to the right to make space for key.
When a suitable position is found (where the element to the left is smaller and the element to the right is larger or equal), 
key is placed in its correct position.
The process repeats until the entire list is sorted.



Time Complexity Analysis:

Best Case: O(n) 
- When the input list is already sorted, and the inner loop doesn't need to shift elements.
Worst Case: O(n^2) 
- When the input list is sorted in reverse order, and each element must be moved to the beginning of the list.
Average Case: O(n^2)  
- On average, insertion sort performs similarly to the worst case because it involves shifting elements around.

Space Complexity: O(1) 
- Insertion sort is an in-place sorting algorithm, meaning it sorts the list without needing additional memory space.
Insertion sort is efficient for small data sets or nearly sorted data but becomes inefficient for larger lists, 
especially when compared to more advanced sorting algorithms.




3. Selection Sort 

Is a simple comparison-based sorting algorithm. 
The idea behind this algorithm is to divide the input list into two parts: a sorted and an unsorted subarray.
The sorted subarray starts as empty, while the unsorted subarray contains all the elements.
The algorithm repeatedly selects the smallest (or largest, depending on the order) element from the 
unsorted subarray and swaps it with the first element of the unsorted subarray. 
The sorted subarray grows in size and the unsorted subarray shrinks until there are no more elements left in the unsorted subarray.

Diagram to illustrate a selection sort.
c:\Users\Mugabi\Desktop\new\selection img.png


Algorithm:

Find the minimum element in the unsorted subarray.
Swap it with the first element of the unsorted subarray.
Expand the sorted subarray by one element.
Repeat steps 1-3 until the unsorted subarray becomes empty


Analysis:

Time Complexity:
The selection sort algorithm has a time complexity of O(n^2), where n is the number of elements in the array. 
This is because, for each iteration of the outer loop, it scans through the remaining unsorted elements in the inner loop,
which takes n iterations in the worst case for each pass.
Therefore, the overall time complexity is quadratic, making it inefficient for large datasets.

Space Complexity:
Selection sort is an in-place sorting algorithm, meaning it doesn't require additional memory space proportional to the input size. 
It sorts the elements within the input array without the need for significant extra memory. 
Hence, its space complexity is O(1), indicating constant space usage.



Graphical Representation of time complexities of sorting algorithms.

![DAA1](https://github.com/Amos-Mugabi/DAA-Assignment-4/assets/115138015/c5b3de43-8b53-4a3e-b163-a82c449d1cf1)



![DAA2](https://github.com/Amos-Mugabi/DAA-Assignment-4/assets/115138015/4f54d761-f941-48f6-8412-cf8855f14529)


In summary, Merge Sort is the most efficient sorting algorithm among the three for large datasets (O(nlogn)). 
Selection Sort and Insertion Sort, both with quadratic time complexity, become impractical as n increases.
Therefore, for large datasets, Merge Sort is the preferred choice due to its stable and consistent performance.
