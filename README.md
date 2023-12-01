1)print odd numbers
const printOddNumbers = function(arr) {
  arr.forEach(function(num) {
    if (num % 2 !== 0) {
      console.log(num);
    }
  });
};

// IIFE
(function(arr) {
  arr.forEach(function(num) {
    if (num % 2 !== 0) {
      console.log(num);
    }
  });
})([1, 2, 3, 4, 5, 6, 7, 8, 9]);

2)Convert all the strings to title caps in a string array

// Anonymous function
const convertToTitleCaps = function(arr) {
  return arr.map(function(str) {
    return str.split(' ').map(function(word) {
      return word.charAt(0).toUpperCase() + word.slice(1);
    }).join(' ');
  });
};

// IIFE
const titleCapsArray = (function(arr) {
  return arr.map(function(str) {
    return str.split(' ').map(function(word) {
      return word.charAt(0).toUpperCase() + word.slice(1);
    }).join(' ');
  });
})(['hello world', 'goodbye universe', 'javascript is awesome']);

console.log(titleCapsArray);

3)Sum of all numbers in an array

const sumArray = function(arr) {
  return arr.reduce(function(acc, num) {
    return acc + num;
  }, 0);
};

// IIFE
const totalSum = (function(arr) {
  return arr.reduce(function(acc, num) {
    return acc + num;
  }, 0);
})([1, 2, 3, 4, 5]);

console.log(totalSum);

4)Return all the prime numbers in an array

// Anonymous function
const getPrimeNumbers = function(arr) {
  return arr.filter(function(num) {
    for (let i = 2; i < num; i++) {
      if (num % i === 0) {
        return false;
      }
    }
    return num > 1;
  });
};

// IIFE
const primes = (function(arr) {
  return arr.filter(function(num) {
    for (let i = 2; i < num; i++) {
      if (num % i === 0) {
        return false;
      }
    }
    return num > 1;
  });
})([2, 3, 5, 7, 11, 13, 17]);

console.log(primes);

5)Return all the palindromes in an array

// Anonymous function
const getPalindromes = function(arr) {
  return arr.filter(function(str) {
    const reversedStr = str.split('').reverse().join('');
    return str === reversedStr;
  });
};

// IIFE
const palindromes = (function(arr) {
  return arr.filter(function(str) {
    const reversedStr = str.split('').reverse().join('');
    return str === reversedStr;
  });
})(['level', 'hello', 'radar', 'world', 'madam']);

console.log(palindromes);


6)Return median of two sorted arrays of the same size.

// Anonymous function
const medianOfSortedArrays = function(arr1, arr2) {
  const mergedArray = arr1.concat(arr2);
  const sortedArray = mergedArray.sort((a, b) => a - b);

  const length = sortedArray.length;
  const middle = Math.floor(length / 2);

  if (length % 2 === 0) {
    // If the length is even, return the average of the two middle elements
    return (sortedArray[middle - 1] + sortedArray[middle]) / 2;
  } else {
    // If the length is odd, return the middle element
    return sortedArray[middle];
  }
};

// IIFE
const result = (function(arr1, arr2) {
  const mergedArray = arr1.concat(arr2);
  const sortedArray = mergedArray.sort((a, b) => a - b);

  const length = sortedArray.length;
  const middle = Math.floor(length / 2);

  if (length % 2 === 0) {
    // If the length is even, return the average of the two middle elements
    return (sortedArray[middle - 1] + sortedArray[middle]) / 2;
  } else {
    // If the length is odd, return the middle element
    return sortedArray[middle];
  }
})([1, 3, 5], [2, 4, 6]);

console.log(result);

7)Remove duplicates from an array
// Anonymous function
const removeDuplicates = function(arr) {
  return arr.filter(function(value, index, self) {
    return self.indexOf(value) === index;
  });
};

// IIFE
const uniqueArray = (function(arr) {
  return arr.filter(function(value, index, self) {
    return self.indexOf(value) === index;
  });
})([1, 2, 2, 3, 4, 4, 5]);

console.log(uniqueArray);

8)Rotate an array by k times

// Anonymous function
const rotateArray = function(arr, k) {
  const len = arr.length;
  k = k % len; // Handle rotations greater than array length
  const rotatedArray = arr.slice(k).concat(arr.slice(0, k));
  return rotatedArray;
};

// IIFE
const rotatedResult = (function(arr, k) {
  const len = arr.length;
  k = k % len; // Handle rotations greater than array length
  return arr.slice(k).concat(arr.slice(0, k));
})([1, 2, 3, 4, 5], 2);

console.log(rotatedResult);


Do the below programs in arrow functions.
1)Print Odd Numbers in an Array:

const printOddNumbers = (arr) => {
  arr.forEach((num) => {
    if (num % 2 !== 0) {
      console.log(num);
    }
  });
};

2)Convert all the strings to title caps in a string array

const titleCapsArray = (arr) => {
  return arr.map((str) => {
    return str.charAt(0).toUpperCase() + str.slice(1);
  });
};

3)Sum of all numbers in an array
const sumArray = (arr) => {
  return arr.reduce((sum, num) => sum + num, 0);
};

4)Return all the prime numbers in an array

const isPrime = (num) => {
  if (num <= 1) return false;
  for (let i = 2; i <= Math.sqrt(num); i++) {
    if (num % i === 0) return false;
  }
  return true;
};

const getPrimeNumbers = (arr) => {
  return arr.filter((num) => isPrime(num));
};

5)Return all the palindromes in an array

const isPalindrome = (str) => {
  const reversedStr = str.split('').reverse().join('');
  return str === reversedStr;
};

const getPalindromes = (arr) => {
  return arr.filter((str) => isPalindrome(str));
};



