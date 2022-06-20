# Stacks and Queues

## **Stacks**

A stack is a data structure that consists of `Nodes`. Each Node references the `next Node` in the stack, but does `not `reference its `previous`.

**Stacks follow these concepts:**

- **FILO:** First In Last Out

This means that the first item added in the stack will be the last item popped out of the stack.

- **LIFO:** Last In First Out

This means that the last item added to the stack will be the first item popped out of the stack.

---
### **Push O(1)**

When adding a Node, you `push` it into the stack by assigning it as the new top, with its `next` property equal to the original `top`.

`Pushing` a Node onto a stack will always be an **`O(1)`** operation. This is because it takes the same amount of time no matter how many Nodes **`(n)`** you have in the stack.

[To know how adding read...](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/stacks_and_queues.html)


### **Pop O(1)**

Popping a Node off a stack is the action of `removing`a Node from the` top`. When conducting a pop, the top Node will be re-assigned to the Node that lives below and the top Node is returned to the user.

Typically, you would check `isEmpty` before conducting a pop. This will ensure that an exception is not raised. Alternately, you can wrap the call in a try/catch block.

[To know how removing read...](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/stacks_and_queues.html)


### **Peek O(1)**

When conducting a `peek`, you will only be inspecting the `top Node` of the stack.

Typically, you would check `isEmpty` before conducting a peek. This will ensure that an exception is not raised. Alternately, you can wrap the call in a try/catch block.


### **IsEmpty O(1)**

This method to check if the stack IsEmpty or not.

---
---

## **Queue**

A Queue is a linear structure which follows a particular order in which the operations are performed. The order is First In First Out (FIFO). 

**Queues follow these concepts:**

- **FIFO:**  First In First Out

This means that the first item in the queue will be the first item out of the queue.

- **LILO:** Last In Last Out

This means that the last item in the queue will be the last item out of the queue.

### **Enqueue O(1)**

When you add an item to a queue, you use the `enqueue` action. This is done with an `O(1)` operation in time because it does not matter how many other items live in the queue` (n)`; it takes the same amount of time to perform the operation.

* The adding just form rear side 

[To know how adding read...](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/stacks_and_queues.html)

### **Dequeue O(1)**


When you remove an item from a queue, you use the `dequeue` action. This is done with an `O(1)` operation in time because it doesn’t matter how many other items are in the queue, you are always just` removing the front Node of the queue`.

* The removing just from front side.


Typically, you would check`isEmpty`before conducting a dequeue. This will ensure that an exception is not raised. Alternately, you can wrap the call in a try/catch block.

[To know how removing read...](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/stacks_and_queues.html)


### **Peek O(1)**

When conducting a peek, you will only be inspecting the` front Node` of the queue.

Typically, you want to check `isEmpty`before conducting a peek. This will ensure that an exception is not raised. Alternately, you can wrap the call in a try/catch block.


### **IsEmpty O(1)**

This method to check if the stack IsEmpty or not.

