Big O is a way to categorize your algorithms time or memory requirements based on input. It’s not meant to be an exact measurement. It’s usually a worst-case evaluation.
## Why do we use it. 

It helps us make decisions about what data structures and algorithms to use.
## Big O, said differently

As your input grows, how fast does computation or memory grow?
## In the Real World

Obviously memory growing is not computationally free, but in the matter of thking about algorithms, we don’t necessarily think about that. 

In languages like Go or Javascript, you pay even heavier penalities because the memory can be kept around, grows faster, and causes complete halts in your program for cleanup.
## for example

### simplist trick for complexity

> Look for Loops!

```typescript
function sum_char_codes(n: string): number {
	let sum = 0;
	for (let i = 0; i < n.length; ++i) {
		sum += n.charCodeAt(i);
	}
	return sum;
}
```

What’s the runtime?

- For every 1 more unit of string, we get one more unit of time.
- We have an N relationship. 

**O(N)** time complexity.
## more complex example

If the previous was O(N), what’s this one?

```typescript
function sum_char_codes(n: string): number {
	let sum = 0;
	for (let i = 0; i < n.length; ++i) {
		sum += n.charCodeAt(i);
	}
	for (let i = 0; i < n.length: ++i) {
		sum += n.charCodeAt(i);
	}
	
	return sum;
}
```

it’s **O(2N)**
## nested loop example

```typescript
function sum_char_codes(n: string): number {
	let sum = 0;
	for (let i = 0; i < n.length; ++i) {
		sum += n.charCodeAt(i);
		// Capital E
		if (charCode = 69) {
			return sum;
		}
	}
	
	return sum;
}
```

It’s still **O(N)**, since if we’re considering worst-case scenario, the character might not exist.
## Important Concepts

1.  **Growth** is with respect to the `input`.
2. **Constants** are *dropped*.
3. **Worst case** is *usually* the way we measure.

## Big O Complexity Chart

![[Screenshot 2025-08-20 at 9.26.12 PM.png]]

- O(1)
- O(log N)
- O(N)
- O(N log N)
- O(N^2)
- O(2^N) - can’t run on traditional computers
- O(N!) - can’t run on traditional computers

## O(N^2) Example

```typescript
function sum_char_codes(n: string): number {
	let sum = 0;
	for (let i = 0; i < n.length; ++i) {
		for (let j = 0; j < n.length; ++j) {
			sum += charCode;
		}
	}
	
	return sum;
}
```

since we have a loop within a loop, it’s N squared, or N to the 2nd power, **O(N^2)**

## O(N^3) Example

```typescript
function sum_char_codes(n: string): number {
	let sum = 0;
	for (let i = 0; i < n.length; ++i) {
		for (let j = 0; j < n.length; ++j) {
			for (let k = 0; k < n.length; ++k) {
				sum += charCode;
			}
		}
	}
	
	return sum;
}
```

since we have a loop within a loop, within a loop, it’s N cubed, or N to the 3nd power, **O(N^3)**

## O(N log N) 

- #quicksort Algo (I will link the file when it’s created)

## O(log N)

- Binary Search Trees

## O(sqrt(N))

- This hasn’t been mentioned, because it comes up so rarely.