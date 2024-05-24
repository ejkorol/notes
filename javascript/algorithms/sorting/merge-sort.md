# Merge Sort

> A stable, comparison-based, divide-and-conquer sorting algorithm.

Merge sort is another example of a divide-and-conquer algorithm, it works by dividing the input array into smaller sub-arrays, sorting them, and merging them back together.

## Example

```
function mergeSort (arr) {

    // Check length of arr, when the arr is too small, either 1 or 0, stop the recursion

    if (arr.length <= 1) {
        return arr;
    };

    const mid = Math.floor(arr.length/2) // Get half of the array
    const subArr1 = arr.slice(0, mid); // slice at mid
    const subArr2 = arr.slice(mid) // after mid

    // Pass into function to merge the arrays
    return merge(mergeSort(subArr1), mergeSort(subArr2));

};
```
> Merge Sort Function

```
function merge (subArr1, subArr2) {
    let result = [];
    let i = 0;
    let j = 0;

    while (i < subArr1.length && j < subArr2.length) {
        if (subArr1[i] < subArr2[j]) {
            results.push(subArr1[i]);
            i++;
        } else {
            results.push(subArr2[j]);
            j++;
        };
    };

    return [...result, ...subArr1.slice(i), ...subArr2.slice(j)];
};
```
> Merge the Arrays

```
const unsortedArray = [38, 27, 43, 3, 9, 82, 10];
const sortedArray = merge(unsortedArray);
console.log(sortedArray);
```
> Example Usage

## How It Works

1. Divide: Split the array into two halves.

2. Conquer: Recursively sort each half.

3. Combine: Merge the sorted halves back together into a single sorted array.

## Use Cases

Merge sort is used in various applications where stable and predictable sorting performance is required, such as:

* Sorting large datasets efficiently.
* External sorting: When data being sorted does not fit into memory, merge sort can be used for sorting data stored on disk.
* Merge sort's stability makes it suitable for sorting objects with multiple keys.
* It's a popular choice for implementing stable sorts in standard libraries of programming languages.


## Time Complexity

Overall, merge sort's guaranteed time complexity of O(n log n) makes it a reliable choice for sorting large datasets in many scenarios. Its divide-and-conquer nature also makes it suitable for parallel computing, where multiple processors can work on sorting different parts of the array simultaneously.
