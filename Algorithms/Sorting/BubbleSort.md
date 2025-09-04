# BubbleSort

Let’s do #BubbleSort. Usually the first #algorithm in almost every major source is insertion #sort, but I find it so boring! Let’s do bubble!

The general definition of a sorted array is this:

```javascript
[                  ]
0                  N

     Xi <= Xi++
```

> For **any index** in the array, the **next index** is *greater than or equal to* the current index

```javascript
[ 1, 3, 7, 4, 2]
```

For BubbleSort, we start at the 0 index, and we loop through the array.

For every index, we check the next index, and if it’s less than the current index, then we swap positions of the two values.

For a singular pass of the array, the largest item will be positioned at the end.

We have to keep looping through the array until each of the items are in-order, but we do not need to check the final element that is in-order
- So the loop should progressively get shorter.

### Example

```javascript
export default function bubble_sort(arr: number[]): void {
    // We have an array from 0 to N
    // We are going to compare i to i+1
    // But we don't want N-1
    // We are going to have an outer loop that will loop through the whole array
    // Then we have the inner loop that does the operations
    // Every time we complete  sort, we want to reduce N - 1
    for (let i = 0; i < arr.length; i++){
        for (let j = 0; j < arr.length - 1 - i; j++) {
            if (arr[j] > arr[j + 1]) {
                const tmp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = tmp;
            }
        }
    }
}
```

### Big O
`O(N^2)`
