---
title: "Data Structure & Algorithm"
summary: Notes on data structure & algorithm
date: 2023-10-21
series: ["Notes"]
weight: 1
aliases: ["/DSA"]
tags: ["Notes"]
author: ["Wahba Kamaluddin"]
cover:
  image: images/papermod-cover.png
  hiddenInList: false
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
  ![Screenshot 2023-10-21 at 2.44.56 PM.png](DSA-Note%201ca69f7969c644dc8a4bde74abbe89b0/Screenshot_2023-10-21_at_2.44.56_PM.png)
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
    ![Screenshot 2023-10-21 at 2.58.18 PM.png](DSA-Note%201ca69f7969c644dc8a4bde74abbe89b0/Screenshot_2023-10-21_at_2.58.18_PM.png)
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
                    - A determination of the max amount of time that an algorithm requires to solve the problems of size *n*
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
                    
                    ![Screenshot 2023-10-22 at 6.41.08 AM.png](DSA-Note%201ca69f7969c644dc8a4bde74abbe89b0/Screenshot_2023-10-22_at_6.41.08_AM.png)
                    
                    ![Screenshot 2023-10-22 at 6.41.25 AM.png](DSA-Note%201ca69f7969c644dc8a4bde74abbe89b0/Screenshot_2023-10-22_at_6.41.25_AM.png)
                    
                    ![Screenshot 2023-10-22 at 6.41.37 AM.png](DSA-Note%201ca69f7969c644dc8a4bde74abbe89b0/Screenshot_2023-10-22_at_6.41.37_AM.png)
                    
                    ![Screenshot 2023-10-22 at 6.41.48 AM.png](DSA-Note%201ca69f7969c644dc8a4bde74abbe89b0/Screenshot_2023-10-22_at_6.41.48_AM.png)
                    
                    ![Screenshot 2023-10-22 at 6.42.00 AM.png](DSA-Note%201ca69f7969c644dc8a4bde74abbe89b0/Screenshot_2023-10-22_at_6.42.00_AM.png)
                    
                    ![Screenshot 2023-10-22 at 8.33.22 AM.png](DSA-Note%201ca69f7969c644dc8a4bde74abbe89b0/Screenshot_2023-10-22_at_8.33.22_AM.png)
                    
                    ![Screenshot 2023-10-22 at 6.42.57 AM.png](DSA-Note%201ca69f7969c644dc8a4bde74abbe89b0/Screenshot_2023-10-22_at_6.42.57_AM.png)

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
        
        ![Screenshot 2023-10-30 at 12.06.30 PM.png](DSA-Note%201ca69f7969c644dc8a4bde74abbe89b0/Screenshot_2023-10-30_at_12.06.30_PM.png)
        
        ![Screenshot 2023-10-30 at 12.13.40 PM.png](DSA-Note%201ca69f7969c644dc8a4bde74abbe89b0/Screenshot_2023-10-30_at_12.13.40_PM.png)
        
        - head: beginning of linked list
        - tail: end of linked list
        - Each node has:
            - Info field: store the info
            - Address field: linking nodes (address field that contains reference to the next node — thats why at the tail, the address field is NULL, since there is no next node)
    - Doubly linked list
        
        ![Screenshot 2023-10-30 at 12.14.23 PM.png](DSA-Note%201ca69f7969c644dc8a4bde74abbe89b0/Screenshot_2023-10-30_at_12.14.23_PM.png)
        
        ![Screenshot 2023-10-30 at 12.16.53 PM.png](DSA-Note%201ca69f7969c644dc8a4bde74abbe89b0/Screenshot_2023-10-30_at_12.16.53_PM.png)
        
        - head: the beginning of the linked list
        - tail: the end of linked list
        - Each nodes have:
            - Info field: the actual data
            - Next field: the address of next node
            - Prev field: the address of previous node
    - Circular linked list
        
        ![Screenshot 2023-10-30 at 12.17.30 PM.png](DSA-Note%201ca69f7969c644dc8a4bde74abbe89b0/Screenshot_2023-10-30_at_12.17.30_PM.png)
        
        ![Screenshot 2023-10-30 at 12.17.41 PM.png](DSA-Note%201ca69f7969c644dc8a4bde74abbe89b0/Screenshot_2023-10-30_at_12.17.41_PM.png)
        
        - Can be:
            - Singly: The next pointer of tail points to head
            - Doubly: The previous pointer of head points to tail
        
    - Self-organizing list
        
        ![example of self-organizing list](DSA-Note%201ca69f7969c644dc8a4bde74abbe89b0/Screenshot_2023-10-30_at_2.47.12_PM.png)
        
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
{{< collapse summary="W1 - Introduction to Data Structure" >}}

{{</ collapse >}}
{{< collapse summary="W1 - Introduction to Data Structure" >}}

{{</ collapse >}}
{{< collapse summary="W1 - Introduction to Data Structure" >}}

{{</ collapse >}}
{{< collapse summary="W1 - Introduction to Data Structure" >}}

{{</ collapse >}}
{{< collapse summary="W1 - Introduction to Data Structure" >}}

{{</ collapse >}}
{{< collapse summary="W1 - Introduction to Data Structure" >}}

{{</ collapse >}}
{{< collapse summary="W1 - Introduction to Data Structure" >}}

{{</ collapse >}}
{{< collapse summary="W1 - Introduction to Data Structure" >}}

{{</ collapse >}}
{{< collapse summary="W1 - Introduction to Data Structure" >}}

{{</ collapse >}}
{{< collapse summary="W1 - Introduction to Data Structure" >}}

{{</ collapse >}}
{{< collapse summary="W1 - Introduction to Data Structure" >}}

{{</ collapse >}}
{{< collapse summary="W1 - Introduction to Data Structure" >}}

{{</ collapse >}}
{{< collapse summary="W1 - Introduction to Data Structure" >}}

{{</ collapse >}}
{{< collapse summary="W1 - Introduction to Data Structure" >}}

{{</ collapse >}}
