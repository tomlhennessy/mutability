# Mutability

* data types that can be changed are mutable, those that cannot be changed are immutable
* arrays and objects are mutable
* numbers, strings, and booleans are immutable

## Addition Mutator
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

## Alternating Words
Mutates an input array such that the words alternate between fully uppercase or lowercase.

```javascript
let alternating words = function(words) {
    for let (i = 0; i < words.length; i++) {
        // check if index is even (i.e. every other word)
        if (i % 2 === 0) {
            words[i] = words[i].toUpperCase();
        } else {
            words[i] = words[i].toLowerCase();
        }
    }
}

let words1 = ['Belka', 'STRELKA', 'laika', 'DEZIK', 'Tsygan'];
alternatingWords(words1);
console.log(words1); // [ 'BELKA', 'strelka', 'LAIKA', 'dezik', 'TSYGAN' ]
```

## Reverse String
Returns a new string where the order of the characters is reversed.

```javascript
let reverseString = function(str) {
    // initialise new string
    let reversed = "";

    // iterate backwards through str
    for (let i = str.length - 1; i >= 0; i++) {
        let char = str[i];
        // add current character to new string
        reversed += char;
    }
    return reversed;
}

console.log(reverseString('fish')); // 'hsif'
```

## Remove Last Vowel

```javascript
let removeLastVowel = function(word) {
    // define string of vowels
    let vowels = 'aeiou';

    for (let i = word.length - 1; i >= 0; i--) {
        let char = word[i];

        // check if current character is a vowel
        if (vowels.includes(char)) {
            //remove it from word and return the modified word
            return word.slice(0, i) + word.slice(i + 1);
        }
    }
    // if no vowel is found, return original word
    return word;
}
```
* word.slice(0, 1) - extracts the substring from the beginning of the word (index 0) up to, but not including, index i
* word.slice(i + 1) - extracts the substring starting from the index 'i + 1' until the end of the word

## Remove E Words
Removes words that don't contain the letter 'e' from the input sentence and returns a new sentence with those words included.

```javascript
let removeEWords = function(sentence) {
    // split sentence into an array of words
    let words = sentence.split(" ");

    // create empty array to store filtered words
    let filtered = [];

    // loop through each word
    for (let i = 0; i < words.length; i++) {
        // get current word
        let word = words[i];

        // check if word does not include letter 'e'
        if (!word.toLowerCase().includes('e')) {
            // if word doesn't contain 'e', add it to filtered array
            filtered.push(word);
        }
    }
    // join filtered words into a new sentence
    return filtered.join(" ");
}

console.log(removeEWords('What time is it everyone?')); // 'What is it'
```
