# Reverse every word in a string in a order.

Write a function which will reverse every word in a string without inbuilt reverse function. The reversed words should be in a same order in a string instead of whole string reverse order.

## Example:

- Input:

```
> let inputString = "Javascript is amazing"
```

- Output:

```
> let reversedString = "tpircsavaJ si gnizama"
```

## CODE

```
let inputString = "Javascript is amazing";

function wordsReverser(str){
    let arrSplittedWords = str.split(" ");
    let arrReversedWords = arrSplittedWords.map(word => word.split("").reverse().join(""));
    let strReversedWords = arrReversedWords.join(" ");
    return strReversedWords;
}

/** Short version of above function **/
function wordsReverserShort(str){
    return str.split(" ").map(word => word.split("").reverse().join("")).join(" ");
}

console.log(wordsReverser(inputString));
```

## Explaination:

- We are accepting input in `inputString` variable.
- We have wriiten a function `wordsReverser` which is accepting `inputString` as a parameter and reverse every words in a order.
- The function `wordsReverser`is splitting a string into array elements which are seperated with spaces.
- This seperated strings array pass to map function, which accepts every element in array and reverse that element.
- Post this successful operation, map is returning a array of elements which are reversed individually.
- at last we are conveting this array into string with spaces using `join(" ")`.
- This is how we are getting every word reversed in a string and in the same order as input string.
