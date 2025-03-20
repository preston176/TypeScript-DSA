# Arrays

- Arrays are used to store a collection of elements of the same type.

- Contiguous memory space containing elements of the same type.

- **Contiguous** means that the elements are stored in memory next to each other.

## Getting at specific index

- Arrays are zero-based, meaning the first element is at index 0.

- To get the element at a specific index, you can use the index operator `[]`.

```typescript
const arr = [1, 2, 3, 4, 5];
console.log(arr[0]); // 1
console.log(arr[1]); // 2
console.log(arr[2]); // 3
```

## Inserting elements

- You can insert elements at the end of the array using the `push` method.

```typescript
const arr = [1, 2, 3, 4, 5];
arr.push(6);
console.log(arr); // [1, 2, 3, 4, 5, 6]
```

- You can insert elements at the beginning of the array using the `unshift` method.

```typescript
const arr = [1, 2, 3, 4, 5];
arr.unshift(0);
console.log(arr); // [0, 1, 2, 3, 4, 5]
```

- You can insert elements at a specific index using the `splice` method.

```typescript
const arr = [1, 2, 3, 4, 5];
arr.splice(2, 0, 2.5);
console.log(arr); // [1, 2, 2.5, 3, 4, 5]
```

## Deleting elements

- You can delete elements at the end of the array using the `pop` method.

```typescript
const arr = [1, 2, 3, 4, 5];
arr.pop();
console.log(arr); // [1, 2, 3, 4]
```

- You can delete elements at the beginning of the array using the `shift` method.

```typescript
const arr = [1, 2, 3, 4, 5];
arr.shift();
console.log(arr); // [2, 3, 4, 5]
```

- You can delete elements at a specific index using the `splice` method.

```typescript
const arr = [1, 2, 3, 4, 5];
arr.splice(2, 1);
console.log(arr); // [1, 2, 4, 5]
```

## Searching elements

- You can search for an element in an array using the `indexOf` method.

```typescript
const arr = [1, 2, 3, 4, 5];
console.log(arr.indexOf(3)); // 2
```

- If the element is not found, the `indexOf` method returns `-1`.

```typescript
const arr = [1, 2, 3, 4, 5];
console.log(arr.indexOf(6)); // -1
```

## Iterating over elements

- You can iterate over the elements of an array using a `for` loop.

```typescript
const arr = [1, 2, 3, 4, 5];
for (let i = 0; i < arr.length; i++) {
  console.log(arr[i]);
}
```

- You can also use the `forEach` method to iterate over the elements of an array.

```typescript
const arr = [1, 2, 3, 4, 5];
arr.forEach((element) => {
  console.log(element);
});
```

## Multidimensional arrays

- Arrays can also store other arrays, creating multidimensional arrays.

```typescript
const matrix = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9],
];
console.log(matrix[0][0]); // 1
console.log(matrix[1][1]); // 5
console.log(matrix[2][2]); // 9
```

- You can use nested loops to iterate over the elements of a multidimensional array.

```typescript
const matrix = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9],
];

for (let i = 0; i < matrix.length; i++) {
  for (let j = 0; j < matrix[i].length; j++) {
    console.log(matrix[i][j]);
  }
}
```

## Time complexity

- Accessing an element at a specific index: `O(1)`.

- Inserting an element at the end of the array: `O(1)`.

- Inserting an element at the beginning of the array: `O(n)`.

- Inserting an element at a specific index: `O(n)`.

- Deleting an element at the end of the array: `O(1)`.

- Deleting an element at the beginning of the array: `O(n)`.

- Deleting an element at a specific index: `O(n)`.

- Searching for an element: `O(n)`.

- Iterating over the elements: `O(n)`.

- Accessing an element in a multidimensional array: `O(1)`.

- Searching for an element in a multidimensional array: `O(n^2)`.

- Iterating over the elements of a multidimensional array: `O(n^2)`.

## Space complexity

- The space complexity of an array is `O(n)`, where `n` is the number of elements in the array.

- The space complexity of a multidimensional array is `O(n * m)`, where `n` is the number of rows and `m` is the number of columns.

## Summary

- Arrays are used to store a collection of elements of the same type.

- You can access, insert, delete, and search for elements in an array.

- Arrays have a time complexity of `O(1)` for accessing an element at a specific index and `O(n)` for other operations.

- Multidimensional arrays can store other arrays, creating a matrix.

- Multidimensional arrays have a time complexity of `O(1)` for accessing an element and `O(n^2)` for searching and iterating over the elements.

- The space complexity of an array is `O(n)` and of a multidimensional array is `O(n * m)`.
