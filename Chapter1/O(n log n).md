# O(n log n)

- This is a common running time for algorithms that use a divide and conquer strategy.

- The most common example is the merge sort algorithm.

## Example

    ```typescript
    function merge_sort(arr: number[]): number[] {
      if (arr.length <= 1) return arr;
      const mid = Math.floor(arr.length / 2);
      const left = merge_sort(arr.slice(0, mid));
      const right = merge_sort(arr.slice(mid));
      return merge(left, right);
    }
