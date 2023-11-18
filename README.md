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
        if (!this.top) return null
        const holdingPointer = this.top;
        this.top = this.top.next;
        this.length--
        return this
    }
}
```
