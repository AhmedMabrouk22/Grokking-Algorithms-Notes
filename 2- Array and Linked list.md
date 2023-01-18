## How memory works
Your computer memory looks like a giant set of drawers and each time you want to store an item in memory, you ask the computer for some space, and it gives you an address where you can store your item. If you want to store multiple items, there are two basic ways to  do so: ***arrays and lists***

![image](https://user-images.githubusercontent.com/105928025/212747052-b20a9135-eefd-4ad3-8b45-2c0561b7f014.png)

*fe0ffeeb is the address of a slot in memory.*

## Arrays and linked lists

### Arrays
Using an array means all your tasks are stored contiguously (right next to each other) in memory, but you must specify the size of the array and you not be able to add new items or change the size.

![image](https://user-images.githubusercontent.com/105928025/212747831-90b954c4-b528-4566-b961-640dd04048cc.png)

when using an array you should be aware of a couple of downsides: 
- You may not need the extra slots that you asked for, and then that memory will be wasted. You aren’t using it, but no one else can use it either.

- You may add more than 10 items to your task list and have to move anyway.

In array you know the address for every item in your array , and you can access any item by his address ***(random access)***

![image](https://user-images.githubusercontent.com/105928025/212816919-c841f24e-797a-43a9-b38a-f798fe8a1bfc.png)

The elements in an array are numbered. This numbereing starts from 0 not 1.

The position of an element is called ***index*** 

![image](https://user-images.githubusercontent.com/105928025/213095762-23da6018-8207-4244-9166-80fa996247d6.png)


### Linked lists
With linked lists, your items can be anywhere in memory. Each item stores the address of the next item in the list. A bunch of random memory addresses are linked together.

![image](https://user-images.githubusercontent.com/105928025/212816134-9a40faef-a6af-4642-8cbf-5ac196a89d55.png)

Linked lists are great if you’re going to read all the items one at a time: you can read one item, follow the address to the next item, and so on. But if you’re going to keep jumping around, linked lists are terrible ***(no random access)*** . Because the elements aren’t next to each other

#### Common operations in array and linked list

1. Reading:
    - Array allow ***random access*** which means you can jump directly to the i-th element

    - Linked list allow only ***sequential acces*** which means reading the elements one by one 

2. Insertion:

    What’s better if you want to insert elements in the middle ?
    - in linked list it's as easy as changing what the previous element point to.

    - in array you have to shift all the rest of the element down, and if there's no space, you might have to copy everything to a new location.

3. Deletions:
    - in linked list you just need to change what the previous element point to 

    - in array everything needs to be moved up when you delete an element.

![image](https://user-images.githubusercontent.com/105928025/213097957-58cb869a-fc68-40ac-9494-c26da37451e0.png)




