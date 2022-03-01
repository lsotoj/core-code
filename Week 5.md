# **Monday**    
2. Complete the square sum function so that it squares each number passed into it and then sums the results together.  
+ Solution
```typescript
export function squareSum(numbers: number[]): number {
    return numbers.reduce((sum, current) => {
      return  sum + Math.pow(current, 2);
    }, 0);
}
```
<br/><br/>
3. In a small town the population is p0 = 1000 at the beginning of a year. The population regularly increases by 2 percent per year and moreover 50 new inhabitants per year come to live in the town. How many years does the town need to see its population greater or equal to p = 1200 inhabitants?  
+ Solution:  
```typescript
export class G964 {

    public static nbYear = (p0: number, percent: number, aug: number, p: number) => {
        // your code
        let yearlyPopulation: number = p0;
        let years: number = 0;
        while (yearlyPopulation <  p) {
            yearlyPopulation = yearlyPopulation + (yearlyPopulation * (percent/100)) + aug;
            years++;
        }
        return years;
    }
}
```
<br/><br/><br/>
4. This time no story, no theory. The examples below show you how to write function accum:  
+ Solution:  
```typescript
export function accum(s: string): string {
    let arr: string[] = s.split("");
    return arr.reduce((acc: string, current: string, index: number) => {
        
        return acc + "-" + current.toUpperCase() + current.toLowerCase().repeat(index);
    }, "").slice(1);

}
```
<br/><br/><br/>
5. Wolves have been reintroduced to Great Britain. You are a sheep farmer, and are now plagued by wolves which pretend to be sheep. Fortunately, you are good at spotting them.  
+ Solution:  
```typescript
export function warnTheSheep(queue: string[]): string {
    if(queue[queue.length - 1] === "wolf") {
        return "Pls go away and stop eating my sheep"
    } else {
        let pos:number = queue.length - queue.indexOf("wolf") - 1;
        return `Oi! Sheep number ${pos}! You are about to be eaten by a wolf!`
    }
}
```
<br/><br/><br/><br/>

# **Tuesday**   
<br/><br/>  
1. "A divisibility rule is a shorthand way of determining whether a given integer is divisible by a fixed divisor without performing the division, usually by examining its digits."  
+ Solution:  
 ```typescript
 export function thirt(n: number): number {
    // your code
    let last: number = n;
    let num: string[] = n.toString().split("");
    let sequence: number[] = [];
    let flag: number = 0;
    for(let i = 0; i < num.length; i++) {
        sequence.push(Math.pow(10, i) % 13);
    }


    while(last !== flag) {
        flag = last;
        last = num.reverse().reduce((sum, current, index) => {
            return (parseInt(current) * sequence[index]) + sum;
        }, 0);
        num = last.toString().split("");

    }
    return last;
}
 ```
 <br/>
 2. Given a positive integer n written as abcd... (a, b, c, d... being digits) and a positive integer p.  

+ we want to find a positive integer k, if it exists, such as the sum of the digits of n taken to the successive powers of p is equal to k * n.  
+ Solution:  
```typescript
export class G964 {

    public static digPow = (n: number, p: number) => {
        let arr: string[] = n.toString().split("")
        let top: number;

        top = arr.reduce((sum: number, current: string, index: number) => {
            return sum + Math.pow(parseInt(current), p++)
        }, 0);
        if(top === n) return 1
        if(!Number.isInteger(top / n)) return -1
        return top / n;
    }
}
```
 <br/> <br/>
3. Write a function that takes a string of braces, and determines if the order of the braces is valid. It should return true if the string is valid, and false if it's invalid.  
+ Solution:  
```typescript
export function validBraces(braces: string): boolean {
   const arr: string[] = braces.split("");
    let count: number = 0;
    let flag: boolean = false;

    for(let i = 0; i < arr.length; i++) {
        if(arr[i] === ")") {
            count--;
            if(arr[i - 1] === "(") flag = true;
        } else if(arr[i] === "]") {
            count--;
            if(arr[i - 1] === "[") flag = true;
        } else if(arr[i] === "}") {
            count--;
            if(arr[i -1] === "{") flag = true;
        } else { count++; }
        if(count < 0) return false;
    }
    return flag;
}
```

