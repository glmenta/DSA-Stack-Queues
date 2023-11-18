### Stacks and Queues are linear DS; traverse data one-by-one

### Beginning or end of data structures 

### Stack => LIFO; STACK OF PLATES
    ```
    Lookup O(n); pop/push/peek O(1)
    
    Examples:
      -Browser History; going back and forth between websites
      -Undo options

    Store prev state in memory => can access that 
    ```
### Queue => FIFO; QUEUE IN LINE
    ```
    Lookup O(n); enqueue/dequeue/peek O(1)

    Examples:
      -Uber ride; priority
      -Waitlist for restaurant
      -Printer printing items
      
    ```


### STACK Implementation using LL
```
class Stack {
    constructor() {
        this.top = null;
        this.bottom = null;
        this.length = 0;
    }
    peek() {
        return this.top
    }
    push(val) {
        const newNode = new Node(val)
        if (this.length === 0) {
            this.top = newNode;
            this.bottom = newNode;
        } else {
            holdingPointer = this.top;
            this.top = newNode;
            this.top.next = holdingPointer;
            this.length++
            return this
    }
    pop() {
        if (!this.top) return null;
        if (this.top === this.bottom) this.bottom = null;
        const holdingPointer = this.top;
        this.top = this.top.next;
        this.length--
        return this
    }
}
```

### Stack Implementation in Arrays
```
class Stack {
    constructor() {
        this.array = [];
    }
    peek() {
        this.array[this.array.length - 1];
    }
    push(val) {
        this.array.push(val);
    }
    pop() {
        this.array.pop();
        return this;
    }
}

```

### Queue Implementation 
```
class Queue {
    constructor() {
        this.first = null;
        this.last = null;
        this.length = 0;
    }
    peek() {
        return this.first
    }
    enqueue(val) {
        const newNode = new Node (val)
        if (this.length === 0) {
            this.first = newNode;
            this.last = newNode;
        } else {
            this.last.next = newNode;
            this.last = newNode;
            this.length++
            return this
        }
    }
    dequeue() {
        if (!this.first) return null;
        if (this.first === this.last) this.last = null;
        this.first = this.first.next;
        this.length--
        return this
    }
}
```
