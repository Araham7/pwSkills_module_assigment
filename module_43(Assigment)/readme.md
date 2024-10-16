# (Q.1). Count the occurrences :---
## You are building a word count generator that will take a large string of text as input and output the words and the number of times they are present in the string. Your task is to write a function that can count the occurrences of each word in the string and return a Map containing each word's count. For simplicity, you can assume that the string only contains alphabetic characters and spaces.

### Solution :

```Javascript
const sentence = "I am xyz. I am learning web development from PW Skills.";

function countWords(str) {
    const words = str.split(" ");
    const map = new Map();

    for (let word of words) {
        if (map.has(word)) {
        map.set(word, map.get(word) + 1);
    } else {
        map.set(word, 1);
    }
}

  return map;
}
console.log(countWords(sentence));
```

# OUTPUT:
```Output
Map(9) {
  'I' => 2,
  'am' => 2,
  'xyz.' => 1,
  'learning' => 1,
  'web' => 1,
  'development' => 1,
  'from' => 1,
  'PW' => 1,
  'Skills.' => 1
}
```

<hr>

<!-- ////////////////////////////////////////////////// -->

# (Q.2). Only unique items are allowed :---

## You are building a program that takes an array of numbers as input and you need to remove all the duplicates from the array. You want to write a function that can accomplish this task efficiently and returns a new set that contains only the unique elements.

### Solution :

```Javascript
let myArray = [5 , 7 , 3 , 2 , 8 , 4 , 5 , 6 , 8 , 12 , 3 , 2 ,  8 , 5 ];

let uniqueElement = (arr)=>{
    return new Set(arr);
}

console.log(uniqueElement(myArray));
```

# OUTPUT:
```Output
Set(8) { 5, 7, 3, 2, 8, 4, 6, 12 }
```

<hr>

<!-- ////////////////////////////////////////////////// -->

# (Q.3). Swap the values :---

## You are working on a project that requires you to swap the values of two variables without using a temporary variable. You decide to write a function that takes two variables as input and swaps their values using destructuring assignment with an array. The function should take the two variables as arguments, destructure them into an array, and then swap their positions within the array. Finally, the function should return an array with the swapped values. For example, if the function is called with the arguments x = 5 and y = 10, it should return an array [10, 5] with x now equal to 10 and y equal to 5.

### Solution :

```Javascript
let swapNum = (x , y)=>{
    [ x , y] = [ y , x];
    return {x , y}
}


let result = swapNum(56 , 63)


console.log(result);
```

# OUTPUT:
```Output
{ x: 63, y: 56 }
```

<hr>

<!-- ////////////////////////////////////////////////// -->

# (Q.4). Access random elements :---

## You are building a program that takes an array of numbers as input and you need to extract the first, second, and last elements of the array. You decide to write a function that can accomplish this task using destructuring assignment with an array. The function should take the array as an argument, destructure it into three variables representing the first, second, and last elements, and then return an array with these three values. For example, if the input array is [1, 2, 3, 4, 5], the function should return an array [1, 2, 5].

### Solution : 
```Javascript
let myArray = [ 56 , 36 , 98 , 105 , 63 , 102 , 63];

let  extract = (arr)=>{
    [ x , y , , , , , z ] = arr;
    return [x , y , z];
}

let result =  extract(myArray);

console.log(result);
```

# OUTPUT:
```Output
[ 56, 36, 63 ]
```

<hr>

<!-- ////////////////////////////////////////////////// -->

# (Q.5). Min and max values :---

## You are building a program that needs to find the maximum and minimum values in an array of numbers. You decide to write a function that can accomplish this task by taking an array of numbers as input and using the spread operator with the Math methods max() and min(). The function should return an object with two properties, max, and min, representing the maximum and minimum values in the input array, respectively. For example, if the input array is [5, 2, 7, 1, 9], the function should return an object { max: 9, min: 1 }.

## Sol.

```Javascript
let myArray = [ 500 , 23 , 42 , 63 , 96 , 108 , 512 , 36 , 48 , 631 , 105 ];

let minMax = (arr)=>{
    let min = Math.min(...arr);
    let max = Math.max(...arr);

    return { min , max };
}

let result = minMax(myArray);

console.log(result);
```

# OUTPUT:
```Output
{ min: 23, max: 631 }
```

<hr>

<!-- ////////////////////////////////////////////////// -->

# (Q.6). Nested Objects :---

## Write a function that takes an object representing a person as input and extracts the name and street properties from a nested object using object destructuring. The function should return an object with these two properties. A sample object is given below.

## Sol.

```Javascript
let person = {
    name: "Mithun",
    age: 21,
    address: {
        street: "B8, Block B, Industrial Area.",
        city: "Sector 62, Noida",
        state: "Uttar Pradesh"
    }
};

let extract = (obj) => {
    let { name, address: { street } } = obj;

    return { name, street };
};

let result = extract(person);

console.log(result);
```

# OUTPUT:
```Output
{ name: 'Mithun', street: 'B8, Block B, Industrial Area.' }
```
