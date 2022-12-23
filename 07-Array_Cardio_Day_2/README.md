![App Screenshot](https://github.com/Huiclaire/JavaScript30/blob/master/07-Array_Cardio_Day_2/images/ja30-day7.png)

# 07- Array Cardio Day 2
Perform more operations on JavaScript Arrays.

## Demo
view demo [here]()

## Lesson learned

- `Array.prototype.some()`
- `Array.prototype.every()`
- `Array.prototype.find()`
- `Array.prototype.findIndex()`
- `Array.prototype.splice()`
- `Array.prototype.slice()`

### `Array.prototype.some()`
The [`some()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/some) method checks at least one in the array that meaches, similar to `or` operation.
```javascript
const isAdult = people.some(function(person) {
  const currentYear = (new Date()).getFullYear();
  if (currentYear - person.year >= 19) {
    return true;
  }
});
```
rewrite above in ES6 syntax:
```javascript
const isAdult = people.some(person => (new Date()).getFullYear() - person.year >= 19);
```

### `Array.prototype.every()`
The [`every()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/every) method tests checks all elements in the array, similar to `AND` operation.
```javascript
const everyAdult = people.every(person => (new Date()).getFullYear() - person.year >= 19);
```

### `Array.prototype.find()`

The [`find()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/find) method returns a value of the first element in the array that satisfies the provided testing function.
```javascript
const comment = comments.find(comment => comment.id == 823423);
```


### `Array.prototype.findIndex()`

The findIndex() method returns an index of the first element in the array that satisfies the provided testing function. Otherwise -1 is returned.
```javascript
const index = comments.findIndex(comment => comment.id == 823423);
```

### `Array.prototype.splice()`

The [splice()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice) method changes the contents of an array by removing or replacing existing elements and/or adding new elements in place.


```javascript
comments.splice(index, 1); // will change content of the origin array
```
`splice()`syntax:

```
splice(start, deleteCount, item1)
```
- Remove (deleteCount) elements before index (start), and insert "item1"

### `Array.prototype.slice()`
The [slice()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice) method returns A new array containing the extracted elements. The original array will not be modified.


```javascript
const newComments = [
  ...comments.slice(0, index),
  ...comments.slice(index + 1)
];
```
`slice` syntax:
```
slice()
slice(start)
slice(start, end)
```
- returns a shallow copy of a portion of an array into a new array object selected from start to end (end not included) where start and end represent the index of items in that array.
