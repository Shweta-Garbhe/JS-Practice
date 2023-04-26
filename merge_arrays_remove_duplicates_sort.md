# Merge dynamic number of arrays, remove duplicate elements and sort it.

Write a function called merge that takes one or more arrays as parameters and returns the arrays merged together with all duplicates removed and with the values sorted in ascending order.

## Example:

- Input:

```
> var a = ["apple", "cherry", "kiwi"]
> var b = ["banana", "grapes"]
> var c = ["strawberry", "kiwi"]
> var d = ["pear", "guava"]

```

- Output:

```
merge(a, b) should return ["apple", "banana", "cherry", "grapes", "kiwi"]
merge(a, b, c, d) should return ["apple", "banana", "cherry", "grapes", "guava", "kiwi", "pear", "strawberry"]
```

## CODE:

```
function mergeArr(...args){
    var arrMerged = [].concat(...args);
    var arrFiltered = [...new Set(arrMerged)]
    return arrFiltered.sort();
}

console.log(mergeArr(a, b, c, d));
```

## Explaination:

- We have accepted arguments to a function using rest operator (...args)
- Arrays have been merged using CONCAT() with new array and args with spread operator ([].concat(...args)).
- Duplicate elements removed using SET(). The Set object is used to store unique values of primitive values or object references.
- Sorting performed using SORT(). The sort() sorts the elements as strings in alphabetical and ascending order.
