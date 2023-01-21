## Recursion
Recursion is where a function calls itself. 

every recursive functions has two parst:
- ***base case*** --> tell the recursive function when it stop. (if you write an incorrect base case it's will make an infinite loop)
- ***recursive case*** --> when the function calls itself.

![image](https://user-images.githubusercontent.com/105928025/213844691-fd41b3a7-5141-46ff-842c-2682b63ea8e0.png)

![image](https://user-images.githubusercontent.com/105928025/213844711-fd1054fd-b15d-4802-ae9c-cc3dd7ac7486.png)

## Stack
The stack is a simple data structure that follows the LIFO (Last In First Out) and it has two operations: (***push*** , ***pop***).

computer uses **call stack** to save the variables for multiple functions.
The computer allocates a box of memory for that function call. Every time you make a function call, your computer saves the values for all the variables for that call in memory and the computer is using the stack for these boxes. when you call another function the new box is added on top of the first one, when the current function is completed the box on top of the stack returns the value and gets popped off.

if you have function *fun1* and it has function *fun2* when you call the *fun2* the *fun1* was ***partially completed*** .

when you call a function from another function, the calling function is paused in a partially completed state and all the values of the variables for this function are still stored in memory.

### The call stack with recursion
recursive function use the call stack, the stack plays a big part in recursion 

using stack in convenient because you don't have to keep tracking every case by yourself, the stack dose it for you, but there's a cost : saving all that info can take up a lot of memory. At this point, you have two options:
- you can rewrite your code to use a loop instead.
- You can use something called tail recursion.