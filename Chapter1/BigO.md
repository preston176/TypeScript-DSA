# Intro to Big O

- Big O is a way to categorize your algorithms time or memory requirements based on input.
- It is a way to describe the efficiency of an algorithm.
- It is not meant to be an exact measurement.

## Example

- So when someone says Oh of N, they mean your algorithm will grow linearly based on input

## Why do we use it?

- Help us make decisions about what data structures and algorithms to use.
- Knowing how they will perform can greatly help create best possible programs out there.

## Example 1

- Consider the following TS code:

```typescript
function sum_char_codes(str: string): number {
  let sum = 0;
  for (let i = 0; i < str.length; i++) {
    sum += str.charCodeAt(i);
  }
  return sum;
}
```

- The above code has a time complexity of O(n) because it will grow linearly with the input.
- The time it takes to run the code will increase linearly with the input size.

## Important concepts

1. Growth is with respect to the input.
2. Constants are dropped
3. Worst case is usually the way we measure Big O.

- In languages like JavaScript, you pay even heavier penalities because the memory can be kept around causing complete halts in the program.
- So it is important to understand how your code will perform with respect to the input.

## Simplest trick for complexity

- Look for loops
- Look for nested loops
- Drop constants (They are not important)

## Example 1 (Above)

```typescript
function sum_char_codes(str: string): number {
  let sum = 0;
  for (let i = 0; i < str.length; i++) {
    sum += str.charCodeAt(i);
  }
  return sum;
}
```

### What's the running time

- If the previous was O(N) then what is the following code?

```typescript
function sum_char_codes(str: string): number {
  let sum = 0;
for (let i = 0; i < str.length; ++i>) {
    sum += str.charCodeAt(i);
}
for (let i = 0; i < str.length; ++i>) {
    sum += str.charCodeAt(i);
}
  return sum;
}
```

- Running time is O(2N) but we drop the constant so it is O(N)

## Example 2

```typescript
function sum_char_codes(str: string): number {
  let sum = 0;
  for (let i = 0; i < str.length; i++) {
    const charCode = n.charCodeAt(i);
    // Capital E
    if (charCode === 69) {
      return true;
    }
    sum += charCode;
  }
  return sum;
}
```

- Running time is O(N) because it will grow linearly with the input.

### Important concepts (Reminder)

1. Growth is with respect to the input.
2. Constants are dropped
3. Worst case is usually the way we measure Big O.
