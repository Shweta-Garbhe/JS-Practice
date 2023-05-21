# Palindrome

Write a code which will accept a string and check passed string is palindrome or not.

### EXAMPLE:

- Input:

```
> const str = "madam";
```

- Output:

```
 Palindrome / Not Palindrome
```

### CODE

```
const str = "Madam";

function isPalindrome(str) {
  // Reversing the string by lowercasing the characters.
  const reverseString = str.toLowerCase().split("").reverse().join("");

  // Checking the reversed string matches with second string
  if (reverseString === str.toLowerCase()) {
    return "Palindrome";
  } else {
    return "Not Palindrome";
  }
}

// Calling the function
console.log(isPalindrome(str));
```

### EXPLAINATION:

- We have passed a random strings
- First we have coverted the string to avoid capital/small checks then we have reversed the string with `.split("").reverse().join("")`.
- Then we have checked if reversed string matches with original passed as an argument string.
- If yes, te string is palindome and if not, it is not palindrome.
