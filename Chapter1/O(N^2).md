# O(N^2)

- This is a common running time for algorithms that use a nested loop.

## Example

```typescript
function sum_char_codes(str: string): number {
  let sum = 0;
  for (let i = 0; i < str.length; i++) {
    for (let j = 0; j < str.length; j++) {
      sum += charCode;
    }
  }
  return sum;
}
```

- Using the trick we learned before, we can see that the running time is O(N^2) because we have a nested loop
