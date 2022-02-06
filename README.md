# core-code
core code bootcamp

> # **Week 1**
> ## **Tuesday**
> - Java language is compiled or interpreted?  
>  &nbsp;&nbsp;&nbsp;&nbsp; Java is both, because it creates the BYTECODE file to iterpret by the JVM.  
> - Create an algorithm to calculate the equivalent of your local currencty to USD  
>  &nbsp;&nbsp;&nbsp;&nbsp; Step 1 – Set current_exchange rate  
>  &nbsp;&nbsp;&nbsp;&nbsp; Step 2 – Get amount_to_convert  
>  &nbsp;&nbsp;&nbsp;&nbsp; Step 3 – Mutiply current_exchange * amunt_to_convert  
>  &nbsp;&nbsp;&nbsp;&nbsp; Step 4 – Get amount converted  
> -  Why is pseudocode helpful?  
>   &nbsp;&nbsp;&nbsp;&nbsp; To understand the problem and plan the solution.  
> - Create a pseudocode to calculate the aproximated age of a user base on the year they born  
> &nbsp;&nbsp;&nbsp;&nbsp; INICIO  
> &nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp; Y <-- 2022  
> &nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp; BORN <-- 1991  
> &nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp; CALCULAR AGE <-- Y - BORN  
> &nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp; DEVOLVER AGE  
> &nbsp;&nbsp;&nbsp;&nbsp; FIN  
> - Why are flowcharts important to us as developers?  
>  To us as developers a flowchart can help us to define the process and flow of our solution, is important to define it before we write some line of code or some PSEUDOCODE  because it should help us determine if our solution ends solving the problem.  
> ## **Wednesday**  
> 1. Learn about binary, decimal and hexadecimal numbers.  
> &nbsp;&nbsp;&nbsp;&nbsp; Done.  
> 2. Translate the year you where born to binary, decimal and hexadecimal.  
> &nbsp;&nbsp;&nbsp;&nbsp; -  11111000111  
> &nbsp;&nbsp;&nbsp;&nbsp; -  1991  
> &nbsp;&nbsp;&nbsp;&nbsp; -  7C7  
> 3. Translate 51966 into hexadecimal and binary.  
> &nbsp;&nbsp;&nbsp;&nbsp; - CAFE  
> &nbsp;&nbsp;&nbsp;&nbsp; - 1100101011111110  
> 4. Use a Low-level language, for example MIPS aseembler, to do so, you will need to follow this guide. We recomend to check the guide first but also this presentation could be helpful.  
> &nbsp;&nbsp;&nbsp;&nbsp; Done.  
> 5. Base on the examples and the guide of the low-level language: 5.1 Create a program to add two numbers given by the user 5.2 Create a program that display your name  
> - 5.1  
```assembly
.data
	number1: .asciiz "\nIngrese el primer numero: "
	number2: .asciiz "\nIngrese el segundo numero: "
.text
    main:
	li $v0, 4
	la $a0, number1
	syscall
	
	li $v0, 5
	syscall
	
	move $t0, $v0
	
	
    
	li $v0, 4
	la $a0, number2
	syscall
	
	li $v0, 5
	syscall
	
	move $t1, $v0
	
	add $t2, $t0, $t1
	
	li $v0, 1
	move $a0, $t2
	syscall
```
> - 5.2  
```assembly
.data
	name: .asciiz "\nLuis Eduardo Sotoj Teque"
.text
    main:
	li $v0, 4
	la $a0, name
	syscall
```

> ## **Thursday**  
> 1. Search for real word applications of Javascript.  
> &nbsp;&nbsp;&nbsp;&nbsp; Slack was build with JavaScript.  
> 2. (optional but great) Watch this video.  
> &nbsp;&nbsp;&nbsp;&nbsp; Done.  
> 3. (optional but great) Watch this video.  
>  &nbsp;&nbsp;&nbsp;&nbsp; Done.  
>  4. Follow the github course, you can find it here.  
>  &nbsp;&nbsp;&nbsp;&nbsp; Done.  
>  


> # **Week 2**  
> ## **Monday**  
> 1. Follow the github course.  
> &nbsp;&nbsp;&nbsp;&nbsp; Done.  
> 2. Watch this video.  
> &nbsp;&nbsp;&nbsp;&nbsp; Done.
> 3. Read this.  
> &nbsp;&nbsp;&nbsp;&nbsp; Done.
> 4. Create an account in Codewars.  
> &nbsp;&nbsp;&nbsp;&nbsp; User: https://www.codewars.com/users/lsotoj


