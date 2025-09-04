# Queue Explained

The #Queue is a *fundamental  #data_structure*.
## Queue Properties
### FIFO (First In, First Out)
- The *first element added* is the *first one removed* — like people waiting in line.
- In Breadth First Search, this means you process nodes in the *order you discovered them*.
- Items are always processed in the exact order they were inserted.
### Two main operations

#### 1. Enqueue → Add an element to the end (tail) of the queue

```js
queue.push(item);
```
#### 2. Dequeue → Remove the element from the front (head) of the queue

```js
const item = queue.shift();
```
### other operations

#### 3. Peek (optional in BFS) Look at the front element without removing it.
```js
const item = queue[0];
```
#### 4. Empty check - You often loop while the queue is not empty:

```js
while (queue.length > 0) { ... }
```
## Why BFS Needs a Queue

- When you **visit a node**, you *enqueue its children*.
- Then you **dequeue the next node** *from the front,* which ensures you **finish all nodes on the current level** before *moving deeper*.

## My Docs

[[Breadth First Search]]
[[Binary Tree Traversal]]