## Divide & conquer
Divide and conquer algorithms are recursive algorithms used to reduce the big problem into small problems.

To solve a problem using D&C, there are two steps:
- Figure out the base case. This should be the simplest possible case.

- Divide or decrease your problem until it becomes the base case.

If you’re using D&C on a list, the base case is probably an empty array or an array with one element.


## Quicksort
Quicksort is a sorting algorithm. It's much faster than selection sort, is frequently used in real life and also uses D&C.

### How it work ?

the simplest array that a sorting algorithm can handle either the array empty or array has one element.

if array has two elements and first elemnt grater than second element just swap them.

if array has 3 elements we well use D&C to break down this array until to reach the base case.

- pick an element from the array. this element called ***pivot***.

- now find the elements smaller than the pivot and the elements grater than the pivot.

![image](https://user-images.githubusercontent.com/105928025/214764751-e537535c-4782-4449-887f-e582b0436e28.png)  ![image](https://user-images.githubusercontent.com/105928025/214764783-7a4e0c00-9570-4798-8a40-6659e5358737.png)  ![image](https://user-images.githubusercontent.com/105928025/214764820-a793bde5-12cc-4329-94c1-2e8ffcc01103.png)

this way is called ***partitioning*** and after applying  this you will have:
- A sub-array of all numbers less than the pivot 

- The pivot

- A sub-array of all numbers greater than the pivot

after applying quick sort again for the two sub-arrays they will be sorted, then you can combain the whole thing like this 

    left array + povit + right array


### Merge sort vs. quicksort

mearge sort is O(n log n) and quicksort is O(n^2) in worst case and O(n log n) on average case, but Quicksort is much faster.

Quicksort is unique because its speed depends on the pivot you choose and quicksort has smaller constant than merge sort, so if they're both O(n log n) time, quicksort is faster. *And quicksort is faster in practice because it hits the average case way more often than the worst case*.


#### Average case vs. worst case

The performance of quicksort heavily depends on the pivot you choose. 

if you call quicksort with array that is already sorted and you always choose the first element as the pivot quicksort will not splitting the array into two sub-arrays. Instead, one of the sub-arrays is always empty and you make (n) recursive call, in every call you itreate the whole array and take O(n) time. So in this case the time will tack O(n^n).

![image](https://user-images.githubusercontent.com/105928025/215014096-eb3e0c11-e753-4495-b584-d195b9e2b265.png)


suppose you always choose the middle element as the pivot, in this case you divide the array in half every time, you don't need to make as many recursive calls. You hit the best case and average case and the time is O(n log n).

![image](https://user-images.githubusercontent.com/105928025/215014596-9cf5bb15-0f25-455a-9ed3-020ee7733654.png)



