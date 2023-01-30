## Hash functions
A hash function is a function where you put in a string and you get back a number.

![image](https://user-images.githubusercontent.com/105928025/215309232-891cfd22-02f7-4f2b-bf24-bb5511d76825.png)

in technical terminolgy : hash function ***maps string to numbers"***.

some requirements for a hash function:
- it needs to be consostent. if you put in "apple" and get back 4 , every time you put in "apple" , you should get 4.

- it should map different words to different numbers.

## Hash table 
hash tables are most complex data structure that use hash function to  intelligently figure out where to store elements.

A hash table has keys and values.

### Use Cases

#### Using hash tables for lookups

Hash tables are great when you want to 
- Create a mapping from one thing to another thing
- Look something up

#### Preventing duplicate entries

Checking for duplicates is very fast with a hash table. 

#### Using hash tables as a cache

Caching is a common way to make things faster. All big websites use caching. And that data is cached in a hash

### Performance 
Hash tabels take O(1) for everything in the average case and take O(n) in worst case.

![image](https://user-images.githubusercontent.com/105928025/215402605-4328e82a-0fb4-484a-bc5e-52e84869375c.png)

in worst case hash tabels are slow for evrything. So it’s important that you don’t hit worst-case performance with hash tables. And to do that, you need to avoid collisions.

    Collisions: two keys have been assigned the same number (slot) and he simplest way to deal with collisions is this: if multiple keys map to the same slot, start a linked list at that slot.

To avoid collisions, you need :
- A low load factor.
- A good hash function.

#### Load factor
Load factor measures how many empty slots remain in your hash table. And hash table use an array for storage, so you count the number of occupied slots in an array.

    load factor = (number of items in the hash table / total number of slots)

***Having a load factor greater than 1 means you have more items than slots in your array.***
In this case you need to add more slots to your hash table. This is called ***resizing***

- First you create a new array that's bigger *The rule of thumb is to make an array that is twice the size and a good rule of thumb is, resize when your load factor is greater than 0.7*

- Re-insert all of those items into this new hash table using the hash function

*Resizing is expensive, and you don’t want to resize too often. But averaged out, hash tables take  (1) even with resizing.*

#### Good hash function
A good hash function distributes values in the array evenly.

![image](https://user-images.githubusercontent.com/105928025/215405983-1c7db6e6-ff7c-4af1-926e-2dc2250f6cbe.png)

A bad hash function groups values together and produces a lot of collisions.

![image](https://user-images.githubusercontent.com/105928025/215406104-15387ab3-a169-4625-b430-26ca29c9a6d6.png)

hash tables use SHA function *Secure Hash Algorithm* 

SHA: is a cryptographic hash function which takes an input and produces a 160-bit (20-byte) hash value and the value in a hexadecimal format.

    EX: 
    Input : hello world 
    Output : 2aae6c35c94fcfb415dbe95f408b9ce91ee846ed

SHA are used in many applications such: Comparing files , Checking passwords.