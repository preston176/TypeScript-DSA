# O(N^3)

```typescript
function sum_char_codes(str: string): number {
  let sum = 0;
  for (let i = 0; i < str.length; i++) {
    for (let j = 0; j < str.length; j++) {
      for (let k = 0; k < str.length; k++) {
        sum += str.charCodeAt(i);
      }
    }
  }
  return sum;
}
```

- Using the trick we learned before, we can see that the running time is O(N^3) because we have a nested loop.

- We have 1 loop that has 2 nested loops, so the running time is O(N^3).
