# Collections

## Stack

![stack](https://github.com/user-attachments/assets/4ecb3ec8-bc64-4624-8225-df67bf14a341)

In order to create a stack, we must import java.util.stack package and use the Stack() constructor of this class. The below example creates an empty Stack.

```Stack<E> stack = new Stack<E>();```

```
// Create a new stack
  Stack<Integer> s = new Stack<>();
  // Push elements onto the stack
  s.push(1);
  s.push(2);
  s.push(3);
  s.push(4); 
  
  // Displaying the Stack
  System.out.println("Initial Stack: " + stack);
  
  // Pop elements from the stack
  // isEmpty() to check if stack is empty
  while(!s.isEmpty()) {
      System.out.println(s.pop());
  }
  Integer element = (Integer) stack.peek();
  System.out.println("Element on stack top: " + element);

  // Searching element in the stack
  Integer pos = (Integer) stack.search(element);

  if(pos == -1)
      System.out.println("Element not found");
  else
      System.out.println("Element is found at position: " + pos);
```


> The Stack class in Java is a legacy class and inherits from Vector in Java. It is a thread-safe class and hence involves overhead when we do not need thread safety. It is recommended to use ArrayDeque for stack implementation as it is more efficient in a single-threaded environment
