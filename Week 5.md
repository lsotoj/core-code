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
