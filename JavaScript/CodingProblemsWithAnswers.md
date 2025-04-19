1. Find Maximum Difference Between Consecutive Elements

Write a function that accepts an array of integers and returns the maximum difference between any two consecutive elements in the array. If the array has less than two elements, return 0.

Example:

Input: [3, 8, 15, 2, 10]
Output: 13


```javascript
const findMaxDifference = arr => {
  if (arr.length > 1) {
    return arr.reduce((acc, item, index) => {
      if (!item || !arr[index + 1]) {
        return acc;
      }
      const diff = item > arr[index + 1] ? item - arr[index + 1] : arr[index + 1] - item;
      return acc > diff ? acc : diff;
    }, 0);
  }
  return 0;
}

console.log(findMaxDifference([3, 8, 15, 2, 10]));
console.log(findMaxDifference([1, 3, 8, 15]));
console.log(findMaxDifference([5, 12, 4, 10]));
console.log(findMaxDifference([10, 8, 6, 4, 2]));
console.log(findMaxDifference([20]));
console.log(findMaxDifference([]));
```


2. Transform Array by Multiplying Even Indices and Subtracting Odd Indices

Create a function that takes an array of integers and transforms it according to specific rules: multiply the elements at even indices by their index number, and subtract the index number from elements at odd indices.

Example:

Input: [4, 3, 6, 2, 5]
Output: [0, 2, 12, -1, 20]


```javascript
function transformArray (arr) { return arr.map((item, index) => index % 2 == 0 ? item * index : item - index) };

console.log(transformArray([4, 3, 6, 2, 5]));
console.log(transformArray([1, 2, 3, 4, 5]));
console.log(transformArray([]));
console.log(transformArray([7, 8]));
console.log(transformArray([10, 20, 30]));
console.log(transformArray([2, 4, 6, 8, 10, 12]));
```

3. Find Number of Vowels in a String

Create a function that counts the number of vowels in a given string. Vowels include 'a', 'e', 'i', 'o', 'u', both uppercase and lowercase. The function should return the total count of vowels in the string.

Example:

Input: "Hello World"
Output: 3


```javascript
function countVowels(str) { 
  return [...str].reduce((acc, item) => 
    ['a', 'e', 'i', 'o', 'u'].includes(item.toLowerCase()) ? ++acc : acc,
  0);
}

countVowels("Hello World");
```

4. Shuffle Array Elements in Pairs

Given an array of even length, shuffle its elements such that the first element is swapped with the second, the third with the fourth, and so on. The task is to rearrange the array in-place in these pairs.

Example:

Input: [5, 9, 1, 3, 8, 2]
Output: [9, 5, 3, 1, 2, 8]


```javascript
function shuffleInPairs(str) { 
  return arr.reduce((acc, item, index) => {
        if (index %2 !== 0) {
            return acc;
        }
        acc[index] = arr[index + 1];
        acc[index + 1] = arr[index];
        return acc;
    },  [])
}

console.log(shuffleInPairs([5, 9, 1, 3, 8, 2]));
console.log(shuffleInPairs([12, 24, 8, 34, 15, 7]));
console.log(shuffleInPairs([100, 200, 300, 400]));
console.log(shuffleInPairs([2, 4, 6, 8, 10, 12, 14, 16]));
console.log(shuffleInPairs([1, 0]));
console.log(shuffleInPairs([2, 4, 6, 8, 10, 12, 14, 16]));
```

5. Rotate Matrix 90 Degrees Clockwise

Given an N x N matrix, write a function to rotate it 90 degrees clockwise. You should do this in-place.

Example:

