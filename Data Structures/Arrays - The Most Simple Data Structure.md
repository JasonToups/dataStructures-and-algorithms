If `const a = []` isn’t an array, what is it?

An #Array is a *contiguous memory space* that contains a *certain amount of bytes*.
## RAM

RAM is where all of our variables are stored.
RAM has a value and an address.
- **value** is *what’s* stored.
- **address** is *where* it’s stored.
### What’s Actually Stored in an Array

#RAM storage is measured in Bytes.
A #Byte is nothing more than 8 bits.
A #bit is a position that can store a digit. The digit is either a 0 or 1.
An #integer is stored as 4 bytes, (8bits x 4bytes) which is a 32 bit number.

## How Arrays are stored in RAM

#Arrays are stored contiguously.

### Integer Arrays

so the array:

`[ 1, 3, 5]`

is stored:

|         | RAM |     |     |
| ------- | --- | --- | --- |
| Value   | 1   | 3   | 5   |
| Address | $0  | $4  | $8  |
The address is incremented by 4, because each **integer value** is stored as *4 bytes*.

> Arrays are considered **the most simple data structure**

### ASCI Arrays

`[ a, b, c]`

is stored:

|         | RAM |     |     |
| ------- | --- | --- | --- |
| Value   | a   | b   | c   |
| Address | $0  | $1  | $2  |
The Address is incremented by 1, because **ASCI characters values** are stored as *1 byte*.

## How we alter and access data in Arrays

You can access values in arrays by their Index.

When you insert values in Arrays, you overwrite the values. 
- You cannot just add a value in an array.

You can’t actually delete a value in an array.

### BigO

When accessing values in an array, it’s constant time. `O(1)`
N does not grow.

