# Maps and Sets Exercise

**Quick Question #1**

What does the following code return?

```JavaScript

new Set([1,1,2,2,3,4]) // [1,2,3,4]

```

**Quick Question #2**

What does the following code return?

```JavaScript

[...new Set("referee")].join("") //ref

```

**Quick Questions #3**

What does the Map m look like after running the following code?

```JavaScript

let m = new Map();
m.set([1,2,3], true);
m.set([1,2,3], false);

//After execution

0 : {Array(3) => true}
1 : {Array(3) => false}

```


**hasDuplicate**

Write a function called hasDuplicate which accepts an array and returns true or false if that array contains a duplicate

```JavaScript

const hasDuplicate = arr => {
   return new Set(arr).size === arr.length? false : true
}

hasDuplicate([1,3,2,1]) // true
hasDuplicate([1,5,-1,4]) // false

```

**vowelCount**

Write a function called vowelCount which accepts a string and returns a map where the keys are numbers and the values are the count of the vowels in the string.

```JavaScript

const vowelCount = (str) => {
  
  const myVowelMap = new Map();
  const vowels = ["a", "e", "i", "o", "u"];
  for (let letter of str.toLowerCase()) {
    if (vowels.includes(letter)) {
      if (myVowelMap.has(letter)) {
        myVowelMap.set(letter, (myVowelMap.get(letter) + 1));
      } else {
        myVowelMap.set(letter, 1);
      }
    }
  }
  return myVowelMap;
}


vowelCount('awesome') // Map { 'a' => 1, 'e' => 2, 'o' => 1 }
vowelCount('Colt') // Map { 'o' => 1 }

```


