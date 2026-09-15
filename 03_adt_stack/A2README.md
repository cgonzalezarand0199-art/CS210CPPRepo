1) What value does topIndex hold immediately after construction, and why does that specific value make isEmpty() return the right answer with no special-casing?
-  My topIndex holds 0 after construction, Because it represents that my index is empty at first so when isEmpty checks it says "yes"

2) Walk through push step by step, in words: what happens to data and topIndex, in what order, and why would swapping that order break the stack?
- When push() is called my code will first check if the stack is full because it won't allow you to add any if it's full. So if it's not full the topIndex will increase by one and the new value will then be stored in data with data{topIndex}. If this were done the other way then my code won't be able to identify the new inserted element.

3) Give the time complexity of push, pop, peek, isEmpty, isFull, and size, individually, in Big-O. For each one, justify it by describing what your code actually does, not by naming the general rule for stacks.
- Push is O(1), as it fixed to a number of operations. pop is O(1), because it reads one array element and decreases topIndex. peek is O(1), because accesses data{topIndex}. isEmpty is O(1), because it only checks topIndex. isFull is O(1) because it compares topIndex with 100. size is O(1) it calculates topIndex  

4) Exactly what happens in your code when push is called while the stack is full? State what prints (if anything), what gets returned (if anything), and whether topIndex changes. Then say why you chose that behavior.
- My push() functions checks ifFull() first, and if its full it prints "Can't push Stack is full" and returns nothing since nothing needed to be added so topIndex does not change. I chose this behavior beucase it made the most sence to me, and it was simple for me to understand

5) Exactly what happens when pop or peek is called while the stack is empty? Same level of detail as above.
- They do the similar things as push() but pop()/ peek() give different messages as pop() will "Can't pop Stack is empty" and peek() will give "Can't peek Stack is empty" they both give this message beucase they use isEmpty() to check also they both return -1 beucase it's a replacemnt for it to return an int

6) Your array is fixed at 100 slots. If a caller needed more room than that, what would have to change in your class to support it, and what would it likely cost in terms of the time complexity you gave in question 3?
-  I would have needed to change the class for its to use a bigger array or a different array structure. And I believe with this change the time complexity would change into O(n) if element, if in the old element needed to be copied to the new. 

7) Without looking anything up: if this stack were built on a linked list instead of an array, name one advantage and one disadvantage that trade-off would bring, based on what you already know about how arrays and pointers behave differently.
- A linked-list would grow as needed without being limited to an array of 100. while the disadvantage would be that a link list may require pointer for the nodes while the array stores it in a fixed memory.