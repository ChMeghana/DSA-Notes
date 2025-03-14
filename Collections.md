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


The Stack class in Java is a legacy class and inherits from Vector in Java.
It is a thread-safe class and hence involves overhead when we do not need thread safety.
It is recommended to use ArrayDeque for stack implementation as it is more efficient in a single-threaded environment.

One more reason to use Deque over Stack is Deque has the ability to use streams convert to list with keeping LIFO concept applied while Stack does not.


```import java.util.*;
import java.util.stream.Collectors;

class GFG {
    public static void main (String[] args) {
 
          Stack<Integer> stack = new Stack<>();
        Deque<Integer> deque = new ArrayDeque<>();

        stack.push(1);//1 is the top
        deque.push(1);//1 is the top
        stack.push(2);//2 is the top
        deque.push(2);//2 is the top

        List<Integer> list1 = stack.stream().collect(Collectors.toList());//[1,2]
          System.out.println("Using Stack -");
          for(int i = 0; i < list1.size(); i++){
              System.out.print(list1.get(i) + " " );
        }
          System.out.println();

        List<Integer> list2 = deque.stream().collect(Collectors.toList());//[2,1]
          System.out.println("Using Deque -");
          for(int i = 0; i < list2.size(); i++){
              System.out.print(list2.get(i) + " " );
        }
          System.out.println();
      
    }
}
```



