# Quicksort

Quicksort is a sorting algorithm that uses the divide and conquer design paradigm dividing the array items into elements smaller and greater than an specific item called pivot, in a process called partition.

On the partition process, we reorder the array so that all elements with values less than the pivot come before the pivot, while all elements with values greater than the pivot come after it. After this operation the pivot is its final position and we need to sort the array to the left and right of it using the same process.

The process usually is recursive, but it can be implemented in a non-recursive manner as well.

There are two partition algorithms, Hoare's and Lomuto.

## Hoare's partition

Considered the most efficient between the two, since it does fewer swaps on average, this algorithms works initializing two indexes at the two final ends of the array (left and right). Both indexes move toward each other and every time the left element is greater than the pivot, and the right element is smaller than the pivot, they switch. At the end the pivot is on its right position.

![gif](https://upload.wikimedia.org/wikipedia/commons/9/9c/Quicksort-example.gif)

## Lomuto's partition

The pivot is usually the last element in the array. There's a loop between the first element and the element previous to the pivot, the second-last element, and there is an index variable initialized with the first index, lets call it partitionIndex. Any time in the loop an element is smaller than the pivot is reached, it is sent to the index partitionIndex is pointing, there's a swap, and this partitionIndex is incremented. This way, all the elements smaller than the pivot are grouped, and at the end the pivot is sent to the positionIndex, and we have a array split between the elements greater than the pivot and smaller than the pivot.

![gif](https://upload.wikimedia.org/wikipedia/commons/8/84/Lomuto_animated.gif)