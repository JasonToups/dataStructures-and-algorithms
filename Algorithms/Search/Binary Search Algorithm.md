This second #algorithm is a bit of a doosy, but it’s definitely a basis for other algorithms we will encounter.

When presented with an #array, we should ask, ‘Is it ordered?’
- If your dataset is ordered, then you have different advantages.

If we have an ordered array, and we are looking for a specific value. 
If we start in the middle, and check that value, to determine which side of the array to check. Then check the middle of that side, and keep dividing the array in half, to check the middle value. Then we will eventually find the value that we want.

This **Binary Search** is `O(logN)` , since the runtime gets progressively smaller, the deeper into the array we go.
- Or, if we were *scanning the value* at the checked index, then it would be `0(NlogN)`.


## The Two Crystal Ball problem

Given two crystal balls that will break if dropped from high enough distance, determine the exact spot in which it will break in the most optimized way.

### What are our options?

Linear or Binary?

There is an array of falses, that eventually becomes true.

```javascript
O[false, false, false ... true]N
```

If we write a for loop, so then it’s Linear, so it’s `O(N)`.

If we check the middle, and it’s true, then we have to check the first half of the array and walk through our options.

But this time, we need to jump the square root of N.

So then our runtime is `O(sqrtN)` 

We broke down a Linear search problem, that can be solved with a different runtime, rather than `O(N)`.


### Solution

```javascript
export default function two_crystal_balls(breaks: boolean[]): number {
    const jmpAmount = Math.floor(Math.sqrt(breaks.length));

    let i = jmpAmount;
    for (; i < breaks.length; i += jmpAmount) {
        if (breaks[i]) {
            break;
        }
    }

    i -= jmpAmount;

    for (let j = 0; j <= jmpAmount && i < breaks.length; ++j, ++i) {
        if (breaks[i]) {
            return i;
        }
    }

    return -1;
}
```



 