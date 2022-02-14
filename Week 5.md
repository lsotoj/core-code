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
