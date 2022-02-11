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
