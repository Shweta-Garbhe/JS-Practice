# Get maximum age from an object using reduce method

Given an object of user details. Find a max age from the object.

## Example:

- Input:

```
> const users = [
> { name: 'abc', age: 35, isAdmin: true },
> { name: 'xyz', age: 25, isAdmin: true },
> { name: 'pqr', age: 45, isAdmin: false}
> ];
```

- Output:

```
> 45
```

## CODE

```
const users = [
{ name: 'abc', age: 35, isAdmin: true },
{ name: 'xyz', age: 25, isAdmin: true },
{ name: 'pqr', age: 45, isAdmin: false}
];

const maxAgeUser = users.reduce((acc, curr) => {
    if(curr.age > acc){
        acc = curr.age;
    }
    return acc;
}, 0);

console.log(maxAgeUser);
```

## Explaination:

- We are passing users object to reduce method.
- Reduce method defining accumulator as a zero (0) and current is reprresenting a current row in an object.
- we are checking, if current row's age is greater than accumulator `acc` (which is initially zero).
- If yes then storing that age value in `acc`, if no then continue to the next row.
- We continue to do so until we check last row in an object.
- At the end, we are getting the maximum age in `acc` and returning it from reduce.
