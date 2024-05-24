```javascript
// Question1: How to find duplicate elements in array in javascript ?
const arrNumber = [1, 2, 8, 2, 9, 8];

const duplicates = arrNumber.filter((elem, index, arr)=> arr.indexOf(elem) !== index);
console.log(duplicates);

// How to find max in a given Array 
const array = [1, 2, 3, 4, 5, 6];
// const maxArr = (arr)=> {
//     return arr.reduce(function(pre, cur){
//         return pre > cur ? pre:cur;
//     })
// }
// console.log(maxArr([1, 2, 3, 4, 5, 6]))
// How to find min in a given Array 
// const array = [1, 2, 3, 4, 5, 6];
const minArr = (arr)=> {
    return arr.reduce(function(pre, cur){
        return pre < cur ? pre : cur
    })
}
console.log(minArr(array));

// How to find second largest value, and remove First largest value in array 
let intArr = [2, 8, 9,7];
const largestValue = (arr) => {
    firstLargetValue = Math.max(...arr);
    index = arr.indexOf(firstLargetValue);
    arr.splice(index, 1);
    secondLargestValue = Math.max(...arr);
    return secondLargestValue;
}
console.log(largestValue(intArr));

// filter() method returns the matched values in an array from the collection.
// find() method returns the first value that matches from the collection. Once it matches the value in findings, it will not check the remaining values in the array collection.
const empArr = [
    {
        name : "king", age : 42
    },
    {
        name : "ali", age : 32
    },
    {
        name : "ahmed", age : 22
    },
    {
        name : "zain", age : 62
    },
    {
        name : "ayesa", age : 52
    },
    {
        name : "hafsa", age : 58
    },
    {
        name : "sadi", age : 27
    }
]

const filterItem = empArr.filter((item) => item.age > 30);
console.log(filterItem);
const findItem = empArr.find((item) => item.age > 30);
console.log(findItem);

// How to find missing elements in a given array from 1 to 10.
const missingArr = [1, 2, 3, 4, 5, 6, 9, 10];
const missingElem = [];
const missingValue = (arr) => {
    const maxValue = Math.max(...arr);
    console.log(maxValue);
    const minValue = Math.min(...arr);
    for(let i = minValue; i < maxValue; i++){
        if(arr.indexOf(i) < 0){
            missingElem.push(i);
        }
    }
    return missingElem;
}
console.log(missingValue(missingArr));

// how to find even or odd numbers an array in javascript
const numbers = [1, 2, 3, 8, 9, 16, 63];
const even = (num) => {
    return num.filter((item) => item % 2 === 0)
}
console.log(even(numbers));
const odd = (num) => {
    return num.filter((item) => item % 2 !== 0)
}
console.log(odd(numbers));

// How to find the sum of elements in array 
const sumUp = (num) => {
    return num.reduce((pre, cur)=> {
        return pre + cur;
    })
}
console.log(sumUp(numbers));

// how to find the factorial number of a given number of javascript

const factorialNum = (num) => {
    let fact = 1;
    for(let i = 1; i <= num; i++){
        fact = fact * i;
    }
    return fact;
}
console.log(factorialNum(6))

function factorial(num){
    let fact = 1;
    for(let i = 1; i <= 5; i++){
        fact = fact * i;
    }
    return fact;
}
console.log("Factorial number is :"+ factorial(5));

// how to find prime number in javascript
function primeNumber(num){
    if(num === 1){
        return num + " is not a prime number neither composite";
    } else if (num < 1){
        return "Prime number is not possible";
    }else{
        let result;
        for(let i = 2; i <num; i++){
            if(num % i == 0){
                result = `${num} is not a prime number`;
                break;
            }else{
                 result = `${num} is a prime number`;
            }
        }
        return result;
    }
}
console.log(primeNumber(11));


// check the character if it's a vowel otherwise consonant
function checkString(str){
    if(str === 'a' || str === 'e' || str === 'i' || str === 'o' || str === 'u'){
        return `${str} is a vowel`;
    }else{
        return `${str} is consonant`;
    }
}
console.log(checkString('p'));
// count the number of vowel of a String 
function countVowel(str){
    let vowels = ['a', 'e', 'i', 'o', 'u'];
    let count = 0;
    for(let x of str){
        if(vowels.includes(x)){
            count++;
        }
    }
    return count;
}
console.log(countVowel('jasim is a student'));

// How to reverse a string in javascript
function reverseStr(str){
    return str.split('').reverse().join('');
}
console.log(reverseStr('Jasim'));

// How to find Palindrome in Javascript 
function PalindromeStr(str){
    str = str.toLowerCase();
    let reverseStr = str.split('').reverse().join('');
    if(reverseStr === str){
        return "String is a Palindrome";
    }else{
        return "String is not a Palindrome";
    }
}
console.log(PalindromeStr("Moma"));
// how to swap variable using third variable 
function swapVariable(a, b){
    let temp = a;
    a = b;
    b= temp;
    return `a = ${a} and b = ${b}`;
}
console.log(swapVariable(10,20));
// how to swap variable using third variable 
const swapVariableThird = (a, b)=> {
    return [a, b] = [b, a]; 
}
console.log(swapVariableThird(10,20));
const swapVariableThirdWithout = (a, b)=> {
    a = a + b;
    b = a - b;
    a = a - b;
    return `After Swaping variable a = ${a} and b = ${b}`;
}
console.log(swapVariableThirdWithout(12, 23));

// How to merged two arrays in Javascript
const mergedArr = (arr1, arr2) => {
    const finalArr = arr1.concat(arr2);
    const sortedArr = finalArr.sort(function(a, b){
        return a-b;
    })
    return sortedArr;
}
console.log(mergedArr([2, 4, 5],[3, 6, 7]));

// using spread matrix
const mergedSort = (arr1, arr2) => {
    let result = [...arr1, ...arr2];
    let sortedArr = result.sort(function(a,b){
        return a-b;
    })
    return sortedArr;
}
console.log(mergedSort([2, 4, 6], [1, 3, 5]));


// How to find factor of a given integer in Javascript 
function factorInt(num){
    for(let i = 0; i <= num; i++){
        if(num % i ==0){
            console.log(i);
        }
    }
}
factorInt(10);

// Simple calculator in Javascript 
function calculator(num1, op, num2){
    if(op === '+'){
        return num1 + num2;
    }else if (op === '-'){
        return num1 - num2;
    }else if (op === '*'){
        return num1 * num2;
    } else if (op === '/'){
        return num1 / num2;
    }
}
console.log(calculator(5, '+', 10));

// How to compare two arrays are equal or not in Javascript 
function isArraySame(arr1, arr2){
    const isSame = (arr1.length == arr2.length) && arr1.every((elem) => {
        if(arr2.indexOf(elem) > -1){
            return elem = [arr2.indexOf(elem)];
        }
    })
    return isSame;
}
console.log("is Array same is " +isArraySame([2, 9, 6, 8, 4], [4, 8, 6, 9, 2]));

// how to find intersection of two arrays in javascript 
const IntersectionFunc = (arr1, arr2) => {
    let returnedValue = arr1.filter((elem) => {
        return arr2.includes(elem);
    })
    return returnedValue;
}
console.log([...new Set(IntersectionFunc([1, 3, 3, 5, 7, 7, 7, 6, 7], [2, 4, 6, 7, 3, 6, 7]))]);

// How to find union of two arrays in Javascript
const UnionFunc = (arr1, arr2) => {
    let unionVar = [...arr1, ...arr2];
    return [...new Set(unionVar)];
}
console.log(UnionFunc([1, 3, 3, 5, 7, 7, 7, 6, 7], [2, 4, 6, 7, 3, 6, 7]))


// How to convert celcius to fahrenheit and fahrenheit to celcius

function converter(input){
    var celciusTofahrenheit = input * 1.8 + 32;
    console.log(celciusTofahrenheit);
    var fahrenheitTocelcius = 5/9*(input - 32);
    console.log(fahrenheitTocelcius);
}
converter(100);

// how to convert First Letter of a String in to Uppercase in Javascript ? 
function firstLetter(inputStr){
    let newStr = inputStr.split(' ').map((elem) => {
        return elem.charAt(0).toUpperCase() + elem.slice(1);
    })
    return newStr.join(' ');
}
console.log(firstLetter("jasim"))

// How to find fibonacci sequence in javascript
function fibonacciNumber(num){
    let a = 0;
    let b = 1;
    for(let i = 0; i <= num; i++){
        let temp = a + b;
        a = b;
        b = temp;
        console.log(temp);
    }
}
fibonacciNumber(15);

 // Print the pyramid, star and Diamond shape in Javascript
function pyramid(num){
    for(let i = 1; i <= num; i++){
        for(let j = 1; j <=i; j++){
            // document.write("*");
        }
        // document.write("<br>");
    }
}
pyramid(5); 
// how to check the number of occurance in a string
function numberOfOccurance(num, digit){
    let counter = 0;
    for(let i = 0; i < num.length; i++){
        if(num[i] == digit){
            counter++;
        }
    }
    return counter;
}
console.log(numberOfOccurance("jasim uddimmmm", 'm'));

// Program to print the table of any user defined number using function
const table = (number)=> {
    for(let i = 1; i <=10; i++){
        let res = i * number;
        console.log(`${i} * ${number} = ${res}`);
    }
}
table(10);
table(20);

// Check armstrong number in Javascript

function armStrong(num){
    let temp = num;
    let sum = 0;
    while(temp > 0){
        let res = temp % 10;
        sum += res*res*res;
        temp = Math.floor(temp /10);
    }
    if(num === sum){
        return "Number is armstrong = " + num;
    }else{
       return "Not an armStrong number";
    }
}
console.log(armStrong(153));




// Which results will be print in the console first
console.log(1);
setTimeout(()=>{console.log(2)},1000);
setTimeout(()=>{console.log(3)}, 0);
console.log(4);

// Which will be the output in the console first
// var i = 1;
setTimeout(()=>{
    console.log(i);
    var i =1;
})
```
