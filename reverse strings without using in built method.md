# Reverse a string without using any in built method in javascript.

## Example:

- Input:

```
> let str = "SHWETA"
```

- Output:

```
> let reversedString = "ATEWHS"
```

## CODE

```
let str = "SHWETA";
let reversedString = '';

for (let i = str.length - 1; i >= 0; i--){
    reversedString += str[i];
}

console.log(reversedString);
```

## Explaination:

- We are accepting input in `str` variable.
- We have declared a `reversedString` variable and initialised it with blank space.
- We are then traversing a loop from str.length - 1 which is last character of a string to first character of string.
- In loop, we are concatenating a `reversedString` with every character in string from a loop.
- Hence getting `reversedString` as a reversed input string.