# **Wednesday**   
<br/><br/>  
1. The goal of this exercise is to convert a string to a new string where each character in the new string is "(" if that character appears only once in the original string, or ")" if that character appears more than once in the original string. Ignore capitalization when determining if a character is a duplicate.  
* Solution:  
```typescript
export function duplicateEncode(word: string){
    // ...
    let arr = word.toLocaleLowerCase().split("")
    let dic: any = {};
    for(let i = 0; i < arr.length; i++) {
        if(arr[i] in dic) dic[arr[i]]++;
        else dic[arr[i]] = 1;
    }
    return arr.map((word) => dic[word] > 1? ")": "(").join("");
}
```
 <br/><br/>  
2. Given an array of integers, find the one that appears an odd number of times. There will always be only one integer that appears an odd number of times.  
* Solution:
```typescript
export const findOdd = (xs: number[]): number => {
    // happy coding!
    let dict: any = {};
    for(let i = 0; i < xs.length; i++) {
        if(xs[i] in dict) dict[xs[i]]++;
        else dict[xs[i]] = 1;
    }

    for(let word in dict) {
        if(dict[word] % 2 !== 0) return parseInt(word);
    }
    return 0;
};
```
<br/><br/>  
3. Given two arrays of strings a1 and a2 return a sorted array r in lexicographical order of the strings of a1 which are substrings of strings of a2.  
+ Solution:  
```typescript
export class G964 {
    public static inArray(a1: string[], a2: string[]): string[] {
      // your code
        let arr: string[]= [];
        let dict: any = {};

        a1.forEach((elemento1) => {
            a2.forEach((elemento2) => {
                if(elemento2.includes(elemento1) && !(elemento1 in dict)) dict[elemento1] = 1;
            })
        })

        return Object.keys(dict).sort();
    }
}
```
<br/><br/>  
4. Let us consider this example (array written in general format): ```ls = [0, 1, 3, 6, 10]```  
The corresponding sums are (put together in a list): [20, 20, 19, 16, 10, 0]  
+ Solution:
```typescript
export function partsSums(ls: number[]): number[] {
    console.log(ls)
    let sum: number = ls.reduce((sum, current) => sum + current, 0);
    let arr: number[] = [];
    arr.push(sum);
    for(let i = 1; i <= ls.length; i++) {
        sum -= ls[i - 1];
        arr.push(sum)
    }
    return arr;
}
```

<br/><br/>  
5. You are given an array(list) strarr of strings and an integer k. Your task is to return the first longest string consisting of k consecutive strings taken in the array.  
+ Solution:  
```typescript
export function longestConsec(strarr: string[], k: number): string {

    if(k === 1) strarr.sort((a, b) => b.length - a.length)[0];
    if(strarr.length === 0 || k < 0 || k > strarr.length) return "";
    
      let newArr: string[] = strarr.map((current, index, arr) => {
        return arr.slice(index, index + k).join("");
      });

    let greatest: number = newArr.map(el => el.length).sort((a, b) => b-a)[0]
    return newArr.find( el => el.length === greatest);
}
```
<br/><br/><br/>
# **Thursday**  
1. Tile Using Typescript.  
+ Solution: 
[Code](https://github.com/lsotoj/CoreCodeChallenges/blob/main/week5/tile/Tile.ts)
<br/><br/>
2. Time Using Typescript.  
+ Solution: 
[Code](https://github.com/lsotoj/CoreCodeChallenges/blob/main/week5/time/Time.ts)

<br/><br/>
3. Rational Using Typescript.  
+ Solution: [Code](https://github.com/lsotoj/CoreCodeChallenges/blob/main/week5/rational/Rational.ts)