> ## **Tuesday**  
> 1. https://www.codewars.com/kata/50654ddff44f800200000004  
```javascript
function multiply(a, b){
  return a * b;
};
```  
> 2. You'll be given a string, and have to return the sum of all characters as an int. The function should be able to handle all ASCII characters.  
```javascript
function uniTotal (string) {
let counter = 0;
  
  for (let i = 0; i < string.length; i++){
    counter += string.charCodeAt(i);
  }
  return counter;
}
```  
> 3. Write a function get_char() / getChar() which takes a number and returns the corresponding ASCII char for that value.  
> Example:  
```javascript
get_char(65)
```  
> should return:  
```javascript
'A'
```  
> Solution:  
```javascript
function getChar(c){
  return String.fromCharCode(c)
}
```  
> 4. Implement a function that adds two numbers together and returns their sum in binary. The conversion can be done before, or after the addition.  
> The binary number returned should be a string.  
>Solution:  
```javascript
function addBinary(a,b) {
  let c =  a + b
  
  let cBinary = c.toString(2)
  
  return cBinary
}
``` 
> 5. Create a function finalGrade, which calculates the final grade of a student depending on two parameters: a grade for the exam and a number of completed projects. This function should take two arguments: exam - grade for exam (from 0 to 100); projects - number of completed projects (from 0 and above);  
> This function should return a number (final grade). There are four types of final grades:  
> 100, if a grade for the exam is more than 90 or if a number of completed projects more than 10.  
> 90, if a grade for the exam is more than 75 and if a number of completed projects is minimum 5.  
> 75, if a grade for the exam is more than 50 and if a number of completed projects is minimum 2.  
> 0, in other cases  
> Solution:
```javascript
function finalGrade (exam, projects) {
  if(exam > 90 || projects > 10) {
    
    return 100;
  }
  
  if(exam > 75 && projects >= 5) {
     return 90;
  }
  
  if(exam > 50 && projects >= 2) {
    return 75
    
  }
  return 0;
}
``` 
 
> ## **Wednesday**  
> 1. The purpose of this kata is to work out just how many bottles of duty free whiskey you would have to buy such that the saving over the normal high street price would effectively cover the cost of your holiday.  
> You will be given the high street price (normPrice), the duty free discount (discount) and the cost of the holiday.  
> For example, if a bottle cost £10 normally and the discount in duty free was 10%, you would save £1 per bottle. If your holiday cost £500, the answer you should return would be 500.  
> All inputs will be integers. Please return an integer. Round down.  
```javascript
function dutyFree(normPrice, discount, hol){
  let amount = hol / (normPrice * (discount * 0.01))
  amount = Math.floor(amount)
  
  return amount;
}
```  
> 2. Your function takes two arguments:  
> current father's age (years)  
> current age of his son (years)  
> Сalculate how many years ago the father was twice as old as his son (or in how many years he will be twice as old).  
```javascript
function twiceAsOld(dadYearsOld, sonYearsOld) {

  return Math.abs(dadYearsOld - (sonYearsOld * 2))
  
}
``` 
> 3. Your task is to write a function called valid_spacing() or validSpacing() which checks if a string has valid spacing. The function should return either True or False. For this kata, the definition of valid spacing is one space between words, and no leading or trailing spaces. Below are some examples of what the function should return.
```javascript
'Hello world' = true
' Hello world' = false
'Hello world  ' = false
'Hello  world' = false
``` 
> Solution:  
```javascript
function validSpacing(s) {
  let last = s[0];
  if(s[0] === " " || s[s.length - 1] === " "){
    return false
  }
  
  for(let i =1; i < s.length; i++){
    if(last === " " && last === s[i]){
      return false
    }
    last = s[i];
  }
  
  return true;
}
``` 
> 4. Given a string of digits, you should replace any digit below 5 with '0' and any digit 5 and above with '1'. Return the resulting string.  
> Solution:  
```javascript
function fakeBin(x){
  let result = [];
  for(let i = 0; i < x.length; i++) {
    if(parseInt(x[i], 10) < 5)
      result.push('0')
    
    if(parseInt(x[i]) >= 5)
       result.push('1');
  }
  return result.join(""); 
}
```


