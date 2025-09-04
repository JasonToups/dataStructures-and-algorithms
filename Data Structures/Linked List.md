Linked Lists are The First “Real” #DataStructure

> It’s available for every language instead of Javascript.

It’s a **Node-based** *data structure*, *not Node.js*

![[Screenshot 2025-08-26 at 4.18.43 PM.png]]

Each of the **Nodes have properties**:
- the **value** of the node
- the **next** node in the Linked List

## Singly-linked List

A **singly-linked list** means that you can only go forward in the linked list, since we *only* have the *next* property on the node.

```js
Node<T> {
	val: T
	next?: Node<T>
}
```

> To *traverse the linked list*, you have to **check** each node, to get to the **next** node.

## Doubly-linked List

A **doubly-linked** list means that we have 3 properties:
- the **value** of the node
- the **next** node in the Linked List
- the **previous** node in the Linked List
```js
Node<T> {
	val: T
	next?: Node<T>
	prev?: Node<T>
}
```

Now that we know the previous and next nodes for each node, we can walk forwards & backwards.

## Deletion & Insertion

![[Screenshot 2025-09-04 at 1.18.44 PM.png]]

### Insertion

#### Singly Linked
When we want to **add the F Node**:

We have to take the *Next property of A*, and *point it to F*.

Then take the *Next property of F*, and *point it to B*.

#### Doubly Linked

When we want to **add the F Node**:

We have to take the *Next property of A*, and *point it to F*.

Then take the *Next property of F*, and *point it to B*.
Then take the *Prev property of F*, and *point it to A*.

Finally take the *Prev property of F*, and *point it to B*

#### How is this different than adding an element to an Array?

Since the elements in a linked list, *are linked*, we only have to adjust the Nodes that the operation affects.

In an **array**, when we want to **add or remove** an element, *all of the other elements* in an array have to be **adjusted**, because *their index changes*.

I’m updating this note to see if free file sync will trigger