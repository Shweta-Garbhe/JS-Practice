# Remove duplicate elements from two arrays using reduce function.

Write a reduce function which will check the elements in two arrays and remove duplicates from them and merge them into single array.

## Example:

- Input:

```
> var a = ["apple", "cherry", "kiwi"]
> var b = ["banana", "kiwi"]
```

- Output:

```
 [ 'apple', 'cherry', 'kiwi', 'banana']
```

## CODE

```
var arrMerged = a.concat(b);
const arrFiltered = arrMerged.reduce((acc, curr) => {
    if(!(acc.includes(curr))){
        acc.push(curr);
    }
    return acc;
}, [])

console.log(arrFiltered);
```

## Explaination:

- Arrays have been merged using `CONCAT()`.
- `REDUCE()` used to iterate through concatenated array.
- `INCLUDES()` used to check a new array which is `acc` has element in `arrFiltered`? if no then added the element into acc.
- Hence we got unique elements in acc array, which has been returned.