> # **Week 3**  
> ## **Monday** 
> 1. https://www.codewars.com/kata/5266876b8f4bf2da9b000362  
> Solution:  
```javascript
function likes(names) {
  // TODO
  if(names.length === 0)
    return "no one likes this"
    
  if(names.length === 1) {
    return `${names[0]} likes this`;
  }
  
  if(names.length === 2) {
    return `${names[0]} and ${names[1]} like this`
  }
  
  if(names.length === 3) {
    return `${names[0]}, ${names[1]} and ${names[2]} like this`
  }
  
  if(names.length >= 4) {
    return `${names[0]}, ${names[1]} and ${names.length - 2} others like this`
  }
}
```
> 2. https://www.codewars.com/kata/526571aae218b8ee490006f4  
> Solution:  
```javascript
var countBits = function(n) {
  let count = 0
  let strNumber = n.toString(2)
  
  for(let i = 0; i < strNumber.length; i++) {
    if(strNumber[i] === '1')
      count++
  }
  
  return count
};
```
>  3. https://www.codewars.com/kata/54b724efac3d5402db00065e  
> Solution:
```javascript
decodeMorse = function(morseCode){
  morseCode = morseCode.trim().split(" ");
  let newWord = ""
  
  for(let i = 0; i < morseCode.length; i++) {
    if(morseCode[i] === "" && morseCode[i + 1] === "") {
      newWord += " "
      continue;
    }
      
    if(morseCode[i] === "") 
      continue;
    newWord += MORSE_CODE[morseCode[i]];
  }
  
  return newWord;
}
```  

> ## **Tuesday** 
> Your task is to sort a given string. Each word in the string will contain a single number. This number is the position the word should have in the result.
> Note: Numbers can be from 1 to 9. So 1 will be the first word (not 0).  
> If the input string is empty, return an empty string. The words in the input String will only contain valid consecutive numbers.  
> Solution  
```javascript
function order(words){
  let regex = /\d/
  let arr = words.split(" ");
  let aux = [];
  
  for(let i = 0; i < arr.length; i++) {
    let num = parseInt(arr[i].match(regex))
    aux[num - 1] = arr[i];
  }
  
  return aux.join(" ")
}
```

> 2. Count the number of Duplicates.  
> Write a function that will return the count of distinct case-insensitive alphabetic characters and numeric digits that occur more than once in the input string. The input string can be assumed to contain only alphabets (both uppercase and lowercase) and numeric digits.  
> Solution:  
```javascript
function duplicateCount(text){
  let counter = 0;
  text = text.toLowerCase().split("").sort();
  
  for(let i = 0; i < text.length; i++) {
    if(text[i] === text[i + 1]) {
      counter++;
      while(text[i] === text[i + 1]) {
        i++;
      }
    }
  }
  
  return counter;
}
```

> 3. Move the first letter of each word to the end of it, then add "ay" to the end of the word. Leave punctuation marks untouched.  
```javascript
function pigIt(str){
  
    str = str.split(" ");
   str = str.map(word => {
        if(/[!¡?¿]/.test(word)){
            return word;
        }
        word = word  + word[0] + "ay";
        word = word.slice(1);
        return word;
    });
    return str.join(" ");
}
```
> ## **Wednesday** 
> 1. Write a function that takes a string of parentheses, and determines if the order of the parentheses is valid. The function should return true if the string is valid, and false if it's invalid.  
> Solution:  
```javascript
function validParentheses(parens) {
  let arr = parens.split("");
  let open= 0;
  console.log(arr);
  for(let i = 0; i < arr.length; i++) {
    if(arr[i] === "(")
      open++;
    
    if(arr[i] === ")")
      open--
      
    if(open < 0) 
      return false
  }
  
  return open === 0;
```
> 2. Complete the method/function so that it converts dash/underscore delimited words into camel casing. The first word within the output should be capitalized only if the original word was capitalized (known as Upper Camel Case, also often referred to as Pascal case).  
```javascript
function toCamelCase(str){
  let arr = str.split(/[\-_]/);
  let result = [arr[0]]
  for(let i = 1; i < arr.length; i++) {
    result.push(arr[i][0].toUpperCase() + arr[i].slice(1))
  }
  return result.join("")
}
```
> 3. Implement the function unique_in_order which takes as argument a sequence and returns a list of items without any elements with the same value next to each other and preserving the original order of elements.  
> Solution:
```javascript
var uniqueInOrder=function(iterable){
  if(!iterable)
    return []
  
  iterable = [...iterable]

  let result = [iterable[0]];
  for(let i = 1; i < iterable.length; i++) {
    if (result[result.length - 1] != iterable[i])
        result.push(iterable[i])
  }
  return result
}
```
> ## **Thursday**
> 1. In this kata you have to write a method that folds a given array of integers by the middle x-times.  
>  Solution:
```javascript
function foldArray(array, runs) {
  let aux = [...array];
  
  while(runs !== 0) {
    let split = Math.trunc(aux.length / 2);
    let newArr = aux.splice(aux.length - split, split);
    for(let i = 0; i < newArr.length; i++) {
      aux[i] = aux[i] + newArr[newArr.length - 1 - i]
    }
    runs--
  }  
  return aux;
}
```  
> 
> 2. You want to create secret messages which can be deciphered by the Decipher this! kata. Here are the conditions:  
> Your message is a string containing space separated words.  
> The first letter must be converted to its ASCII code.  
> The second letter must be switched with the last letter.  
```javascript
function encryptThis(message) {
  let arr = message.split(" ");
  
  arr.forEach((element, index, fullArr) => {
    let aux = element.split("");
    aux[0] = aux[0].charCodeAt(0);
    let ultima = aux[1];
    aux[1] = aux[aux.length - 1];
    aux[aux.length - 1] = ultima;
    fullArr[index] = aux.join("");
  })
  
  return arr.join(" ")
}
```  
> 3. Given: an array containing hashes of names.  
>
> Return: a string formatted as a list of names separated by commas except for the last two names, which should be separated by an ampersand.  
> Solution:
```javascript
function list(names){
  //your code here
  let result = "";
  return names.reduce((acc, current, idx) =>{ return idx === names.length - 1? acc + " & " + current.name: acc + ", " + current.name
  },"").slice(2).trim()
}
```  
> # **Week 4**
> ## **Tuesday**
> 2. Typescript object type.       
> Given the data, define the interface "User" and use it accordingly.  
```javascript
export type User = {name: string, age: number, occupation: string};

export const users: User[] = [
    {
        name: 'Max Mustermann',
        age: 25,
        occupation: 'Chimney sweep'
    },
    {
        name: 'Kate Müller',
        age: 23,
        occupation: 'Astronaut'
    }
];

export function logPerson(user: User) {
    console.log(` - ${user.name}, ${user.age}`);
}

console.log('Users:');
users.forEach(logPerson);


``` 
> 4. Typescript union types.  
> Solution:

