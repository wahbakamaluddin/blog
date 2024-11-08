---
title: "Data Structure & Algorithm"
summary: Notes on data structure & algorithm
date: 2023-10-21
series: ["Notes"]
weight: 1
aliases: ["/DSA"]
tags: ["Notes", "Undergraduate"]
author: ["Wahba Kamaluddin"]
---

{{< collapse summary="W1 - Introduction to Data Structure" >}}

- What is problem solving in a programmer POV?
  ![Screenshot 2023-10-21 at 2.40.17 PM.png](images/university-notes/DSA/Screenshot_2023-10-21_at_2.40.17_PM.png)
  - Taking the statement of a problem and develop a computer program to solve the problem
  - A solution is a computer program written in programming language consists of module (e.g dunciton, method, class, etc)
  - A good computer program (solution) consists of modules that:
    - Organize data collection to facilitate operations
    - Store, move and alter data
    - Use algorithms to communicate with one another
- What is algorithm?
  ![Screenshot 2023-10-21 at 2.44.56 PM.png](images/university-notes/DSA/Screenshot_2023-10-21_at_2.44.56_PM.png)
  - A step-by-step procedure to perform a task in a finite amount of time
  - It operate on a collection of data
  - It’s a problem solving using logic
  - A well-defined instructions in algorithm include:
    - Input
    - Processing
    - Output
  - Basic Control Structures;
    - Sequential
    - Selection
    - Repetition
  - Techniques to design algorithm:
    - Pseudocode
    - Flowchart
    - State Machine
    -
- What is Abstract Data Type (ADT)?
  - It’s a high-level conceptual model for organizing and working with data in cs, it defines sets of operations that can be preformed on the data.
- What is Data Structure?
  - A way of storing and organizing data in a computer so that it can be used efficiently
  - Choosing the right data structure will affect the efficiency of an algorithm implementation
  - Operations to data structure
    - traversing
    - searching
    - insertion
    - deletion
    - sorting
    - merging
  - What are 2 data structure types (how data is organized and stored)?
    ![Screenshot 2023-10-21 at 2.58.18 PM.png](images/university-notes/DSA/Screenshot_2023-10-21_at_2.58.18_PM.png)
    - **Primitive Data Structures**: These are basic data types provided by programming languages, like integers, floating-point numbers, characters, booleans, and pointers.
    - **Non-Primitive Data Structures**: These are more complex structures created by combining primitive data types or other non-primitive structures, like arrays, structures, linked lists, stacks, queues, trees, and graphs. They help organize and manage data in various ways.

{{</ collapse >}}

{{< collapse summary="W2 - Complexity Analysis" >}}

- Why is algorithm analysis needed?
  - To predict the performance (time + space(memory))
  - To compare algorithms
  - To provide guarantees
  - To avoid bugs
- What are the measurements?
  - Effectiveness
    - Easy to understand
    - Easy to trace
    - The step of logical execution are well organized
  - Termination
    - Step of execution contains ending
    - Termination happen as planned, not because of problems like looping, out of memory, or infinite value
  - Efficiency
    - Running time
    - Memory usage
    - Accuracy (output is expected or required)
- What is algorithm complexity?
  - The analysis of how the resources required by an algorithm (time and memory) grow as a function as the size of the input data
  - it provides measure of how efficient an algorithm is in terms of time and memory usage
  - What are 2 primary aspects of algorithm complexity?
    - Time
      - Most algorithms transform input objects into output objects
      - The running time of an algorithm typically grows with the input size
      - 3 case to consider
        - Worst case
          - A determination of the max amount of time that an algorithm requires to solve the problems of size _n_
          - eg: sorting increasing of number for input:
            - 9, 8, 7, 6, 5, 4, 3, 2, 1, 0 (the algorithm will need to compare the first number to all the number after it to find the lowest, thus take a looooong time)
        - Average case
          - A determination of the average amount of time that an algorithm requires to solve the problems of size n
          - eg: sorting increasing of number for input:
            - 8,6,4,5,3,2,0,1,9 (the algorithm does not need to compare the numbers all the. way to the back, hence better than the worse case)
        - Best case
          - A determination of the min amount of time that an algorithm requires to solve problems of size n
          - eg: sorting increasing of number for input:
            - 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 (the numbers are already sorted)
      - Represented using Big O notation
        - provides idea on how an algorithm will grow in complexity as the number of input increases
        - 7 Big O
          ![Screenshot 2023-10-22 at 6.41.08 AM.png](images/university-notes/DSA/Screenshot_2023-10-22_at_6.41.08_AM.png)
          ![Screenshot 2023-10-22 at 6.41.25 AM.png](images/university-notes/DSA/Screenshot_2023-10-22_at_6.41.25_AM.png)
          ![Screenshot 2023-10-22 at 6.41.37 AM.png](images/university-notes/DSA/Screenshot_2023-10-22_at_6.41.37_AM.png)
          ![Screenshot 2023-10-22 at 6.41.48 AM.png](images/university-notes/DSA/Screenshot_2023-10-22_at_6.41.48_AM.png)
          ![Screenshot 2023-10-22 at 6.42.00 AM.png](images/university-notes/DSA/Screenshot_2023-10-22_at_6.42.00_AM.png)
          ![Screenshot 2023-10-22 at 8.33.22 AM.png](images/university-notes/DSA/Screenshot_2023-10-22_at_8.33.22_AM.png)
          ![Screenshot 2023-10-22 at 6.42.57 AM.png](images/university-notes/DSA/Screenshot_2023-10-22_at_6.42.57_AM.png)

{{</ collapse >}}
{{< collapse summary="W3 - Linked List" >}}

- A data structure composed of nodes, each node holding some information and a reference to another node in the list
  - Nodes can be located anywhere in the memory
  - Passing one node to another using references
  - Can be implemented many ways, but the most flexible is by using a separate object for each node
- Closest thing is array, but array has limitation:
  - Changing of array size needs to create new array and copy all data
  - Data in array are next to each other sequentially, inserting new data require shifting other data
- What are the types of linked list?
  - Singly linked list
    ![Screenshot 2023-10-30 at 12.06.30 PM.png](images/university-notes/DSA/Screenshot_2023-10-30_at_12.06.30_PM.png)
    ![Screenshot 2023-10-30 at 12.13.40 PM.png](images/university-notes/DSA/Screenshot_2023-10-30_at_12.13.40_PM.png)
    - head: beginning of linked list
    - tail: end of linked list
    - Each node has:
      - Info field: store the info
      - Address field: linking nodes (address field that contains reference to the next node — thats why at the tail, the address field is NULL, since there is no next node)
  - Doubly linked list
    ![Screenshot 2023-10-30 at 12.14.23 PM.png](images/university-notes/DSA/Screenshot_2023-10-30_at_12.14.23_PM.png)
    ![Screenshot 2023-10-30 at 12.16.53 PM.png](images/university-notes/DSA/Screenshot_2023-10-30_at_12.16.53_PM.png)
    - head: the beginning of the linked list
    - tail: the end of linked list
    - Each nodes have:
      - Info field: the actual data
      - Next field: the address of next node
      - Prev field: the address of previous node
  - Circular linked list
    ![Screenshot 2023-10-30 at 12.17.30 PM.png](images/university-notes/DSA/Screenshot_2023-10-30_at_12.17.30_PM.png)
    ![Screenshot 2023-10-30 at 12.17.41 PM.png](images/university-notes/DSA/Screenshot_2023-10-30_at_12.17.41_PM.png)
    - Can be:
      - Singly: The next pointer of tail points to head
      - Doubly: The previous pointer of head points to tail
  - Self-organizing list
    ![example of self-organizing list](images/university-notes/DSA/Screenshot_2023-10-30_at_2.47.12_PM.png)
    example of self-organizing list
    - A list that reorders its elements based on some self-organizing heuristic to improve average access time
    - Methods for organizing list:
      - Move-to-front
        - After the desired element is located, put it at the beginning of the list
      - Transpose
        - After the desired element is located, swap it with its predecessor unless it is at the head of the list
      - Count
        - Order the list by the number of times elements are being accessed (the more it is accessed, the closer it is to the beginning)
      - Ordering
        - Order the list using certain criteria natural for the information under scrutiny — This means that the order of elements in the list is not fixed; it changes dynamically based on how often and how recently elements are accessed or searched for.
- Access to the list

  - isEmpty()
  - addToHead(Tel)
  - addToTail()
  - deleteFromHead()
  - deleteFromTail()
  - Delete(Tel)
  - printAll()
  - isInList(Tel)

  ```java
      public class IntSLList {
          protected IntSLLNode head, tail;
          public IntSLList() { //constructor, initiating a value
              head = tail = null;
          }

          public boolean isEmpty() {
              return head == null; //check if head is empty, then the list is empty
          }

          public void addToHead(int el) {
              head = new intSLLNode(el, head);
              if (tail==null)
                  tail = head; //if tail is null, then the list is empty (only contain the newly added head)
          }

          public void addToTail(int el) {
              if  (!isEmpty()) {
                  tail.next = new IntSLLNode(el);
                  tail = tail.next
              }
              else head = tail = new IntSLLNode(el); //if the list is empty, head = tail
          }

          public int deleteFromHead() {
              int el = head.info;
              if (head==tail)
                  head = tail = null; //if only one node in the list
              else head = head.next;
              return el; //the value deleted is returned
              }

          public int deleteFromTail() {
              int el = tail.info;
              if (head==tail)
                  head = tail = null;
              else {
                  IntSLLNode tmp;
                  for (tmp = head; tmp.next != null; tmp = tmp.next);//finding the predecessor of tail
                  tail = tmp; //the predecessor of tail becomes tail
                  tail.next = null;
                  }
              return el;
              }

          public void printAll() {
              for(IntSLLNode tmp = head; tmp != null; tmp = tmp.next)
                  System.out.print(tmp.info + " ")
          }

          public boolean isInList(int el) {
              InsSLLNode tmp;
              for(tmp = head; tmp!=null && tmp.info!=el; tmp=tmp,next);
              return tmp!=null;
          }

          public void delete(int el) {
          if(!isEmpty())
              if(head==tail && el==head.info)
                  if(head==tail && el==head.info)
                      head = tail = null; //if only one node in the list
                  else if(el==head.info)
                      head = head.next; //if the node is the head
                  else {
                      IntSLLNode pred, tmp;//of node is not the head
                      for(pred=head, tmp=head.next;
                          tmp!=null && tmp.info !=el;
                          pred=pred.next, tmp=tmp.next);
                      if(tmp!=null {
                          pred.next = tmp.next;//it skips the deleted node, jump straight to next node
                          if(tmp==tail) //if el is in tail
                              tail=pred;
                      })
                  }
          }
          }

  ```

- Implementation of linked list
  - Implement other complex data structure:
    - Trees
    - Graphs
    - Heaps
  - To store and process polynomials
  - To create. dynamic stacks and queues which can grow and shrink at run time
  - To add two large numbers (stack)
  - To check if it is palindrome — katak ↔ katak

{{</ collapse >}}
{{< collapse summary="W4 - Stacks and Queues" >}}

