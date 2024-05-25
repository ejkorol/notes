# Merge Sort

> A stable, comparison-based, divide-and-conquer sorting algorithm.

Merge sort is another example of a divide-and-conquer algorithm, it works by dividing the input array into smaller sub-arrays, sorting them, and merging them back together.

## Example

```
const unsortedArr = [12, 23, 45, 54, 32, 1, 67, 43, 31, 5, 9];
const sortedArr = mergeSort(unsortedArr);

function mergeSort (arr) {

  if (arr.length <= 1) {
    return arr;
  };

  const mid = Math.floor(arr.length / 2);
  let subArr1 = arr.slice(0, mid);
  let subArr2 = arr.slice(mid);

  return merge(mergeSort(subArr1), mergeSort(subArr2));

};

function merge (arr1, arr2) {

  let result = [];
  let arr1Index = 0;
  let arr2Index = 0;

  while (arr1Index < arr1.length && arr2Index < arr2.length) {
    if (arr1[arr1Index] < arr2[arr2Index]) {
      result.push(arr1[arr1Index]);
      arr1Index++;
    } else {
      result.push(arr2[arr2Index]);
      arr2Index++;
    };
  };

  return result.concat(arr1.slice(arr1Index)).concat(arr2.slice(arr2Index));
};

console.log(sortedArr);
```

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
