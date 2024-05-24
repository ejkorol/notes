# Quick Sort

> An efficient, comparison-based, divide-and-conquer sorting algorithm.

A widely used sorting algorithm known for it's efficiency, as well as its easy implementation.

It falls under the category of comparison-based sorting, and follows a *divide and conquer* approach.

## Example

```
const unsortedArray = [7, 2, 1, 6, 8, 5, 3, 4]; // Target Array
const sortedArray = quickSort(unsortedArray); // Closure

function quickSort (arr) {

    // Check length of arr, when the arr is too small, either 1 or 0, stop the recursion

    if (arr.length <= 1) {
        return arr;
    };

    const pivot = arr[arr.length - 1]; // Choose last element as pivot

    const subArr1 = []; // Dividing into 1
    const subArr2 = []; // Diving into 2

    for (let i = 0; i < arr.length - 1; i++) {
        if (arr[i] < pivot) {
            subArr1.push(arr[i]);
        } else {
            subArr2.push(arr[i]);
        };
    };

    // Combine using spread operator, with pivot in the middle
    return [...quickSort(subArr1), pivot, ...quickSort(subArr2)];
};

console.log(sortedArray);
```

## How It Works

1. Divide.
Choose a "pivot" element from the array. Partition the array into two sub-arrays. Elements with less than the pivot, and elements greater than the pivot.

2. Conquer.
Recursively apply the same process to the sub arrays.

3. Combine.
As the sub arrays become sorted, they are combined to produce the final sorted array.

## Use Cases

Quick sort is used in various applications where sorting is a critical operation, such as:

* Sorting large datasets efficiently.
* Implementing search algorithms that require sorted data, like binary search.
* Many programming languages and libraries use quick sort as their default sorting algorithm due to its efficiency and versatility.
* It's also commonly used in real-time systems and embedded devices where memory usage is a concern, as it sorts in-place, i.e., it doesn't require additional memory proportional to the size of the input array.

## Time Complexity

complexity of O(n log n) makes it a preferred choice for sorting large datasets in many scenarios.

However, it's essential to note that its worst-case time complexity is O(n^2), which occurs when the pivot selection consistently creates unbalanced partitions.

Nevertheless, its efficient average performance makes it a popular choice in practice.