```typescript

interface User {
    name: string;
    age: number;
    occupation: string;
}

interface Admin {
    name: string;
    age: number;
    role: string;
}


export type Person = User | Admin;

export const persons: Person[] /* <- Person[] */ = [
    {
        name: 'Max Mustermann',
        age: 25,
        occupation: 'Chimney sweep'
    },
    {
        name: 'Jane Doe',
        age: 32,
        role: 'Administrator'
    },
    {
        name: 'Kate Müller',
        age: 23,
        occupation: 'Astronaut'
    },
    {
        name: 'Bruce Willis',
        age: 64,
        role: 'World saver'
    }
];

export function logPerson(user: Person) {
    console.log(` - ${user.name}, ${user.age}`);
}

persons.forEach(logPerson);


```
> 5. Typescript in operator.   
> Solution:

```typescript
interface User {
    name: string;
    age: number;
    occupation: string;
}

interface Admin {
    name: string;
    age: number;
    role: string;
}

export type Person = User | Admin;

export const persons: Person[] = [
    {
        name: 'Max Mustermann',
        age: 25,
        occupation: 'Chimney sweep'
    },
    {
        name: 'Jane Doe',
        age: 32,
        role: 'Administrator'
    },
    {
        name: 'Kate Müller',
        age: 23,
        occupation: 'Astronaut'
    },
    {
        name: 'Bruce Willis',
        age: 64,
        role: 'World saver'
    }
];

export function logPerson(person: Person) {
    let additionalInformation: string;
    if ('role' in person) {
        additionalInformation = person.role;
    } else {
        additionalInformation = person.occupation;
    }
    console.log(` - ${person.name}, ${person.age}, ${additionalInformation}`);
}

persons.forEach(logPerson);

``` 
> 6. Given an array of integers, find the one that appears an odd number of times.  
> Solution:  

```javascript
function findOdd(A) {
    //happy coding!
    let numbers = {}
    A.forEach(element => {
        if(element in numbers){
            numbers[element]++;
        } else {    
            numbers[element] = 1;
        }
    });

    function isOdd(num){
        return parseInt(num) % 2 == 0? false: true;
    }
    for(let i in numbers){
       if(isOdd(numbers[i])) return parseInt(i)
    }
}
```
> 7. Write a function that takes in a string of one or more words, and returns the same string, but with all five or more letter words reversed (Just like the name of this Kata). Strings passed in will consist of only letters and spaces. Spaces will be included only when more than one word is present.  
> Solution:  
```javascript
function spinWords(string){
    return string.split(" ").map(word => {
        if(word.length >= 5) return word.split("").reverse().join("");
        return word
    }).join(" ");
}
```