Input: [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
Output: [[7, 4, 1], [8, 5, 2], [9, 6, 3]]


```javascript
function rotateMatrix(matrix) {
  return matrix.reduce((acc, item, index) => {
    acc[index] = [];
    for(var i=0;i< item.length; i++) {
      acc[index][i] = matrix[matrix.length - i -1][index];
    }
    return acc;
  }, []);
}

console.log(rotateMatrix([[1, 2, 3], [4, 5, 6], [7, 8, 9]]));
console.log(rotateMatrix([[1, 2], [3, 4]]));
console.log(rotateMatrix([[1, 2, 3, 4], [5, 6, 7, 8], [9, 10, 11, 12], [13, 14, 15, 16]]));
```

6. Compute the Longest Common Prefix

Write a JavaScript function to find the longest common prefix string amongst an array of strings. If there is no common prefix, return an empty string "".

Example:

Input: ["flower","flow","flight"]
Output: "fl"


```javascript
function findLongestCommonPrefix(arr) {
  let matched = '';
  if (!arr.length){
    return matched;
  }
  const sortedArr = arr.sort((a, b) => a.length - b.length);
  const firstItem = sortedArr[0];
  for(i=0;i< firstItem.length; i++) {
    const spliced = firstItem.substr(0, firstItem.length -i);
    const isPreFixPresent = arr.every(a => a.includes(spliced));
    if(isPreFixPresent){
      matched = spliced;
      break;
    }
  }
  return matched;
}

console.log(findLongestCommonPrefix(["dog","racecar","car"]))
console.log(findLongestCommonPrefix(["interspace","internal","internet"]))
console.log(findLongestCommonPrefix(["over","overcome","overlap","overtime"]))
console.log(findLongestCommonPrefix(["prefix","preach","premise"]))
console.log(findLongestCommonPrefix(["apple","ape","april"]))
console.log(findLongestCommonPrefix(["flower","flow","flight"]));
```

7. Calculate Median of a Number Array

Write a function that takes an array of numbers and returns the median value. The median is the middle number in a sorted list of numbers. If the list is even, the median is the average of the two middle numbers.

Example:

Input: [3, 1, 4, 1, 5, 9]
Output: 3.5


```javascript
function findMedian(arr) {
  const sortedArr = arr.sort((a, b) => a - b);
  const middleIndex = Math.ceil(sortedArr.length / 2) -1;
  if (sortedArr.length % 2 === 0) {
    const [a, b] = sortedArr.slice(middleIndex, middleIndex+2);
    return (a + b)/ 2;
  }
  return sortedArr[middleIndex];
}

console.log(findMedian([3, 1, 4, 1, 5, 9]));
console.log(findMedian([1, 3, 2]));
console.log(findMedian([5, 8, 1, 4, 7]));
console.log(findMedian([1, 6, 7, 2, 5, 3]));
console.log(findMedian([12, 11, 15, 10, 14]));
```

8. Array: Find Missing Number in Arithmetic Sequence

Given an array that represents an arithmetic progression with one missing element, implement a function to find the missing number. An arithmetic progression is defined as a sequence of numbers such that the difference of any two successive members is a constant. Consider the input array is non-empty and the progression has at least three elements (including the missing one).

Example:

Input: [5, 10, 20, 25, 30]
Output: 15


```javascript
function findMedian(arr) {
  const sortedArr = arr.sort((a, b) => a - b);
  const middleIndex = Math.ceil(sortedArr.length / 2) -1;
  if (sortedArr.length % 2 === 0) {
    const [a, b] = sortedArr.slice(middleIndex, middleIndex+2);
    return (a + b)/ 2;
  }
  return sortedArr[middleIndex];
}

console.log(findMedian([3, 1, 4, 1, 5, 9]));
console.log(findMedian([1, 3, 2]));
console.log(findMedian([5, 8, 1, 4, 7]));
console.log(findMedian([1, 6, 7, 2, 5, 3]));
console.log(findMedian([12, 11, 15, 10, 14]));
```

9. String Compression

Implement a string compression function that uses the counts of repeated characters. For character sequence, if the character is repeated, it should be compressed into the format `character+count`. For example, the string "aabcccccaaa" should become "a2b1c5a3". If the compressed string is not smaller than the original, return the original string.

Example:

Input: "aabcccccaaa"
Output: "a2b1c5a3"


```javascript
function compressString(str) {
  const chars = [...str];
  const uniqueChars = [...new Set(str)];
  return uniqueChars?.reduce((acc, item) => {
    const charLength = chars.filter(char => char === item)?.length;
    return `${acc}${item}${charLength}`;
  }, '')
}

console.log(compressString("aabcccccaaa"));
console.log(compressString("abcd"));
console.log(compressString("bbbaaa"));
console.log(compressString("aabbcc"));
console.log(compressString("zzzzzzzz"));
```


10. Find Majority Element in an Array

Given an array of integers, your task is to find the majority element. The majority element is the element that appears more than ⌊ n/2 ⌋ times in the array, where n is the length of the array. You can assume that the array always has a majority element.

Example:

Input: [3, 2, 3]
Output: 3

```javascript
function findMajority(arr) {
  const numbers = [...arr];
  const majorityObj = numbers?.reduce((acc, item) => {
    const count = chars.filter(char => char === item)?.length;
    if (!Object.values(acc).length) {
      return { [item]: count}
    }
    const value = Object.values(acc)?.[0];
    if (value > count) {
      return acc;
    }
    return { [item]: count};
  }, {});
  return Object.keys(majorityObj)?.[0];
}

console.log(findMajority([3, 2, 3]));
```

11. Determine Leap Year

Create a function to determine if a given year is a leap year. A year is a leap year if it is divisible by 4. However, if the year is a century (divisible by 100), it must also be divisible by 400 to qualify as a leap year.

Example:

Input: 2000
Output: true

```javascript
// Method 1
function isLeapYear(year) {
  if ((year % 4 === 0 && year % 100 !== 0) || year % 400 === 0) {
    return true;
  }
  return false;
}

// Method 2
const isLeapYear = (year) => new Date(year, 1, 29).getDate() === 29;

console.log(isLeapYear(2020))
console.log(isLeapYear(1900))
console.log(isLeapYear(2000))
console.log(isLeapYear(2021))
console.log(isLeapYear(2400))
```

12. Determine Leap Year

Given a string, reverse the order of words in the string. A word is defined as a sequence of non-space characters. The words in the input string will be separated by at least one space. You need to return a string that joins the words with a single space in the reversed order. Ensure to trim any leading or trailing spaces from the input before processing.

Example:

Input: ' Hello World! Welcome to JavaScript Challenges '
Output: 'Challenges JavaScript to Welcome World! Hello'

```javascript
function reverseWords(string) {
  const splittedWords = string.trim().split(" ");
  const reversed = splittedWords.reduce((acc, item) => {
    acc.unshift(item);
    return acc;
  }, []);
  return reversed.join(" ");
}

console.log(reverseWords(" Hello World! Welcome to JavaScript Challenges "));
console.log(reverseWords("Good luck with the Coding Challenges!"))
console.log(reverseWords(" Quick brown fox "))
console.log(reverseWords("JavaScript is awesome!"))
console.log(reverseWords(" Spaces should be trimmed "))
```

13. Flatten a Nested Object

Given a deeply nested object, write a function that returns a new flattened object where each key is a path to the value in the original object using dot notation. You should not use any external libraries, only pure JavaScript.

Example:

Input: { "a": { "b": { "c": 1 }, "d": 2 } }
Output: { "a.b.c": 1, "a.d": 2 }

```javascript
function flattenObj(obj, parent, res = {}){
  for(let key in obj){
      let propName = parent ? parent + '.' + key : key;
      if(typeof obj[key] == 'object'){
          flattenObj(obj[key], propName, res);
      } else {
          res[propName] = obj[key];
      }
  }
  return res;
}

console.log(flattenObj({ "a": { "b": { "c": 1 }, "d": 2 } })) 
```

14. Add Numbers in a Matrix Diagonal

Create a function that takes a square matrix (2D array) as input and returns the sum of the numbers in the matrix's main diagonal. The main diagonal of a matrix consists of the elements starting from the top left corner to the bottom right corner.

Example:

Input: [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
Output: 15

```javascript
function sumMatrixDiagonal(matrix) {
  return matrix.reduce((acc, item, index) => acc+item[index], 0);
}

console.log(sumMatrixDiagonal([[1, 2, 3], [4, 5, 6], [7, 8, 9]]));
```

15. Find the Smallest Element in Rotated Sorted Array

You're given a rotated sorted array, where the original array was sorted in increasing order, but then it was rotated at some pivot. Your task is to find the smallest element in the rotated array. Assume there are no duplicate elements in the array.

Example:

Input: [4,5,6,7,0,1,2]
Output: 0

```javascript
function findSmallest(arr) {
  return Math.min(...arr);
}

console.log(findSmallest([4,5,6,7,0,1,2]))
console.log(findSmallest([3,4,5,1,2]))
console.log(findSmallest([11,13,15,17]))
console.log(findSmallest([30, 40, 50, 10, 20]))
console.log(findSmallest([7,8,9,10,1,2,3,4,5,6]))
```

15. Sort Array by Parity

Write a function that takes an array of non-negative integers and returns a new array where all the even numbers are followed by all the odd numbers. The order of even numbers and odd numbers in the original array should be preserved in the output array.

Example:

Input: [3, 1, 2, 4]
Output: [2, 4, 3, 1]

```javascript
function sortArray(arr) {
  const evenArr = [];
  const oddArr = [];
  for(let item of arr){
    if (item%2 === 0){
      evenArr.push(item)
    } else {
      oddArr.push(item)
    }
  }
  return [...evenArr, ...oddArr];
}

console.log(sortArray([3, 1, 2, 4])) // [2,4,3,1]
console.log(sortArray([0, 2, 1, 3, 4])) // [0,2,4,1,3]
console.log(sortArray([1, 3, 5, 7])) // [1,3,5,7]
console.log(sortArray([])) // []
console.log(sortArray([2, 4, 6, 8])) // [2, 4, 6, 8]
```

16. Flatten Deeply Nested Arrays

Write a function that takes a deeply nested array of integers and returns a completely flattened array. The nested arrays can have any depth.

Example:

Input: [1, [2, [3, [4, 5], 6], 7], 8]
Output: [1, 2, 3, 4, 5, 6, 7, 8]

```javascript
function flatArray(arr) {
  return arr.flat(Infinity);
}

console.log(flatArray([1, [2, [3]], 4]))
console.log(flatArray([[[1], 2], 3, [4, [5, [6]]]]))
console.log(flatArray([]))
console.log(flatArray([10, [[20], [30, [40, [50]], 60], 70], 80]))
console.log(flatArray([[1, 2, 3], 4, [5, 6, [7, 8, [9, 10]]]]))
```

17. Replace Vowels with Asterisks

Write a function that takes a string as input and returns a new string with all vowels (a, e, i, o, u) replaced by asterisks (*). This function should be case-insensitive, meaning 'A' and 'a' are both considered vowels and should be replaced by '*'.

Example:
Input: "hello World"
Output: "h*ll* W*rld"

```javascript
function replaceVowels(input) {
  return input.replace(/[aeiou]/gi, '*');
}

console.log(replaceVowels('hello World'));
console.log(replaceVowels('JAVASCRIPT'));
console.log(replaceVowels('abcdefgABCDE'));
console.log(replaceVowels('PROGRAMMING fun'));
console.log(replaceVowels('Vowels AEIOU XyZ'));
```

18. Frequency of Numbers in a Matrix

Write a function that receives a matrix of integers and returns an object representing the frequency of each number present in the matrix. The matrix can vary in dimensions (n x m), and the numbers can be both positive and negative.

Example:
Input: [[1, 2, 2, 3], [3, 3, 1], [4, 5, 1, 1]]
Output: {"1": 4, "2": 2, "3": 3, "4": 1, "5": 1}

```javascript
function findFrequency(arr) {
  const sortedArr = arr.flat().sort((a,b) => a-b);
    const unique = [...new Set(sortedArr)];
    return unique.reduce((acc, item) => {
        const itemCount = sortedArr.filter(arr => arr === item)?.length;
        return {
            ...acc,
            [item]: itemCount
        }
    }, {});
}

console.log(findFrequency([[1, 2, 2, 3], [3, 3, 1], [4, 5, 1, 1]]));
console.log(findFrequency([[5, 5, 5], [5, 5], [5]]));
console.log(findFrequency([[7, 8, 9, 7], [8, 7, -1], [-1, -1, -1, 10]]));
console.log(findFrequency([[0, 0, 0], [0, 0, 0], [0, 0, 0]]));
console.log(findFrequency([[1], [2], [3], [4], [5]]));
```

19. Sort Array by Parity

Write a function that takes an array of non-negative integers and returns a new array where all the even numbers are followed by all the odd numbers. The order of even numbers and odd numbers in the original array should be preserved in the output array.

Example:
Input: [3, 1, 2, 4]
Output: [2, 4, 3, 1]

```javascript
function sortArray(arr) {
  const evenArr = [];
  const oddArr = [];
  for(let item of arr){
    if (item%2 === 0){
      evenArr.push(item)
    } else {
      oddArr.push(item)
    }
  }
  return [...evenArr, ...oddArr];
}

console.log(sortArray([3, 1, 2, 4])) // [2,4,3,1]
console.log(sortArray([0, 2, 1, 3, 4])) // [0,2,4,1,3]
console.log(sortArray([1, 3, 5, 7])) // [1,3,5,7]
console.log(sortArray([])) // []
console.log(sortArray([2, 4, 6, 8])) // [2, 4, 6, 8]
```

20. Find the Second Largest Number in an Array
Given an array of numbers, write a function to find the second largest number in the array. If the array contains less than two unique numbers, return null.

Example:
Input: [5, 3, 9, 1, 9]
Output: 5

```javascript
function findSecondLargest(numbers) {  
  const unique = [...new Set(numbers.sort((a,b) => a-b))];
  if(unique.length < 2) {
    return null;
  }
  return unique[unique.length - 2];
}

console.log(findSecondLargest([5, 3, 9, 1, 9]));
console.log(findSecondLargest([5, 5, 5, 5]));
console.log(findSecondLargest([13, 34, 56, 34, 56, 13]));
console.log(findSecondLargest([1, 2]));
console.log(findSecondLargest([7]));
```

21. Convert Snake Case to Camel Case

Write a function that converts a given string in snake_case format to camelCase format. Snake case strings are those where words are separated by underscores ( _ ). In camelCase, words are joined together and each word after the first word starts with an uppercase letter, and no underscores should be present.

Example:
Input: 'this_is_a_test_string'
Output: 'thisIsATestString'

```javascript
function convertCamelCase(str) {
  const strArr = str.split("_");
  return strArr.reduce((acc, item, index) => {
    if (!index) {
      return item;
    }
    const converted = item.charAt(0).toUpperCase() + item.substr(1, item.length-1);
    return acc+converted;
  }, '');
}

console.log(convertCamelCase("this_is_a_test_string"))
console.log(convertCamelCase("hello_world"))
console.log(convertCamelCase("convert_snake_to_camel_case"))
console.log(convertCamelCase("inner_function_example"))
console.log(convertCamelCase("this_is_already_camel_case"))
```