- Stacks

  - Linear data structure that can be accessed only at one of its ends for storing and retrieving data
  - **LIFO** structure: Last In First Out — useful when data have to be stored and then retrieved in reverse order
  - Functions on stack
    ![a series of operations executed on a stack](images/university-notes/DSA/Screenshot_2023-11-09_at_2.12.42_PM.png)
    a series of operations executed on a stack
    - clear() - clear the stack
    - isEmpty() - check if stack is empty
    - push(el) - put element el on top of the stack
    - pop() - take the topmost element form the stack (only the top can be removed)
    - topEl() - return the topmost element without removing
  - What are the applications of stack?

    - Matching delimiters/ balanced parenthesis

      - delimiters:
        - parentheses ( )
        - square brackets [ ]
        - curly brackets { }
        - comment delimiters /\* \*/

      ```python

      read character ch from file;
      while not end of file
          if ch is '(', '[', or '{'
              push(ch);#if open brakcet found, push into stack
          else if ch is double quote
              skip all chars to a double quote;
          else if ch is ')', ']', or '}'
              if ch and popped off delimiter not match
                  failure;#if close bracket found, pop from stack
                                  #if popped doesnt mactch the close brakcet
                                  #means the bracket isn't balanced
              else
                  pop stack;
          else if ch is '/'
              read the next character;
              if character is '*'
                  skip all character until '*/' is found
                  report if until end of file, no '*/' found
              else ch = the character read in;
                  continue; //go to the beginning of the loop
          if stack is empty
              success;
          ese failure;
      ```

      ![Screenshot 2023-11-09 at 3.20.40 PM.png](images/university-notes/DSA/Screenshot_2023-11-09_at_3.20.40_PM.png)
      ![Screenshot 2023-11-09 at 3.23.54 PM.png](images/university-notes/DSA/Screenshot_2023-11-09_at_3.23.54_PM.png)

      - if open bracket found, push into stack
      - if close bracket found, pop the stack, if not match, than the parentheses is not balanced
        - Since stack is **LIFO**, if it is balanced, the bracket should always match

    - addingLargeNumbers()

      ```python
      read numerals of the first number, store the
      numbers corresponding to them on the stack;

      read numerals of the second number, store the
      numbers corresponding to them on the stack;

      carry=0;

      while at least one stack is not empty

          pop a number from each nonempty stack, add
          to carry;

          push the unit part on the result stack;
          store carry in carry;

      push carry on the result stack if it is
      not zero;

      pop numbers from the result stack and
      display them'
      ```

      ![Screenshot 2023-11-09 at 3.30.44 PM.png](images/university-notes/DSA/Screenshot_2023-11-09_at_3.30.44_PM.png)

    - convertDecimaltoBinary()

      ```python
      Create stack object
      Read (number)
      While num != 0
          d = num % 2 #d= remainder
          push d into stack
          num = num / 2 #num is updated

      while stack is not empty
          pop numbers from the stack,
          display them; #stack is popped according
                                      #to LIFO
      ```

    - reverseWord()

      ```python
      read(data)
      while (not end of file && stack not full)
          push data
          read data
      while (stack is not empty)
          pop data
          print data

      ```

    - Postfix Evaluation

      - Prefix: +ab
      - Infix: a+b
      - Postfix: ab+
      - In high level languages, infix can’t be used to evaluate expressions, because it make ambiguity in the order of expressions, therefore computer convert infix to postfix first then evaluate it

      ```java
      eg: 23+*

      if digit
          push into stack;
          //1, 2, 3 is pushed into stack
      else
          pop last digit;
          //3 is popped
          pop last difit;
          //2 is popped
          calculate;
          //2+3=5
          push result into stack;
          //stack: 1, 5
      ```

    - Infix to Postfix conversion
      - Rules
        - Operand directly to output
        - Operators are pushed into the stack (including parenthesis)
          - Priority: \*/ → +- → ()
          - Check if top operator, if:
            - top < current, push current onto stack
            - top > current, pop top, push current
          - If there is ‘(’, pop into stack, wait until ‘)’ is found, then pop the operators after ‘(’, (parenthesis is not output-ed)
      - eg:
        ![Screenshot 2023-11-11 at 9.38.55 PM.png](images/university-notes/DSA/Screenshot_2023-11-11_at_9.38.55_PM.png)
        ![Screenshot 2023-11-11 at 9.39.06 PM.png](images/university-notes/DSA/Screenshot_2023-11-11_at_9.39.06_PM.png)

  - How to implement stack?

    - Custom implementation

      - Using array

        ```java
        public class ArrayStack {
            private int maxSize;
            private int[] stackArray;
            private int top;

            public ArrayStack(int size) {
                maxSize = size;
                stackArray = new int[maxSize];
                top = -1;
            }

            public void push(int value) {
                if (top < maxSize - 1) {
                    stackArray[++top] = value;
                } else {
                    System.out.println("Stack is full. Cannot push " + value);
                }
            }

            public int pop() {
                if (top >= 0) {
                    return stackArray[top--];
                } else {
                    System.out.println("Stack is empty. Cannot pop.");
                    return -1; // Or throw an exception
                }
            }

            public int peek() {
                return top >= 0 ? stackArray[top] : -1;
            }

            public boolean isEmpty() {
                return top == -1;
            }
        }
        ```

      - Using LinkedList

        ```java
        import java.util.LinkedList;

        public class LinkedListStack {
            private LinkedList<Integer> stack = new LinkedList<>();

            public void push(int value) {
                stack.addFirst(value);
            }

            public int pop() {
                if (!stack.isEmpty()) {
                    return stack.removeFirst();
                } else {
                    System.out.println("Stack is empty. Cannot pop.");
                    return -1; // Or throw an exception
                }
            }

            public int peek() {
                return stack.isEmpty() ? -1 : stack.getFirst();
            }

            public boolean isEmpty() {
                return stack.isEmpty();
            }
        }
        ```

    - Using Java’s standard library

      - Using java.util.Stack

        ```java
        import java.util.Stack;

        public class JavaUtilStackExample {
            public static void main(String[] args) {
                Stack<Integer> stack = new Stack<>();
                stack.push(1);
                stack.push(2);
                stack.push(3);

                System.out.println("Top element: " + stack.peek());

                while (!stack.isEmpty()) {
                    System.out.println("Popped: " + stack.pop());
                }
            }
        }
        ```

        - Method summary
          | Modifier and Type | Method and Description |
          | ------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
          | `boolean` | [**`empty**](https://docs.oracle.com/javase/8/docs/api/java/util/Stack.html#empty--)()`Tests if this stack is empty.                                                                                                                                   |
| [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Stack.html) | [**`peek**](https://docs.oracle.com/javase/8/docs/api/java/util/Stack.html#peek--)()`Looks at the object at the top of this stack without removing it from the stack. |
          | [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Stack.html) | [**`pop**](https://docs.oracle.com/javase/8/docs/api/java/util/Stack.html#pop--)()`Removes the object at the top of this stack and returns that object as the value of this function. |
          | [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Stack.html) | [**`push**](https://docs.oracle.com/javase/8/docs/api/java/util/Stack.html#push-E-)([**E**](https://docs.oracle.com/javase/8/docs/api/java/util/Stack.html) item)`Pushes an item onto the top of this stack.                                           |
| `int`                                                                     | [**`search**](https://docs.oracle.com/javase/8/docs/api/java/util/Stack.html#search-java.lang.Object-)([**Object\*\*](https://docs.oracle.com/javase/8/docs/api/java/lang/Object.html) o)`Returns the 1-based position where an object is on this stack. |

      - Using java.util.ArrayDeque

        - Deque is double-ended queue, it extends queue interface, allow for double-ended queue; can be used to implement stack and queue

        ```java
        import java.util.ArrayDeque;
        import java.util.Deque;

        public class DequeAsStackExample {
            public static void main(String[] args) {
                Deque<Integer> stack = new ArrayDeque<>();

                // Push elements onto the stack
                stack.push(1);
                stack.push(2);
                stack.push(3);

                System.out.println("Top element: " + stack.peek());

                // Pop elements from the stack
                while (!stack.isEmpty()) {
                    System.out.println("Popped: " + stack.pop());
                }
            }
        }
        ```

        - Method summary
          | Modifier and Type | Method and Description |
          | ------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
          | `boolean` | [**`add**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#add-E-)([**E**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) e)`Inserts the specified element into the queue represented by this deque (in other words, at the tail of this deque) if it is possible to do so immediately without violating capacity restrictions, returning `true` upon success and throwing an `IllegalStateException` if no space is currently available. |
| `void`                                                                                                                                                       | [**`addFirst**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#addFirst-E-)([**E**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) e)`Inserts the specified element at the front of this deque if it is possible to do so immediately without violating capacity restrictions, throwing an `IllegalStateException` if no space is currently available.                                                                                   |
| `void` | [**`addLast**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#addLast-E-)([**E**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) e)`Inserts the specified element at the end of this deque if it is possible to do so immediately without violating capacity restrictions, throwing an `IllegalStateException` if no space is currently available. |
          | `boolean` | [**`contains**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#contains-java.lang.Object-)([**Object**](https://docs.oracle.com/javase/8/docs/api/java/lang/Object.html) o)`Returns `true` if this deque contains the specified element.                                                                                                                                                                                                                  |
| [**`Iterator**](https://docs.oracle.com/javase/8/docs/api/java/util/Iterator.html)<[**E**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html)>` | [**`descendingIterator**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#descendingIterator--)()`Returns an iterator over the elements in this deque in reverse sequential order. |
          | [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) | [**`element**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#element--)()`Retrieves, but does not remove, the head of the queue represented by this deque (in other words, the first element of this deque).                                                                                                                                                                                                                                             |
| [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html)                                                                                    | [**`getFirst**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#getFirst--)()`Retrieves, but does not remove, the first element of this deque. |
          | [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) | [**`getLast**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#getLast--)()`Retrieves, but does not remove, the last element of this deque. |
          | [**`Iterator**](https://docs.oracle.com/javase/8/docs/api/java/util/Iterator.html)<[**E**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html)>` | [**`iterator**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#iterator--)()`Returns an iterator over the elements in this deque in proper sequence. |
          | `boolean` | [**`offer**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#offer-E-)([**E**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) e)`Inserts the specified element into the queue represented by this deque (in other words, at the tail of this deque) if it is possible to do so immediately without violating capacity restrictions, returning `true` upon success and `false` if no space is currently available. |
          | `boolean` | [**`offerFirst**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#offerFirst-E-)([**E**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) e)`Inserts the specified element at the front of this deque unless it would violate capacity restrictions.                                                                                                                                                                                        |
| `boolean`                                                                                                                                                    | [**`offerLast**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#offerLast-E-)([**E**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) e)`Inserts the specified element at the end of this deque unless it would violate capacity restrictions. |
          | [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) | [**`peek**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#peek--)()`Retrieves, but does not remove, the head of the queue represented by this deque (in other words, the first element of this deque), or returns `null` if this deque is empty. |
          | [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) | [**`peekFirst**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#peekFirst--)()`Retrieves, but does not remove, the first element of this deque, or returns `null` if this deque is empty.                                                                                                                                                                                                                                                                 |
| [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html)                                                                                    | [**`peekLast**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#peekLast--)()`Retrieves, but does not remove, the last element of this deque, or returns `null` if this deque is empty. |
          | [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) | [**`poll**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#poll--)()`Retrieves and removes the head of the queue represented by this deque (in other words, the first element of this deque), or returns `null` if this deque is empty. |
          | [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) | [**`pollFirst**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#pollFirst--)()`Retrieves and removes the first element of this deque, or returns `null` if this deque is empty.                                                                                                                                                                                                                                                                           |
| [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html)                                                                                    | [**`pollLast**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#pollLast--)()`Retrieves and removes the last element of this deque, or returns `null` if this deque is empty. |
          | [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) | [**`pop**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#pop--)()`Pops an element from the stack represented by this deque. |
          | `void` | [**`push**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#push-E-)([**E**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) e)`Pushes an element onto the stack represented by this deque (in other words, at the head of this deque) if it is possible to do so immediately without violating capacity restrictions, throwing an `IllegalStateException` if no space is currently available.                                             |
| [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html)                                                                                    | [**`remove**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#remove--)()`Retrieves and removes the head of the queue represented by this deque (in other words, the first element of this deque). |
          | `boolean` | [**`remove**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#remove-java.lang.Object-)([**Object**](https://docs.oracle.com/javase/8/docs/api/java/lang/Object.html) o)`Removes the first occurrence of the specified element from this deque. |
          | [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) | [**`removeFirst**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#removeFirst--)()`Retrieves and removes the first element of this deque.                                                                                                                                                                                                                                                                                                                 |
| `boolean`                                                                                                                                                    | [**`removeFirstOccurrence**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#removeFirstOccurrence-java.lang.Object-)([**Object**](https://docs.oracle.com/javase/8/docs/api/java/lang/Object.html) o)`Removes the first occurrence of the specified element from this deque. |
          | [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) | [**`removeLast**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#removeLast--)()`Retrieves and removes the last element of this deque. |
          | `boolean` | [**`removeLastOccurrence**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#removeLastOccurrence-java.lang.Object-)([**Object**](https://docs.oracle.com/javase/8/docs/api/java/lang/Object.html) o)`Removes the last occurrence of the specified element from this deque.                                                                                                                                                                                 |
| `int`                                                                                                                                                        | [**`size\*\*](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#size--)()`Returns the number of elements in this deque. |

    - Stacks function in java.util
      - `boolean empty()`- return true if empty
      - `Object peek()` - return top element, throw EmptyStackException for empty stack
      - `Object pop()` - remove top element, throw EmptyStackException if empty
      - `Object push(Object el)` - insert el at the top of the stack, return it
      - `int search(Object el)` - return position of el
      - `Stack()` - create empty stack

- Queue

  - A waiting line that grows by adding elements to its end, shrinks elements from its front (both end are used, compared to stack, only the front end is used to add, remove)
  - **FIFO** structure: First In, First Out
  - Functions on queue
    ![Screenshot 2023-11-09 at 4.46.08 PM.png](images/university-notes/DSA/Screenshot_2023-11-09_at_4.46.08_PM.png)
    - clear() - clear the queue
    - isEmpty() - check if the queue is empty
    - enqueue(el) - put the element el at the end of the queue
    - dequeue() - take the first element from the queue
    - firstEl() - return the first element in the queue without removing it
  - What are the applications?
    - Tracing people at ticket windows
    - CPU scheduling
    - Printing task
    - Checking palindrome
  - How to implement queue?

    - Custom implementation

      - Using Array

        ```java
        public class ArrayStack {
            private int maxSize;
            private int[] stackArray;
            private int top;

            public ArrayStack(int size) {
                maxSize = size;
                stackArray = new int[maxSize];
                top = -1;
            }

            public void push(int value) {
                if (top < maxSize - 1) {
                    stackArray[++top] = value;
                } else {
                    System.out.println("Stack is full. Cannot push " + value);
                }
            }

            public int pop() {
                if (top >= 0) {
                    return stackArray[top--];
                } else {
                    System.out.println("Stack is empty. Cannot pop.");
                    return -1; // Or throw an exception
                }
            }

            public int peek() {
                return top >= 0 ? stackArray[top] : -1;
            }

            public boolean isEmpty() {
                return top == -1;
            }
        }
        ```

      - Using LinkedList

        ```java
        import java.util.LinkedList;

        public class LinkedListQueue {
            private LinkedList<Integer> queue = new LinkedList<>();

            public void enqueue(int value) {
                queue.addLast(value);
            }

            public int dequeue() {
                if (!queue.isEmpty()) {
                    return queue.removeFirst();
                } else {
                    System.out.println("Queue is empty. Cannot dequeue.");
                    return -1; // Or throw an exception
                }
            }

            public int peek() {
                return queue.isEmpty() ? -1 : queue.getFirst();
            }

            public boolean isEmpty() {
                return queue.isEmpty();
            }
        }
        ```

    - Using [Java’s standard library](https://docs.oracle.com/javase/8/docs/api/java/util/Queue.html)

      - Using java.util.LinkedList

        ```java
        import java.util.LinkedList;
        import java.util.Queue;

        public class JavaUtilQueueExample {
            public static void main(String[] args) {
                Queue<Integer> queue = new LinkedList<>();
                queue.offer(1);
                queue.offer(2);
                queue.offer(3);

                System.out.println("Front element: " + queue.peek());

                while (!queue.isEmpty()) {
                    System.out.println("Dequeued: " + queue.poll());
                }
            }
        }
        ```

        - Method summary
          | Modifier and Type | Method and Description |
          | ------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
          | `boolean` | [**`add**](https://docs.oracle.com/javase/8/docs/api/java/util/Queue.html#add-E-)([**E**](https://docs.oracle.com/javase/8/docs/api/java/util/Queue.html) e)`Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions, returning `true` upon success and throwing an `IllegalStateException` if no space is currently available. |
| [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Queue.html) | [**`element**](https://docs.oracle.com/javase/8/docs/api/java/util/Queue.html#element--)()`Retrieves, but does not remove, the head of this queue. |
          | `boolean` | [**`offer**](https://docs.oracle.com/javase/8/docs/api/java/util/Queue.html#offer-E-)([**E**](https://docs.oracle.com/javase/8/docs/api/java/util/Queue.html) e)`Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions. |
          | [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Queue.html) | [**`peek**](https://docs.oracle.com/javase/8/docs/api/java/util/Queue.html#peek--)()`Retrieves, but does not remove, the head of this queue, or returns `null` if this queue is empty.                                                                                                                                                                                                               |
| [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Queue.html) | [**`poll**](https://docs.oracle.com/javase/8/docs/api/java/util/Queue.html#poll--)()`Retrieves and removes the head of this queue, or returns `null` if this queue is empty. |
          | [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Queue.html) | [**`remove**](https://docs.oracle.com/javase/8/docs/api/java/util/Queue.html#remove--)()`Retrieves and removes the head of this queue. |

      - Using java.util.ArrayDeque

        - Deque is double-ended queue, it extends queue interface, allow for double-ended queue; can be used to implement stack and queue

        ```java
        import java.util.ArrayDeque;
        import java.util.Deque;

        public class ArrayDequeQueueExample {
            public static void main(String[] args) {
                Deque<Integer> queue = new ArrayDeque<>();
                queue.offer(1);
                queue.offer(2);
                queue.offer(3);

                System.out.println("Front element: " + queue.peek());

                while (!queue.isEmpty()) {
                    System.out.println("Dequeued: " + queue.poll());
                }
            }
        }
        ```

        - Method summary
          | Modifier and Type | Method and Description |
          | ------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
          | `boolean` | [**`add**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#add-E-)([**E**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) e)`Inserts the specified element into the queue represented by this deque (in other words, at the tail of this deque) if it is possible to do so immediately without violating capacity restrictions, returning `true` upon success and throwing an `IllegalStateException` if no space is currently available. |
| `void`                                                                                                                                                       | [**`addFirst**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#addFirst-E-)([**E**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) e)`Inserts the specified element at the front of this deque if it is possible to do so immediately without violating capacity restrictions, throwing an `IllegalStateException` if no space is currently available.                                                                                   |
| `void` | [**`addLast**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#addLast-E-)([**E**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) e)`Inserts the specified element at the end of this deque if it is possible to do so immediately without violating capacity restrictions, throwing an `IllegalStateException` if no space is currently available. |
          | `boolean` | [**`contains**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#contains-java.lang.Object-)([**Object**](https://docs.oracle.com/javase/8/docs/api/java/lang/Object.html) o)`Returns `true` if this deque contains the specified element.                                                                                                                                                                                                                  |
| [**`Iterator**](https://docs.oracle.com/javase/8/docs/api/java/util/Iterator.html)<[**E**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html)>` | [**`descendingIterator**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#descendingIterator--)()`Returns an iterator over the elements in this deque in reverse sequential order. |
          | [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) | [**`element**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#element--)()`Retrieves, but does not remove, the head of the queue represented by this deque (in other words, the first element of this deque).                                                                                                                                                                                                                                             |
| [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html)                                                                                    | [**`getFirst**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#getFirst--)()`Retrieves, but does not remove, the first element of this deque. |
          | [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) | [**`getLast**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#getLast--)()`Retrieves, but does not remove, the last element of this deque. |
          | [**`Iterator**](https://docs.oracle.com/javase/8/docs/api/java/util/Iterator.html)<[**E**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html)>` | [**`iterator**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#iterator--)()`Returns an iterator over the elements in this deque in proper sequence. |
          | `boolean` | [**`offer**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#offer-E-)([**E**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) e)`Inserts the specified element into the queue represented by this deque (in other words, at the tail of this deque) if it is possible to do so immediately without violating capacity restrictions, returning `true` upon success and `false` if no space is currently available. |
          | `boolean` | [**`offerFirst**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#offerFirst-E-)([**E**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) e)`Inserts the specified element at the front of this deque unless it would violate capacity restrictions.                                                                                                                                                                                        |
| `boolean`                                                                                                                                                    | [**`offerLast**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#offerLast-E-)([**E**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) e)`Inserts the specified element at the end of this deque unless it would violate capacity restrictions. |
          | [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) | [**`peek**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#peek--)()`Retrieves, but does not remove, the head of the queue represented by this deque (in other words, the first element of this deque), or returns `null` if this deque is empty. |
          | [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) | [**`peekFirst**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#peekFirst--)()`Retrieves, but does not remove, the first element of this deque, or returns `null` if this deque is empty.                                                                                                                                                                                                                                                                 |
| [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html)                                                                                    | [**`peekLast**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#peekLast--)()`Retrieves, but does not remove, the last element of this deque, or returns `null` if this deque is empty. |
          | [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) | [**`poll**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#poll--)()`Retrieves and removes the head of the queue represented by this deque (in other words, the first element of this deque), or returns `null` if this deque is empty. |
          | [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) | [**`pollFirst**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#pollFirst--)()`Retrieves and removes the first element of this deque, or returns `null` if this deque is empty.                                                                                                                                                                                                                                                                           |
| [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html)                                                                                    | [**`pollLast**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#pollLast--)()`Retrieves and removes the last element of this deque, or returns `null` if this deque is empty. |
          | [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) | [**`pop**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#pop--)()`Pops an element from the stack represented by this deque. |
          | `void` | [**`push**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#push-E-)([**E**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) e)`Pushes an element onto the stack represented by this deque (in other words, at the head of this deque) if it is possible to do so immediately without violating capacity restrictions, throwing an `IllegalStateException` if no space is currently available.                                             |
| [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html)                                                                                    | [**`remove**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#remove--)()`Retrieves and removes the head of the queue represented by this deque (in other words, the first element of this deque). |
          | `boolean` | [**`remove**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#remove-java.lang.Object-)([**Object**](https://docs.oracle.com/javase/8/docs/api/java/lang/Object.html) o)`Removes the first occurrence of the specified element from this deque. |
          | [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) | [**`removeFirst**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#removeFirst--)()`Retrieves and removes the first element of this deque.                                                                                                                                                                                                                                                                                                                 |
| `boolean`                                                                                                                                                    | [**`removeFirstOccurrence**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#removeFirstOccurrence-java.lang.Object-)([**Object**](https://docs.oracle.com/javase/8/docs/api/java/lang/Object.html) o)`Removes the first occurrence of the specified element from this deque. |
          | [**`E`**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html) | [**`removeLast**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#removeLast--)()`Retrieves and removes the last element of this deque. |
          | `boolean` | [**`removeLastOccurrence**](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#removeLastOccurrence-java.lang.Object-)([**Object**](https://docs.oracle.com/javase/8/docs/api/java/lang/Object.html) o)`Removes the last occurrence of the specified element from this deque.                                                                                                                                                                                 |
| `int`                                                                                                                                                        | [**`size\*\*](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html#size--)()`Returns the number of elements in this deque. |

- Priority queues

  - Can be assigned to enable a particular process, or event, to be executed out of a sequence without affecting overall system operation
  - Elements are dequeued according to their priority and their current queue position
  - How to implement priority queue?

    - Custom implementation

      - Using LinkedList

        ```java
        import java.util.LinkedList;
        import java.util.ListIterator;

        public class LinkedListPriorityQueue<T extends Comparable<T>> {

            private LinkedList<PriorityNode<T>> list = new LinkedList<>();

            public void enqueue(T element, int priority) {
                PriorityNode<T> newNode = new PriorityNode<>(element, priority);

                if (list.isEmpty() || priority > list.getLast().getPriority()) {
                    list.addLast(newNode);
                } else {
                    ListIterator<PriorityNode<T>> iterator = list.listIterator();

                    while (iterator.hasNext()) {
                        if (priority < iterator.next().getPriority()) {
                            iterator.previous();
                            iterator.add(newNode);
                            break;
                        }
                    }
                }
            }

            public T dequeue() {
                if (isEmpty()) {
                    return null;
                }

                return list.removeFirst().getElement();
            }

            public T peek() {
                return isEmpty() ? null : list.getFirst().getElement();
            }

            public boolean isEmpty() {
                return list.isEmpty();
            }

            public static void main(String[] args) {
                LinkedListPriorityQueue<String> priorityQueue = new LinkedListPriorityQueue<>();

                priorityQueue.enqueue("Task 1", 3);
                priorityQueue.enqueue("Task 2", 1);
                priorityQueue.enqueue("Task 3", 2);

                System.out.println("Peek: " + priorityQueue.peek());

                while (!priorityQueue.isEmpty()) {
                    System.out.println("Dequeued: " + priorityQueue.dequeue());
                }
            }

            private static class PriorityNode<T> {
                private T element;
                private int priority;

                public PriorityNode(T element, int priority) {
                    this.element = element;
                    this.priority = priority;
                }

                public T getElement() {
                    return element;
                }

                public int getPriority() {
                    return priority;
                }
            }
        }
        ```

    - Using Java’s standard library

      - Using java.util.PriorityQueue

        ```java
        import java.util.PriorityQueue;

        public class PriorityQueueExample {
            public static void main(String[] args) {
                PriorityQueue<Integer> priorityQueue = new PriorityQueue<>();

                priorityQueue.offer(3);
                priorityQueue.offer(1);
                priorityQueue.offer(2);

                System.out.println("Peek: " + priorityQueue.peek());

                while (!priorityQueue.isEmpty()) {
                    System.out.println("Poll: " + priorityQueue.poll());
                }
            }
        }
        ```

  - How to represent priority queue by linked list?
    - All elements are entry ordered (unordered list, since its based on which element are added first)
      - Big O for:
        - adding element: O(1)
        - searching element: O(n)
    - Order is maintained by putting new element at its proper position according to its priority (sorted list)
      - Big O for:
        - adding element: O(n) — need to traverse to proper position to add the new element
        - searching element: O(1)
  - What are the application?
    - Assignment priority based on dateline
    - Airline check in — business class is prioritized

{{</ collapse >}}
{{< collapse summary="W5 - Recursion" >}}

- Technique of making a function call itself, it provides a way to break complicated problems into simple problems which are easier to solve
- The name "recursive" comes from the idea of recursion, where a problem is broken down into smaller, more manageable subproblems, and the solution is obtained by solving these subproblems and combining their results. The repetition of the function calls, each addressing a smaller part of the problem, gives rise to the term "recursive.”
- General form of a recursive call

  ```java
  if (base case condition) { //calculate base without recursion
  }
  else {
  }
  // general case with recursive calls
  // break the problem into a smaller problem of the same form
  // solve the smaller problems by calling the recursive function.
  // smaller solutions can be used to solve the larger problem
  }
  ```

  - It have 2 cases:
    - Base case - identify case that easily solvable (no need for recursion)
    - Recursive case - breaks problem into smaller problem of the same form
  - eg: n - factorial

    - Pseudocode

      ```java
      //Recursive
      int fact(int n) {
          if(n==0)
              return 1.0;
          else
              return n*fact(n-1);
      }

      //Iterative
      int fact(int n) {
          int product=1;
          for(int j = 1; j <= n; j++)
              product *=j;
          return product;
      }

      ```

    - Anatomy of a recursive call
      ![Screenshot 2023-11-15 at 11.00.14 AM.png](images/university-notes/DSA/Screenshot_2023-11-15_at_11.00.14_AM.png)
      - n=0 is base case
      - n>0 is recursive case
    - Tracing
      ![Screenshot 2023-11-15 at 11.01.01 AM.png](images/university-notes/DSA/Screenshot_2023-11-15_at_11.01.01_AM.png)

  - eg: summation
    ```java
    public class Main {
        public static void main(String[] args) {
        int result = sum(10);
        System.out.println(result);
        }
        public static int sum(int k) {
        if (k > 0) {
            return k + sum(k - 1);
        } else {
            return 0;
        }
        }
    }
    ```
    - When `sum()` function is called, it adds parameter `k` to the sum of all numbers < `k` until k = 0.
    - Tracing:
      10 + sum(9)
      10 + ( 9 + sum(8) )
      10 + ( 9 + ( 8 + sum(7) ) )
      ...
      10 + 9 + 8 + 7 + 6 + 5 + 4 + 3 + 2 + 1 + sum(0)
      10 + 9 + 8 + 7 + 6 + 5 + 4 + 3 + 2 + 1 + 0

- What are types of recursion?

  - 1. Direct Recursion

    - Function calls itself within the same function repeatedly:
      - Tail recursion
        - The function call itself, the call is the last statement executed by the function before returning.
        - eg: Printing num down to 1
          ```java
          void fun1(int num) {
              // if block check the condition
              if (num == 0)
                  return;
              else
                  printf ("\n Number is: %d", num); // print the number
              return fun1(num - 1);      // recursive call at the end in the fun() function
          }
          int main () {
              fun1(7); // pass 7 as integer argument
              return 0;
          }
          ```
      - Non-tail/ head recursion
        - Non-tail simply means every recursion that is not tail, one of which is head recursion (if the recursion doesn’t fit tail recursion, it’s non-tail)
        - The recursive call is the first statement in the function
        - eg: Print num down to 1
          ```java
          void head_fun (int num) {
              if ( num > 0 ) {
                  // Here the head_fun() is the first statement to be called
                  head_fun (num - 1);
                  printf (" %d", num);
              }
          }
          int main () {
              int a = 5;
              printf (" Use of Non-Tail/Head Recursive function \n");
              head_fun (a); // function calling
              return 0;
          }
          ```
    - Structure of direct recursion:
      ```java
      fun() {
          //some code
          fun();
          //some code
      }
      ```
      - the outer fun() recursively calls the inner fun()
    - Eg: Finding fibonacci series

      ```java
      int fibo_num (int i) {
          // if the num i is equal to 0, return 0;
          //base case
          if ( i == 0) {
              return 0;
          }
          //base case
          if ( i == 1) {
              return 1;
          }
          //recursive case
          return fibo_num (i - 1) + fibonacci (i -2);
      }

      int main () {
          int i;
          // use for loop to get the first 10 fibonacci series
          for ( i = 0; i < 10; i++) {
              printf (" %d \t ", fibo_num (i));
          }
          return 0;
      }
      ```

  - 2. Indirect Recursion

    - Function is mutually called by another function in a circular manner
    - Structure of indirect recursion:

      ```java
      fun1() {
          //  write some code
          fun2()
      }

      fun2() {
          // write some code
          fun3()
          // write some code
      }

      fun3() {
          // write some code
          fun1()
      }
      ```

      - There are 3 functions, When the fun1() function is executed, it calls the fun2() for its execution. And then, the fun2() function starts its execution calls the fun3() function
      - Each function leads to another function to make their execution cicularly

    - Eg: Checking even or odd of 1 - 10;
      ```java
      int num = 1; // global variable
      public void odd () {
          // if statement check and execute the block till n is less than equal to 10
          if (num <= 10)
          {
              printf (" %d ", num + 1);  // print a number by adding 1
              num++; // increment by 1
              even(); // invoke the even function
          }
          return;
      }
      public void even () {
          // if block check the condition that n is less than equal to 10
          if ( num <= 10)
          {
              printf (" %d ", num - 1); // print a number by subtracting 1
              num++;
              odd(); // call the odd() function
          }
          return;
      }
      public static void main (String[] args) {
          odd(); // main call the odd() function at once
          return 0;
      }
      ```

  - 3. Nested Recursion
    - Recursive function calls itself with a recursive call as on of its arguments (the input parameter is the result of a recursive call)
    - eg: Ackerman function
      ```java
      public void int ackerman(int m, int n) {
          if(m == 0) {
              retunr n + 1;
          } else if(m > 0 && n == 0) {
                  return ackerman(m - 1, 1)
              } else {
                      return ackerman(m - 1, ackerman(m, n - 1))
                  }
      }
      ```

- What is excessive recursion?
  - A situation where recursion continues for an extended period, potentially leading to issue like stack overflow.
  - eg
    ![Screenshot 2023-11-15 at 12.15.40 PM.png](images/university-notes/DSA/Screenshot_2023-11-15_at_12.15.40_PM.png)
    ```java
    int fib(int n) {
        if (n<2)
            return n;
        else
            return fib(n-2) + fib(n-1);
    }
    ```
    ![Screenshot 2023-11-15 at 12.16.46 PM.png](images/university-notes/DSA/Screenshot_2023-11-15_at_12.16.46_PM.png)
    ![Screenshot 2023-11-15 at 12.16.59 PM.png](images/university-notes/DSA/Screenshot_2023-11-15_at_12.16.59_PM.png)
- What are the applications of recursion?
  - Fibonacci Series
  - Linear Search
  - Binary Search
  - Quick Sort
  - Merge Sort
  - Tower of Hanoi
  - Tree traversals
  - Graph traversals
- What are the advantage and disadvantage of recursive over iterative?
  - Advantages
    - Code is simpler, shorter
    - Performs better in solving problems based on tree structures
  - Disadvantages
    - Can throw a StackOverflow Exception since it consumes a lot of memory
- Iteration to recursion

  - Print reverse using of a linked list

    - Reverse linked list by iteration

    ```java
    package Q3.Q3_a;
    import java.util.LinkedList;

    public class reverseLinkedList {

            //reverse by iteration
        public static void printReverseByIteration (LinkedList<Integer> list) {
            int listLength = list.size();
            for (int i = 0; i < listLength; i ++) {
                System.out.println(list.pollLast());
            }
        }

            //funtion testing
        public static void main(String [] args) {
            LinkedList<Integer> list = new LinkedList<>();
            list.add(1);
            list.add(2);
            list.add(3);
            list.add(4);
            list.add(5);
            list.add(6);
                    System.out.println("Reverse linked list by iteration: ");
            printReverseByIteration(list);
        }
    }
    ```

    - Reverse linked list by recursion

      ```java
      package Q3.Q3_a;
      import java.util.LinkedList;

      public class reverseLinkedList {

              //reverse by recursion
          public static void printReverseByRecursion (LinkedList<Integer> list) {
              if (list.isEmpty()) {
                  return;
                      System.out.println(list.pollLast());
              printReverseByIteration(list);
          }

              //funtion testing
          public static void main(String [] args) {
              LinkedList<Integer> list = new LinkedList<>();
              list.add(1);
              list.add(2);
              list.add(3);
              list.add(4);
              list.add(5);
              list.add(6);
                      System.out.println("Reverse linked list by recursion: ");
              printReverseByRecursion(list);
          }
      }
      ```

      ![Screenshot 2023-11-20 at 9.07.08 AM.png](images/university-notes/DSA/Screenshot_2023-11-20_at_9.07.08_AM.png)

  - Sum of array elements

    - Sum of array by iteration

      ```java
      package Q3.Q3_b;
      public class sumOfArray {

              //sum calculation using for loop
          public static int sumByIteration (int[] numArr) {
              int sum = 0;
              for (int i = 0; i < numArr.length; i++) {
                  sum += numArr[i];
              }
              return sum;
          }

          public static void main (String [] args) {
              int numArr[] = {1,2,3,4,5};
              System.out.print(sumByIteration(numArr));
          }
      }

      ```

    - Sum of array by recursion

      ```java
      sumOfArray{
              //sum calculation using recursion
          public static int sumByRecursion (int[] numArr, int index) {
              if (index == numArr.length) {
                  return 0;
              }

              //recursive case
              return numArr[index] + sumByRecursion(numArr, index + 1);
          }

          public static void main (String [] args) {
              int numArr[] = {1,2,3,4,5};
              System.out.print(sumByRecursion(numArr, 0));
          }
      }
      ```

  - Reverse a stack

    - Reverse stack via iteration:

      ```java
      class reverseByIteration {
          static void insertAtBottom(Stack<Integer> st, int x) {
              Stack<Integer> tmpStack2 = new Stack<>();

              // Pop all elements from the original stack
              // and push them onto tmpStack2
              while (!st.isEmpty()) {
                  tmpStack2.push(st.pop());
              }

              // Push the new element x onto the original stack
              st.push(x);

              // Pop all elements from tmpStack2 and push them
              // back onto the original stack
              while (!tmpStack2.isEmpty()) {
                  st.push(tmpStack2.pop());
              }
          }

          static void reverse(Stack<Integer> st) {
              Stack<Integer> tmpStack = new Stack<>();

              // Pop all elements from the original stack and
              // push them onto tmpStack
              while (!st.isEmpty()) {
                  tmpStack.push(st.pop());
              }

              // Insert each element from tmpStack at the bottom of the original stack
              while (!tmpStack.isEmpty()) {
                  int x = tmpStack.pop();
                  insertAtBottom(st, x);
              }
          }
      }

      public class reverseStack {
          public static void main (String [] args) {
              Stack<Integer> st = new Stack<>();

              st.push(1);
              st.push(2);
              st.push(3);
              st.push(4);
              st.push(5);

              // System.out.print("Original string: " + st);
              // reverseByRecursion.reverse(st);
              // System.out.print("\nReversed string " + st);
              System.out.print("Original string: " + st);
              reverseByIteration.reverse(st);
              System.out.print("\nReversed string using iteration:" + st);
          }
      }
      ```

    - Reverse stack via recursion:

      ```java
      package Q3.Q3_c;
      import java.util.Stack;

      class reverseByRecursion{
          static void insertAtBottom(Stack<Integer> st, int x) {
              //if stack is empty, insert directly to stack
              if (st.isEmpty()) {
                  st.push(x);
              //if stack not empty, pop element,
              //store as tmp,
              //repeat until stack is empty.
              //push x,
              //push tmp
              } else {
                  int tmp = st.peek();
                  st.pop();
                  insertAtBottom(st, x);
                  st.push(tmp);
              }
          }

          static void reverse(Stack<Integer> st) {
              //if stack size not 0,
              //pop element, store as x;
              //when size = 0,
              //call insertAtBottom(x)
              //until the last element
              if (st.size() > 0) {
                  int x = st.peek();
                  st.pop();
                  reverse(st);
                  insertAtBottom(st, x);
              }
          }
      }

      public class reverseStack {
          public static void main (String [] args) {
              Stack<Integer> st = new Stack<>();

              st.push(1);
              st.push(2);
              st.push(3);
              st.push(4);
              st.push(5);

              System.out.print("Original string: " + st);
              reverseByRecursion.reverse(st);
              System.out.print("\nReversed string using recursion" + st);
          }
      }
      ```

      ![Screenshot 2023-11-20 at 8.57.01 AM.png](images/university-notes/DSA/Screenshot_2023-11-20_at_8.57.01_AM.png)

{{</ collapse >}}
{{< collapse summary="W6 - Binary tree" >}}

- What is tree?
  ![Untitled](images/university-notes/DSA/Untitled.png)
  - A data type that consists of nodes and arcs
  - These trees are depicted upside-down, the root at the top, the leaves(terminal nodes) at the bottom
  - Basic terminologies
    - Parent node: Predecessor of a node (eg: 4 = 2; 8 = 4)
    - Child node: Immediate successor of a node (eg: 4 = 8, 9)
    - Root node: Topmost node (eg: 1)
    - Leaf/ terminal node: Nodes without children(eg: 8, 9, 10, 11, 13, 14)
    - Ancestor of a node: All predecessor of a node (eg: 8 = 4, 2, 1)
    - Descendants: child, grandchild, grand-grandchild(eg: 2 = 4, 8, 9, 5, 10, 11)
    - Sibling: Children of the same parent node(eg: 8 = 9)
    - Depth of a node: number of edges in path from root to node (eg: 4 = 2)
    - Level: 1 + Depth (eg: 4 = 3)
    - Height of a tree: Depth of the root; Number of edges on the longest downward path between root and a leaf (3)
    - Height of a node: No. of edges on the longest downward path between that node and a leaf (eg: 8 = 3)
- What is binary tree?
  ![Screenshot 2023-11-22 at 9.04.41 PM.png](images/university-notes/DSA/Screenshot_2023-11-22_at_9.04.41_PM.png)

  - A tree whose nodes have at most two children, each node of a binary tree consists of:
    - data item
    - address of left child
    - address of right child
  - max no of nodes at level i (root starts with level 1) = (2^i)-1
  - What are the categories of binary tree?
    - Strict/ proper binary tree
      ![Screenshot 2023-11-22 at 9.09.33 PM.png](images/university-notes/DSA/Screenshot_2023-11-22_at_9.09.33_PM.png)
      - Each node can only have either 2 or no children
    - Complete binary tree
      ![Screenshot 2023-11-22 at 9.22.15 PM.png](images/university-notes/DSA/Screenshot_2023-11-22_at_9.22.15_PM.png)
      - Identical with full binary tree, with two differences:
        1. Every level must be completely filled except for the last level
        2. The last level has all values as left as possible
    - Perfect binary tree
      ![Screenshot 2023-11-22 at 9.25.43 PM.png](images/university-notes/DSA/Screenshot_2023-11-22_at_9.25.43_PM.png)
      - All levels are completely filled
      - max no of nodes(elements) with height h = (2^(h+1))-1
  - What are the types of binary trees?

    - Binary search tree
      ![Screenshot 2023-11-23 at 11.44.31 AM.png](images/university-notes/DSA/Screenshot_2023-11-23_at_11.44.31_AM.png)

      - Its called search tree because it can be used to search for the number in `O(log(n))` time
      - left child < parent
      - right child ≥ parent
      - Converting array into BST
        - If child ≥ parent, insert right
        - if child < parent, insert left
        - eg: converting sequence of number into BST
          ![Screenshot 2023-11-23 at 6.34.23 AM.png](images/university-notes/DSA/Screenshot_2023-11-23_at_6.34.23_AM.png)
          ![Untitled Notebook.jpeg](images/university-notes/DSA/Untitled_Notebook.jpeg)
      - Deletion in BST
        ![Screenshot 2024-01-30 at 9.40.12 PM.png](images/university-notes/DSA/Screenshot_2024-01-30_at_9.40.12_PM.png)
      - Searching in BST
        ![Screenshot 2023-11-23 at 10.26.27 AM.png](images/university-notes/DSA/Screenshot_2023-11-23_at_10.26.27_AM.png)
        - On each node, if el < node, go down left, if el > node, go right
      - Implementation in JAVA

        ```java
        // Binary Search Tree operations in Java

        class BinarySearchTree {
            class Node {
            int key;
            Node left, right;

            public Node(int item) {
                key = item;
                left = right = null;
            }
            }

            Node root;

            BinarySearchTree() {
            root = null;
            }

            void insert(int key) {
            root = insertKey(root, key);
            }

            // Insert key in the tree
            Node insertKey(Node root, int key) {
            // Return a new node if the tree is empty
            if (root == null) {
                root = new Node(key);
                return root;
            }

            // Traverse to the right place and insert the node
            if (key < root.key)
                root.left = insertKey(root.left, key);
            else if (key > root.key)
                root.right = insertKey(root.right, key);

            return root;
            }

            void inorder() {
            inorderRec(root);
            }

            // Inorder Traversal
            void inorderRec(Node root) {
            if (root != null) {
                inorderRec(root.left);
                System.out.print(root.key + " -> ");
                inorderRec(root.right);
            }
            }

            void deleteKey(int key) {
            root = deleteRec(root, key);
            }

            Node deleteRec(Node root, int key) {
            // Return if the tree is empty
            if (root == null)
                return root;

            // Find the node to be deleted
            if (key < root.key)
                root.left = deleteRec(root.left, key);
            else if (key > root.key)
                root.right = deleteRec(root.right, key);
            else {
                // If the node is with only one child or no child
                if (root.left == null)
                return root.right;
                else if (root.right == null)
                return root.left;

                // If the node has two children
                // Place the inorder successor in position of the node to be deleted
                root.key = minValue(root.right);

                // Delete the inorder successor
                root.right = deleteRec(root.right, root.key);
            }

            return root;
            }

            // Find the inorder successor
            int minValue(Node root) {
            int minv = root.key;
            while (root.left != null) {
                minv = root.left.key;
                root = root.left;
            }
            return minv;
            }

            // Driver Program to test above functions
            public static void main(String[] args) {
            BinarySearchTree tree = new BinarySearchTree();

            tree.insert(8);
            tree.insert(3);
            tree.insert(1);
            tree.insert(6);
            tree.insert(7);
            tree.insert(10);
            tree.insert(14);
            tree.insert(4);

            System.out.print("Inorder traversal: ");
            tree.inorder();
            System.out.println("\n\nAfter deleting 10");
            tree.deleteKey(10);
            System.out.print("Inorder traversal: ");
            tree.inorder();
            }
        }
        ```

      - Complexity of BST
        | **Operation** | **Best Case Complexity** |
        | ------------- | ------------------------ |
        | Search | O(log n) |
        | Insertion | O(log n) |
        | Deletion | O(log n) |

    - Heap
      ![Screenshot 2023-11-23 at 11.44.31 AM.png](images/university-notes/DSA/Screenshot_2023-11-23_at_11.44.31_AM.png)
      - Properties
        - Complete binary tree — each level is completely filled, except for last level, it is filled from left to right
        - children ≤ parent
      - Converting array to heap
        - Always insert the new element at the end, and gradually move it upward if needed
        - Top-down method — John Williams Algorithm
          1. Insert the elements on the last, leftmost
          2. Heapify, repeat until the last element
          - Example
            ![Screenshot 2023-12-14 at 10.16.46 AM.png](images/university-notes/DSA/Screenshot_2023-12-14_at_10.16.46_AM.png)
        - Bottom-up method - Floyd Algorithm
          1. Arrange the arrays into a binary tree
          2. Heapify, starting from the lowest parent, check for the largest child, swap with parent, work our way up
          - Pseudocode
            ```java
            FloydAlgorithm(data [])
                for i = index of the last nonlead, down to 0
                    p = data [i];
                    while p not a lead and p < any of its children
                    swap p with the larger child
            ```
          - Example
            ![Screenshot 2023-12-14 at 10.17.00 AM.png](images/university-notes/DSA/Screenshot_2023-12-14_at_10.17.00_AM.png)
      - Insertion
        ![Screenshot 2023-11-23 at 11.58.42 AM.png](images/university-notes/DSA/Screenshot_2023-11-23_at_11.58.42_AM.png)
        1. Insert element at the end of the tree
           ![Screenshot 2023-11-23 at 11.59.19 AM.png](images/university-notes/DSA/Screenshot_2023-11-23_at_11.59.19_AM.png)
        1. Heapify the tree
      - Deletion
        ![Screenshot 2024-01-25 at 2.20.30 PM.png](images/university-notes/DSA/Screenshot_2024-01-25_at_2.20.30_PM.png)
        1. Delete the elements
        2. Replace with the lowest elements
        3. Heapify the tree
      - Heap representation using array
        | Parent | Left child | RIght child |
        | ------ | ------------ | ------------ |
        | i | (2 \* i) + 1 | (2 \* i) + 1 |
        ![Screenshot 2024-01-25 at 2.25.17 PM.png](images/university-notes/DSA/Screenshot_2024-01-25_at_2.25.17_PM.png)

  - How to traverse a tree?
    [https://www.youtube.com/watch?v=IpyCqRmaKW4&ab_channel=GeeksforGeeks](https://www.youtube.com/watch?v=IpyCqRmaKW4&ab_channel=GeeksforGeeks)

    - Process of visiting each node in the tree exactly one time in some order
    - Breadth-First Traversal (BFT)

      - Nodes on each level is read from left to right, from top to bottom
      - Logical approach:
        - Start from the root, a queue is initialized with root, root is dequeued, its child is enqueued
        - The elements in queue is dequeued one at a time, and its child in enqueued
        - Process is repeated until queue is empty
      - Tracing
        ![DSA-Lab 7.jpeg](images/university-notes/DSA/DSA-Lab_7.jpeg)
      - Implementation

        ```java
        import java.util.ArrayDeque;
        import java.util.Deque;
        import java.util.Queue;

        class Node {
            int data;
            Node left, right;

            public Node(int data) {
                this.data = data;
                this.left = this.right = null;
            }
        }

        public class BFTTraversal {
            static void BFTraversal(Node root) {
                if (root == null) {
                    return;
                }

                Queue<Node> queue = new ArrayDeque<>();
                queue.add(root);

                while (!queue.isEmpty()) {
                    Node tempNode = queue.poll();
                    System.out.print(tempNode.data + " ");

                                //enque left child
                    if (tempNode.left != null) {
                        queue.add(tempNode.left);
                    }
                                //enque right child
                    if (tempNode.right != null) {
                        queue.add(tempNode.right);
                    }
                }

        public static void main(String[] args) {
                Node root = new Node(1);
                root.left = new Node(2);
                root.right = new Node(3);
                root.left.left = new Node(4);
                root.left.right = new Node(5);

                System.out.println("Breadth First Traversal (using ArrayDeque): ");
                BFTraversal(root);
                }
            }
        ```

    - Depth-First Traversal (DFT)
      ![Screenshot 2023-12-14 at 10.16.31 AM.png](images/university-notes/DSA/Screenshot_2023-12-14_at_10.16.31_AM.png)

      - Preorder traversal
        ![Screenshot 2023-11-23 at 11.18.45 AM.png](images/university-notes/DSA/Screenshot_2023-11-23_at_11.18.45_AM.png)
        <Root><Left><Right>

        ```java
        void printPreorder(Node node)
            {
                if (node == null)
                    return;

                // First print data of node
                System.out.print(node.key + " ");

                // Then recur on left subtree
                printPreorder(node.left);

                // Now recur on right subtree
                printPreorder(node.right);
            }
        ```

        - eg
          ![Screenshot 2023-12-12 at 7.29.36 PM.png](images/university-notes/DSA/Screenshot_2023-12-12_at_7.29.36_PM.png)
          - Preorder: ABDEFC
          - step-by-step explanation
            1. at A, print A, read A.left
            2. at B, print B, read B.left
            3. at D, print D, read D.left
            4. D.left is null, return, read D.right
            5. D.right is null, return, read B.right
            6. at E, print E, read E.left
            7. at F, print F, read F.left
            8. F.left is null, return, read E.right
            9. E.right is null, return, read A.right
            10. at C, print C, read C.left
            11. C.left is null, return, read C.right
            12. C.tight is null, return

      - Inorder traversal
        ![Screenshot 2023-11-23 at 10.59.12 AM.png](images/university-notes/DSA/Screenshot_2023-11-23_at_10.59.12_AM.png)
        <Left><Root><Right>

        ```java
        void printInorder(Node node)
            {
                if (node == null)
                    return;

                // First recur on left child
                printInorder(node.left);

                // Then print the data of node
                System.out.print(node.key + " ");

                // Recur on right child
                printInorder(node.right);
            }
        ```

        - eg
          ![Screenshot 2023-12-12 at 7.29.36 PM.png](images/university-notes/DSA/Screenshot_2023-12-12_at_7.29.36_PM.png)
          - Inorder: DBFEAC
          - step-by-step explagnation
            1. at A, read A.left
            2. at B, read B.left
            3. at D, read D.left
            4. D.left is null, return, print D
            5. D.right is null, return
            6. at B, print B, read B.right
            7. at E, read E.left
            8. at F, read F.left
            9. F.left is null, return, print F
            10. at F, read F.right
            11. F.right is null, return
            12. at E, print E, read E.right
            13. E.right is null, return
            14. at A, print A, read A.right
            15. at C, read C.left
            16. C.left is null, return, print C, read C.right
            17. C.right is null, return

      - Postorder traversal
        ![Screenshot 2023-11-23 at 11.18.56 AM.png](images/university-notes/DSA/Screenshot_2023-11-23_at_11.18.56_AM.png)
        <Root><Left><Right>

        ```java
        void printPostorder(Node node)
            {
                if (node == null)
                    return;

                // First recur on left subtree
                printPostorder(node.left);

                // Then recur on right subtree
                printPostorder(node.right);

                // Now deal with the node
                System.out.print(node.key + " ");
            }
        ```

        - eg
          ![Screenshot 2023-12-12 at 7.29.36 PM.png](images/university-notes/DSA/Screenshot_2023-12-12_at_7.29.36_PM.png)
          - postorder: DFEBCA
          - step-by-step explanation
            1. at A, read A.left
            2. at B, read B.left
            3. at D. read D.left
            4. D.left is null, return, read D.right
            5. D.right is null, return, print D
            6. at B, read B.right
            7. at E, read E.left
            8. at F, read F.left
            9. F.left is null, return, read F.right
            10. F.right is null, return, print F
            11. at E, read E.right
            12. E.right is null, return, print E
            13. at B, print B
            14. at A, read A.right
            15. at C, read C.left
            16. C.left is null, return, read C.right
            17. C.right is null, return, print C
            18. at A, print A

  - Implementing binary trees
    ![Screenshot 2023-11-22 at 9.50.12 PM.png](images/university-notes/DSA/Screenshot_2023-11-22_at_9.50.12_PM.png)

    - Array

      ```java
      public class BinaryTreeArray {
          private int[] treeArray;
          private int size;

          public BinaryTreeArray(int capacity) {
              treeArray = new int[capacity];
              size = 0;
          }

          // Insert a new element into the binary tree
          public void insert(int data) {
              if (size < treeArray.length) {
                  treeArray[size] = data;
                  size++;
              } else {
                  System.out.println("Binary tree is full. Cannot insert more elements.");
              }
          }

          // Display the elements using in-order traversal
          public void inOrderTraversal(int index) {
              if (index < size) {
                  inOrderTraversal(2 * index + 1); // Left child
                  System.out.print(treeArray[index] + " ");
                  inOrderTraversal(2 * index + 2); // Right child
              }
          }

          public static void main(String[] args) {
              BinaryTreeArray binaryTree = new BinaryTreeArray(10);

              binaryTree.insert(1);
              binaryTree.insert(2);
              binaryTree.insert(3);
              binaryTree.insert(4);
              binaryTree.insert(5);

              System.out.println("In-order traversal:");
              binaryTree.inOrderTraversal(0);
          }
      }
      ```

    - Node-based

      ```java
      // Node creation
      class Node {
          int key;
          Node left, right;

          public Node(int item) {
          key = item;
          left = right = null;
          }
      }

      class BinaryTree {
          Node root;

          BinaryTree(int key) {
          root = new Node(key);
          }

          BinaryTree() {
          root = null;
          }

          // Traverse Inorder
          public void traverseInOrder(Node node) {
          if (node != null) {
          traverseInOrder(node.left);
          System.out.print(" " + node.key);
          traverseInOrder(node.right);
          }
          }

          // Traverse Postorder
          public void traversePostOrder(Node node) {
          if (node != null) {
          traversePostOrder(node.left);
          traversePostOrder(node.right);
          System.out.print(" " + node.key);
          }
          }

          // Traverse Preorder
          public void traversePreOrder(Node node) {
          if (node != null) {
          System.out.print(" " + node.key);
          traversePreOrder(node.left);
          traversePreOrder(node.right);
          }
          }

          public static void main(String[] args) {
          BinaryTree tree = new BinaryTree();

          tree.root = new Node(1);
          tree.root.left = new Node(2);
          tree.root.right = new Node(3);
          tree.root.left.left = new Node(4);

          System.out.print("Pre order Traversal: ");
          tree.traversePreOrder(tree.root);
          System.out.print("\nIn order Traversal: ");
          tree.traverseInOrder(tree.root);
          System.out.print("\nPost order Traversal: ");
          tree.traversePostOrder(tree.root);
          }
      }
      ```

{{</ collapse >}}
{{< collapse summary="W7/ W8- Graph" >}}

- What is graph?
  ![Screenshot 2023-12-30 at 10.58.10 AM.png](images/university-notes/DSA/Screenshot_2023-12-30_at_10.58.10_AM.png)
  - A data structure, G(V, E) that consist of:
    - Vertices/ Nodes, V
      - The data
    - Edges, E
      - Connect two vertices, can be labeled and directed
    ```cpp
    V = {1, 2, 3, 4, 5, 6}
    E = {(5, 3), (3, 1), (3, 4), (1, 2), (4, 2), (2, 6)}
    G = {V, E}
    ```
  - Tree vs graph
    - A tree is a type of graph that is connected, acyclic (meaning it has no cycles or loops), and has a single root node.
  - Terminologies
    - Path
      - A sequence of edges that allows you to go from vertex A to vertex B (when no vertex is repeated = simple path)
      - eg from 5 to 1: 531 or 53421
    - Cycle
      - Simple path path from A to A (graph without cycle = acyclic graph)
      - eg from 3 to 3: 3421 or 3142
    - Loop
      - An edge that connects the vertex to itslelf
      - eg
        ![Screenshot 2023-12-30 at 11.12.07 AM.png](images/university-notes/DSA/Screenshot_2023-12-30_at_11.12.07_AM.png)
- Types of graph
  - Directed and Undirected
    - Directed
      ![Screenshot 2023-12-30 at 11.00.19 AM.png](images/university-notes/DSA/Screenshot_2023-12-30_at_11.00.19_AM.png)
    - Undirected
      ![Screenshot 2023-12-30 at 11.00.36 AM.png](images/university-notes/DSA/Screenshot_2023-12-30_at_11.00.36_AM.png)
  - Connected and Disconnected
    - Connected
      ![Screenshot 2023-12-30 at 11.00.36 AM.png](images/university-notes/DSA/Screenshot_2023-12-30_at_11.00.36_AM.png)
    - Disconnected (at least 2 vertices aren’t connected by a path)
      ![Screenshot 2023-12-30 at 11.14.23 AM.png](images/university-notes/DSA/Screenshot_2023-12-30_at_11.14.23_AM.png)
  - Weighted graph
    ![Screenshot 2023-12-30 at 11.18.15 AM.png](images/university-notes/DSA/Screenshot_2023-12-30_at_11.18.15_AM.png)
    - Weights are assigned to each edge
    - If graph is weighted + directed = network
  - Complete graph
    ![Screenshot 2023-12-30 at 11.17.16 AM.png](images/university-notes/DSA/Screenshot_2023-12-30_at_11.17.16_AM.png)
    - Each vertex is connected to all other vertex
  - Spanning tree of an undirected graph
    ![Screenshot 2024-01-30 at 12.13.33 PM.png](images/university-notes/DSA/Screenshot_2024-01-30_at_12.13.33_PM.png)
    ![Screenshot 2024-01-30 at 12.13.42 PM.png](images/university-notes/DSA/Screenshot_2024-01-30_at_12.13.42_PM.png)
    - A sub-graph that contains all the vertices, no cycle
    - If we add any edge to this spannig tree, it forms a cycle, the tree becomes a graph
- Graph representation
  ![DSA-Lab 9.jpeg](images/university-notes/DSA/DSA-Lab_9.jpeg)
  - adjacency matrix
  - adjacency list
  - incidence matrix
- Graph traversal

  - Breadth-First Search algorithm (BFS)

    - Code

      ```java
      // Java program to print BFS traversal from a given source
      // vertex. BFS(int s) traverses vertices reachable from s.

      import java.io.*;
      import java.util.*;

      // This class represents a directed graph using adjacency
      // list representation
      class Graph {

          // No. of vertices
          private int V;

          // Adjacency Lists
          private LinkedList<Integer> adj[];

          // Constructor
          Graph(int v)
          {
              V = v;
              adj = new LinkedList[v];
              for (int i = 0; i < v; ++i)
                  adj[i] = new LinkedList();
          }

          // Function to add an edge into the graph
          void addEdge(int v, int w) { adj[v].add(w); }

          // prints BFS traversal from a given source s
          void BFS(int s)
          {
              // Mark all the vertices as not visited(By default
              // set as false)
              boolean visited[] = new boolean[V];

              // Create a queue for BFS
              LinkedList<Integer> queue
                  = new LinkedList<Integer>();

              // Mark the current node as visited and enqueue it
              visited[s] = true;
              queue.add(s);

              while (queue.size() != 0) {

                  // Dequeue a vertex from queue and print it
                  s = queue.poll();
                  System.out.print(s + " ");

                  // Get all adjacent vertices of the dequeued
                  // vertex s.
                  // If an adjacent has not been visited,
                  // then mark it visited and enqueue it
                  Iterator<Integer> i = adj[s].listIterator();
                  while (i.hasNext()) {
                      int n = i.next();
                      if (!visited[n]) {
                          visited[n] = true;
                          queue.add(n);
                      }
                  }
              }
          }

          // Driver code
          public static void main(String args[])
          {
              Graph g = new Graph(4);
              g.addEdge(0, 1);
              g.addEdge(0, 2);
              g.addEdge(1, 2);
              g.addEdge(2, 0);
              g.addEdge(2, 3);
              g.addEdge(3, 3);

              System.out.println(
                  "Following is Breadth First Traversal "
                  + "(starting from vertex 2)");

              g.BFS(2);
          }
      }

      // This code is contributed by Aakash Hasija
      ```

    - Pseudocode

      ```java
      BFS()
          boolean visited[];
          for all vertices v
              visited[v] = false;

          while there is a vertex v such that visited[v] == false
              enqueue(v)
              visited[v] = true

              while queue is not empty
                  u = dequeue()
                  print u
                  for all vertices w adjacent to u
                      if visited[w] == false
                          visited[w] = true
                          enqueue(w)
      ```

    - Tracing
      ![Linear Algebra - Tuto 4.jpeg](images/university-notes/DSA/Linear_Algebra_-_Tuto_4.jpeg)

  - Depth-First Search algorithm (DFS)

    - Code

      ```java
      // Java program to print DFS traversal
      // from a given graph
      import java.io.*;
      import java.util.*;

      // This class represents a
      // directed graph using adjacency
      // list representation
      class Graph {
          private int V;

          // Array of lists for
          // Adjacency List Representation
          private LinkedList<Integer> adj[];

          // Constructor
          @SuppressWarnings("unchecked") Graph(int v)
          {
              V = v;
              adj = new LinkedList[v];
              for (int i = 0; i < v; ++i)
                  adj[i] = new LinkedList();
          }

          // Function to add an edge into the graph
          void addEdge(int v, int w)
          {
              // Add w to v's list.
              adj[v].add(w);
          }

          // A function used by DFS
          void DFSUtil(int v, boolean visited[])
          {
              // Mark the current node as visited and print it
              visited[v] = true;
              System.out.print(v + " ");

              // Recur for all the vertices adjacent to this
              // vertex
              Iterator<Integer> i = adj[v].listIterator();
              while (i.hasNext()) {
                  int n = i.next();
                  if (!visited[n])
                      DFSUtil(n, visited);
              }
          }

          // The function to do DFS traversal.
          // It uses recursive DFSUtil()
          void DFS(int v)
          {
              // Mark all the vertices as
              // not visited(set as
              // false by default in java)
              boolean visited[] = new boolean[V];

              // Call the recursive helper
              // function to print DFS
              // traversal
              DFSUtil(v, visited);
          }

          // Driver Code
          public static void main(String args[])
          {
              Graph g = new Graph(4);

              g.addEdge(0, 1);
              g.addEdge(0, 2);
              g.addEdge(1, 2);
              g.addEdge(2, 0);
              g.addEdge(2, 3);
              g.addEdge(3, 3);

              System.out.println(
                  "Following is Depth First Traversal "
                  + "(starting from vertex 2)");

              // Function call
              g.DFS(2);
          }
      }
      // This code is contributed by Aakash Hasija
      ```

    - Pseudocode

      ```java
      DFS()
          boolean visited[];
          for all vertices v
              visited[v] = false;

          while there is a vertex v such that visited[v] == false
              stack.push(v)
              visited[v] = true

              while stack is not empty
                  u = stack.pop()
                  print u

                  for all vertices w adjacent to u
                      if visited[w] == false
                          visited[w] = true
                          stack.push(w)
      ```

    - Tracing
      ![Screenshot 2024-01-30 at 8.10.09 PM.png](images/university-notes/DSA/Screenshot_2024-01-30_at_8.10.09_PM.png)

- Shortest path algorithm
  - Algorithm to find a path of a minimum length between two specified vertices of a connected weighted graph
  - Dijkstra’s algorithm (greedy method — following a procedure to get the optimal path)
    [https://www.youtube.com/watch?v=XB4MIexjvY0&ab_channel=AbdulBari](https://www.youtube.com/watch?v=XB4MIexjvY0&ab_channel=AbdulBari)
    - Pseudocode
      ```java
      DijkstraAlgorithm (weighted simple digraph, vertex first)
          for all vertices v
              currDist(v) = infinity;
          currDist(first) = 0;
          toBeChecked = all vertices;
          while toBeChecked in not empty
              v = a vertex in toBeChecked with minimal currDist(v);
              remove v from toBeChecked;
              for all vertices u adjacent to v
                  if currDist(u) > currDist(v) + weight(edge(vu))
                      currDist(u) = currDist(v) + weight(edge(vu));
                      predecessor(u) = v;
      ```
    - Tracing
      ![IMG_2802.jpg](images/university-notes/DSA/IMG_2802.jpg)
  - Bellman Ford algorithm (dynamic programming — try all possible solution, find the best)
    [https://www.youtube.com/watch?v=FtN3BYH2Zes&ab_channel=AbdulBari](https://www.youtube.com/watch?v=FtN3BYH2Zes&ab_channel=AbdulBari)
    - Pseudocode
      ```java
      FordAlgorithm(weighted simple digraph, vertex first)
          for all vertices v
              currDist(v) = infinity;
          currDist(first) = 0;
          while there is an edge(vu) such that
                  currDist(u) > currDist(v) + weight(edge(vu));
              currDist(u) = currDist(v) + weight(edge(vu));
      ```
    - Tracing
      ![Linear Algebra - Tuto 6.jpeg](images/university-notes/DSA/Linear_Algebra_-_Tuto_6.jpeg)
      ![DSA-Lab 6.jpeg](images/university-notes/DSA/DSA-Lab_6.jpeg)
      - Total Iteration is (number of vertices(n)) - 1
  - Dijkstra vs Bellman Ford
    - Negative edge
      - example
        ![DSA-Lab 3.jpeg](images/university-notes/DSA/DSA-Lab_3.jpeg)
      - Dijkstra wont work with negative edge, since it relies on assumption that the shortest path to a node is found by always selecting the minimum distance from the source.
      - The problem is, a path with negative edges can make the path shorter when performing addition with a positive edge
      - Dijkstra however, does not consider the total addition of the path, it just consider the singular edge and make assumption based on the current edge.
      - For example, if there is two edges, one with heavier weight but it contains a negative edge in its path, and one with a lighter weight and have no negative edges, Dijkstra’s algorithm will make assumption that the latter is shorter, since logically, whatever numbers added to the former, it will be larger than the latter.
      - However in this case, the former actually have a shorter path since addition with the negative edge will make the total weight lighter
    - Negative cycle
      - Dijkstra can’t detect a negative cycle, while Bellman-Ford can.
      - Dijskstra algorithm only run based on the number of edges, and when it is finished, it consider the path obtained is the shortest.
      - Bellman-Ford algorithm will perform path-relaxation for total of (no . of vertex, n - 1 times). Since the maximum number of edges for an graph with n number of edges is n -1 , Bellman-Ford will do the relaxation process for n - 1 times to make sure it cover all the possible path.
      - For a graph with no negative cycle, the maximum number of relaxation is only n -1 .
      - Bellman-Ford algorithm can detect that the graph has a negative edges by observing if the relaxation continues over n - 1 times, since a negative edges can always be relaxed for infinite number of times.
    - Complexity
      | Dijsktra | Bellman-Ford |
      | ---------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
      | O(V\*E) | O(V+E)\*log(V) |
      | V iterations, each iterations involves E edges | Extraxting the minimum edge take O(Log V), for adjacent vertex, it updates the distance if a shorter path is found at most is E edges |
  - A\* algorithm
    - Step by step
      1. **Initialization:**
         - Create open and closed sets to keep track of visited and unvisited nodes.
         - Assign a tentative distance value to every node, initially set to infinity.
         - Assign a heuristic estimate to the destination node. The heuristic is a function that provides an estimate of the remaining distance from a node to the goal.
      2. **Start Node:**
         - Add the start node to the open set with a tentative distance of 0 and the heuristic estimate.
      3. **Main Loop:**
         - While the open set is not empty:
           - Select the node with the lowest tentative distance and heuristic estimate from the open set. This node is the current node.
           - If the current node is the destination, the algorithm has found the shortest path, and the path can be reconstructed.
           - Move the current node from the open set to the closed set to mark it as visited.
      4. **Neighbor Exploration:**
         - For each neighbor of the current node:
           - If the neighbor is in the closed set, skip it.
           - Calculate the tentative distance from the start node to the neighbor.
           - If the tentative distance is less than the recorded distance for the neighbor or the neighbor is not in the open set:
             - Update the recorded distance for the neighbor.
             - Set the neighbor's heuristic estimate.
             - Add the neighbor to the open set.
      5. **Optimal Path Extraction:**
         - Once the destination node is reached, reconstruct the path from the start node to the destination node by following the recorded predecessors.

{{</ collapse >}}
{{< collapse summary="W10 - Sorting" >}}

- Sorting is arranging things into either ascending or descending order
  [Sorting algorithm-animated](https://homepages.bluffton.edu/~nesterd/apps/SortingDemo.html)
- Types of sorting algorithms

  - Elementary

    - Insertion

      - Pseudocode
        ```java
        insertion(arr[])
            for i = 1 to arr.length - 1
                tmp = arr[i];
                compare tmp with arr[i]'s adjacent arr[j];
                move all elements greater than tmp, arr[j] by one position;
                place tmp it its proper position
        ```
        - Compare two value:
          - If in-order, move to next value
          - if not in-order, swap, compare to previous value until in order, then move to next value
      - Implementation

        ```java
        void insertionSort(int arr[], int n)
        {
                int n = arr.length

                //iteration
            for (i = 1; i < n; i++) {
                int key = arr[i];
                int j = i - 1;


                        //Comparison, movement
                        // Move elements of arr[0..i-1],
                // that are greater than key,
                // to one position ahead of their
                // current position
                while (j >= 0 && arr[j] > key) {
                    arr[j + 1] = arr[j];
                    j = j - 1;
                }
                arr[j + 1] = key;
            }
        }
        ```

        - Time complexity:
          | | Best | Worse |
          | -------------------- | ---- | ------ |
          | Iteration | n | n |
          | Comparison, movement | 1 | n |
          | BigO notation | O(n) | O(n^2) |
          - Best case:
            - Iteration: 1 - (arr.length - 1)
            - Movement, comparison: 1 (When the adjacent is in order, immediately exit the while loop)
          - Worst case:
            - Iteration: 1 - (arr.length - 1)
            - Comparison, movement: Swap with every elements before.

      - Tracing
        ![DSA-Lab 4.jpeg](images/university-notes/DSA/DSA-Lab_4.jpeg)
      - Long explanation
        ![Untitled](images/university-notes/DSA/Untitled%201.png)
        - \*Consider an example: arr[]: **{12, 11, 13, 5, 6}\***
          **_12      11      13      5      6_**
          **_First Pass:_**
        - _Initially, the first two elements of the array are compared in insertion sort._
          **\*12**      **11**      13      5      6\*
        - _Here, 12 is greater than 11 hence they are not in the ascending order and 12 is not at its correct position. Thus, swap 11 and 12.So, for now 11 is stored in a sorted sub-array._
          **\*11**      **12**      13      5      6\*
          **_Second Pass:_**
        - _Now, move to the next two elements and compare them_
          _11      **12**      **13**      5      6_
        - _Here, 13 is greater than 12, thus both elements seems to be in ascending order, hence, no swapping will occur. 12 also stored in a sorted sub-array along with 11_
          **_Third Pass:_**
        - _Now, two elements are present in the sorted sub-array which are **11** and **12**Moving forward to the next two elements which are 13 and 5_
          _11      12      **13**      **5**      6_
        - _Both 5 and 13 are not present at their correct place so swap them_
          _11      12      **5**      **13**      6_
        - _After swapping, elements 12 and 5 are not sorted, thus swap again_
          _11      **5**      **12**      13      6_
        - _Here, again 11 and 5 are not sorted, hence swap again_
          **\*5**      **11**      12      13      6\*
        - _Here, 5 is at its correct position_
          **_Fourth Pass:_**
        - _Now, the elements which are present in the sorted sub-array are **5, 11** and **12**Moving to the next two elements 13 and 6_
          \*5      11      12      **13**      **6\***
        - _Clearly, they are not sorted, thus perform swap between both_
          \*5      11      12      **6**      **13\***
        - _Now, 6 is smaller than 12, hence, swap again_
          \*5      11      **6**      **12**      13**\***
        - _Here, also swapping makes 11 and 6 unsorted hence, swap again_
          \*5      **6**      **11**      12   \***\*   13\*\*\***
        - _Finally, the array is completely sorted._

    - Selection

      - Pseudocode
        ```java
        selectionSort(arr[])
            for i = 0 to arr.length-2 (iterate all elements except the last one)
                select the smallest element among arr[i],...,arr[arr.length-1];
                    swap it with arr[i];
        ```
        - Find the smallest element, swap with 1st element
        - Find the 2nd-smallest element, swap with 2nd element
        - Repeat until array is sorted
      - Implementation

        ```java
        void sort(int arr[])
            {
                int n = arr.length;

                        //Iteration
                // One by one move boundary of unsorted subarray
                for (int i = 0; i < n-1; i++)
                {
                                //Finding smallest value
                    // Find the minimum element in unsorted array
                    int min_idx = i;
                    for (int j = i+1; j < n; j++)
                        if (arr[j] < arr[min_idx])
                            min_idx = j;

                                //Movement
                    // Swap the found minimum element with the first
                    // element
                    int temp = arr[min_idx];
                    arr[min_idx] = arr[i];
                    arr[i] = temp;
                }
            }
        ```

        - Time complexity:
          | | Best | Worse |
          | ---------------------- | ------ | ------ |
          | Iteration | n | n |
          | Finding smallest value | n | n |
          | Movement | 0 | 1 |
          | BigO notation | O(n^2) | O(n^2) |
          - Best case:
            - Iteration: 0 - (arr.length - 1) = n
            - Finding smallest value: n (although its in order, the algorithm still traverse the whole array finding for the smallest value for each iterations)
            - Movement: 0 (when it’s in order, there’ll be no swapping
          - Worst case:
            - Iteration: 0 - (arr.length - 1) = n
            - Finding smallest value: n
            - Movement: 1

      - Tracing
        ![DSA-Lab 5.jpeg](images/university-notes/DSA/DSA-Lab_5.jpeg)
      - Long explanation
        \*Lets consider the following array as an example: **arr[] = {64, 25, 12, 22, 11}\***
        **_First pass:_**
        ![https://media.geeksforgeeks.org/wp-content/uploads/20230524115038/1.webp](https://media.geeksforgeeks.org/wp-content/uploads/20230524115038/1.webp)
        - _For the first position in the sorted array, the whole array is traversed from index 0 to 4 sequentially. The first position where **64** is stored presently, after traversing whole array it is clear that **11** is the lowest value._
        - _Thus, replace 64 with 11. After one iteration **11**, which happens to be the least value in the array, tends to appear in the first position of the sorted list._
          \*\*
          **_Second Pass:_**
          ![https://media.geeksforgeeks.org/wp-content/uploads/20230526165135/2.webp](https://media.geeksforgeeks.org/wp-content/uploads/20230526165135/2.webp)
        - _For the second position, where 25 is present, again traverse the rest of the array in a sequential manner._
        - _After traversing, we found that **12** is the second lowest value in the array and it should appear at the second place in the array, thus swap these values._
          \*\*
          **_Third Pass:_**
          ![https://media.geeksforgeeks.org/wp-content/uploads/20230526165200/3.webp](https://media.geeksforgeeks.org/wp-content/uploads/20230526165200/3.webp)
        - _Now, for third place, where **25** is present again traverse the rest of the array and find the third least value present in the array._
        - _While traversing, **22** came out to be the third least value and it should appear at the third place in the array, thus swap **22** with element present at third position._
          \*\*
          **_Fourth pass:_**
          ![https://media.geeksforgeeks.org/wp-content/uploads/20230526165244/4.webp](https://media.geeksforgeeks.org/wp-content/uploads/20230526165244/4.webp)
        - _Similarly, for fourth position traverse the rest of the array and find the fourth least element in the array._
        - _As **25** is the 4th lowest value hence, it will place at the fourth position._
          \*\*
          **_Fifth Pass:_**
          ![https://media.geeksforgeeks.org/wp-content/uploads/20230526165320/5.webp](https://media.geeksforgeeks.org/wp-content/uploads/20230526165320/5.webp)
        - _At last the largest value present in the array automatically get placed at the last position in the array_
        - _The resulted array is the sorted array._

    - Bubble

      - Pseudocode

        ```java
        //Sort from left to right
        bubbleSort(arr[])
            for i = to arr.length-2
                for j = arr.length-1 downto i+1
                    if elements in positions j and j-1 are out of order
                        swap them;

        //Sort from right to left
        bubbleSort(arr[])
            for i = arr.length-1 downto 1
                for j = 0 upto i - 1
                    if elements in positions j and j+1 are out of order
                        swap them;
        ```

        - Scan the list, exchanging adjacent elements if they are not in relative order: bubbles the highest value to the top
        - Scan the list again, bubbling up the second highset value
        - Repeat untill all elements have been placed in their proper order.

      - Implementation

        ```java
        // An optimized version of Bubble Sort
            static void bubbleSort(int arr[], int n)
            {
                int i, j, temp;
                boolean swapped;

                        //Iteration
                for (i = 0; i < n - 1; i++) {
                    swapped = false;

                                //Comparison, movement
                    for (j = 0; j < n - i - 1; j++) {
                        if (arr[j] > arr[j + 1]) {

                            // Swap arr[j] and arr[j+1]
                            temp = arr[j];
                            arr[j] = arr[j + 1];
                            arr[j + 1] = temp;
                            swapped = true;
                        }
                    }

                    // If no two elements were
                    // swapped by inner loop, then break
                    if (swapped == false)
                        break;
                }
            }
        ```

        - Time complexity:
          | | Best | Worse |
          | ----------------------------------- | ---- | ------ |
          | Iteration | 1 | n |
          | Comparing adjacent values, swapping | n | n |
          | BigO notation | O(n) | O(n^2) |
          - Best case:
            - Iteration: 1 (when in the first iteration, the inner loop (swapping) does not perform any swapping, it will automatically indicate the arrays are sorted, hence it will exit the outer loop; refer to the implementation
            - Comparing adjacent values, swapping: n (although it’s in order, it’ll compare all adjacent elements in the first iteration but there’s no swapping)
          - Worst case:
            - Iteration: 0 - (arr.length - 1) = n
            - Comparing adjacent values, swapping: n

      - Tracing
        ![DSA-Lab-49.jpg](images/university-notes/DSA/DSA-Lab-49.jpg)
      - Long explanation
        Input: arr[] = {6, 3, 0, 5}
        First Pass:
        ![Untitled](images/university-notes/DSA/Untitled%202.png)
        - The largest element is placed in its correct position, i.e., the end of the array
          Second Pass:
          ![Untitled](images/university-notes/DSA/Untitled%203.png)
        - Place the second largest element at correct position
          Third Pass:
          ![Untitled](images/university-notes/DSA/Untitled%204.png)
        - Place the remaining two elements at their correct positions.
        - **Total no. of passes:** n-1
        - **Total no. of comparisons:** n\*(n-1)/2

    - Complexity comparison
      | | Best | Worse |
      | --------- | ------ | ------ |
      | Insertion | O(n) | O(n^2) |
      | Selection | O(n^2) | O(n^2) |
      | Bubble | O(n) | O(n^2) |

  - Advanced - Merge Sort - Pseudocode
    `java
        mergesort(arr[], first, last)
            if first < last
                mid = (first + last) / 2
                mergesort(arr[], first, mid);
                mergesort(arr[], mid + 1, last);
                merge(data[], first, last);
        ` - Divide the array into to, 2 until it become a single elements - Merge the elements by putting it in the correct position until sorted - Implementation
    ```java
    // Java program for Merge Sort
    import java.io.\*;

            class MergeSort {

                // Merges two subarrays of arr[].
                // First subarray is arr[l..m]
                // Second subarray is arr[m+1..r]
                void merge(int arr[], int l, int m, int r)
                {
                    // Find sizes of two subarrays to be merged
                    int n1 = m - l + 1;
                    int n2 = r - m;

                    // Create temp arrays
                    int L[] = new int[n1];
                    int R[] = new int[n2];

                    // Copy data to temp arrays
                    for (int i = 0; i < n1; ++i)
                        L[i] = arr[l + i];
                    for (int j = 0; j < n2; ++j)
                        R[j] = arr[m + 1 + j];

                    // Merge the temp arrays

                    // Initial indices of first and second subarrays
                    int i = 0, j = 0;

                    // Initial index of merged subarray array
                    int k = l;
                    while (i < n1 && j < n2) {
                        if (L[i] <= R[j]) {
                            arr[k] = L[i];
                            i++;
                        }
                        else {
                            arr[k] = R[j];
                            j++;
                        }
                        k++;
                    }

                    // Copy remaining elements of L[] if any
                    while (i < n1) {
                        arr[k] = L[i];
                        i++;
                        k++;
                    }

                    // Copy remaining elements of R[] if any
                    while (j < n2) {
                        arr[k] = R[j];
                        j++;
                        k++;
                    }
                }

                // Main function that sorts arr[l..r] using
                // merge()
                void sort(int arr[], int l, int r)
                {
                    if (l < r) {

                        // Find the middle point
                        int m = l + (r - l) / 2;

                        // Sort first and second halves
                        sort(arr, l, m);
                        sort(arr, m + 1, r);

                        // Merge the sorted halves
                        merge(arr, l, m, r);
                    }
                }

                // A utility function to print array of size n
                static void printArray(int arr[])
                {
                    int n = arr.length;
                    for (int i = 0; i < n; ++i)
                        System.out.print(arr[i] + " ");
                    System.out.println();
                }

                // Driver code
                public static void main(String args[])
                {
                    int arr[] = { 12, 11, 13, 5, 6, 7 };

                    System.out.println("Given array is");
                    printArray(arr);

                    MergeSort ob = new MergeSort();
                    ob.sort(arr, 0, arr.length - 1);

                    System.out.println("\nSorted array is");
                    printArray(arr);
                }
            }
            /* This code is contributed by Rajat Mishra */
            ```
            - Time complexity:
              |                        | Best   | Worse  |
              | ---------------------- | ------ | ------ |
              | Iteration              | n      | n      |
              | Finding smallest value | n      | n      |
              | Movement               | 0      | 1      |
              | BigO notation          | O(n^2) | O(n^2) |
              - Best case:
                - Iteration: 0 - (arr.length - 1) = n
                - Finding smallest value: n (although its in order, the algorithm still traverse the whole array finding for the smallest value for each iterations)
                - Movement: 0 (when it’s in order, there’ll be no swapping
              - Worst case:
                - Iteration: 0 - (arr.length - 1) = n
                - Finding smallest value: n
                - Movement: 1
          - Tracing
            ![Screenshot 2024-01-30 at 10.51.10 AM.png](images/university-notes/DSA/Screenshot_2024-01-30_at_10.51.10_AM.png)
        - Radix Sort
          - Pseudocode
            ```java
            radixsort(data[])
                for d = 1 to the position of the leftmost digit of the longest number
                    distribute all numbers in data[] among queues 0 through 9
                    according to the dth digit;
                    put all integers in data[];
            ```
            - Enque elements according to decimal places, starting with tens, up to the max decimal place of the data
            - Deque the elements starting with 9 to 0, enque according to hundreds decimal places
            - Repeat until sorted
          - Implementation
            ```java
            class Radix {

                // A utility function to get maximum value in arr[]
                static int getMax(int arr[], int n)
                {
                    int mx = arr[0];
                    for (int i = 1; i < n; i++)
                        if (arr[i] > mx)
                            mx = arr[i];
                    return mx;
                }

                // A function to do counting sort of arr[] according to
                // the digit represented by exp.
                static void countSort(int arr[], int n, int exp)
                {
                    int output[] = new int[n]; // output array
                    int i;
                    int count[] = new int[10];
                    Arrays.fill(count, 0);

                    // Store count of occurrences in count[]
                    for (i = 0; i < n; i++)
                        count[(arr[i] / exp) % 10]++;

                    // Change count[i] so that count[i] now contains
                    // actual position of this digit in output[]
                    for (i = 1; i < 10; i++)
                        count[i] += count[i - 1];

                    // Build the output array
                    for (i = n - 1; i >= 0; i--) {
                        output[count[(arr[i] / exp) % 10] - 1] = arr[i];
                        count[(arr[i] / exp) % 10]--;
                    }

                    // Copy the output array to arr[], so that arr[] now
                    // contains sorted numbers according to current
                    // digit
                    for (i = 0; i < n; i++)
                        arr[i] = output[i];
                }

                // The main function to that sorts arr[] of
                // size n using Radix Sort
                static void radixsort(int arr[], int n)
                {
                    // Find the maximum number to know number of digits
                    int m = getMax(arr, n);

                    // Do counting sort for every digit. Note that
                    // instead of passing digit number, exp is passed.
                    // exp is 10^i where i is current digit number
                    for (int exp = 1; m / exp > 0; exp *= 10)
                        countSort(arr, n, exp);
                }

                // A utility function to print an array
                static void print(int arr[], int n)
                {
                    for (int i = 0; i < n; i++)
                        System.out.print(arr[i] + " ");
                }

                // Main driver method
                public static void main(String[] args)
                {
                    int arr[] = { 170, 45, 75, 90, 802, 24, 2, 66 };
                    int n = arr.length;

                    // Function Call
                    radixsort(arr, n);
                    print(arr, n);
                }
            }
            ```
            - Time complexity:
              |                        | Best   | Worse  |
              | ---------------------- | ------ | ------ |
              | Iteration              | n      | n      |
              | Finding smallest value | n      | n      |
              | Movement               | 0      | 1      |
              | BigO notation          | O(n^2) | O(n^2) |
              - Best case:
                - Iteration: 0 - (arr.length - 1) = n
                - Finding smallest value: n (although its in order, the algorithm still traverse the whole array finding for the smallest value for each iterations)
                - Movement: 0 (when it’s in order, there’ll be no swapping
              - Worst case:
                - Iteration: 0 - (arr.length - 1) = n
                - Finding smallest value: n
                - Movement: 1
          - Tracing
            ![Screenshot 2024-01-30 at 10.18.07 AM.png](images/university-notes/DSA/Screenshot_2024-01-30_at_10.18.07_AM.png)
        - Heap Sort
          - Pseudocode
            ```java
            heapsort(arr[])
                transform data[] into heap;
                for i = data.length-1 downto 2
                    swap the root with the element in porition i;
                    restore the heap property for the tree data[0], ..., data[i - 1]
            ```
        - QuickSort
          - Based on the divide and conquer algorithm that picks an element as pivot and partitions the given array around the pivot in its correct position in the sorted array
          - How does QuickSort work?
            ![https://www.geeksforgeeks.org/wp-content/uploads/gq/2014/01/QuickSort2.png](https://www.geeksforgeeks.org/wp-content/uploads/gq/2014/01/QuickSort2.png)
            - _The key process in **quickSort** is a **partition()**. The target of partitions is to place the pivot (any element can be chosen to be a pivot) at its correct position in the sorted array and put all smaller elements to the left of the pivot, and all greater elements to the right of the pivot._
            - _Partition is done recursively on each side of the pivot after the pivot is placed in its correct position and this finally sorts the array._

    {{</ collapse >}}
