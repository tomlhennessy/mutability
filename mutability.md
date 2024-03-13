# Mutability

* data types that can be changed are mutable, those that cannot be changed are immutable
* arrays and objects are mutable
* numbers, strings, and booleans are immutable

# Addition Mutator
Modifies the input arrays by adding a specific value to each element in the array.

```javascript
// takes in two parameters: an array of numbers and the value to be added to each element of the array
let additionMutator = function(numbers, n) {
    // iterate through each element of 'numbers' array
    for (let i = 0; i < numbers.length; i++) {
        // add value of 'n' to each element
        numbers[i] += n;
    }
}

// example 1
let nums1 = [3, 7, 1, 2];
additionMutator(nums1, 4);
console.log(nums1); // output: [7, 11, 5, 6]

// example 2
let nums2 = [11, 9, 4];
additionMutator(nums 2, -1);
console.log(nums2); // output: [10, 8, 3]
```
