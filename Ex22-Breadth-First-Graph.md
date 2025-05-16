# Ex22 Breadth First Graph
## DATE: 16.5.25
## AIM:
To write a printQueue C function of the given graph that is to be traversed in the breadth first manner.

![image](https://github.com/user-attachments/assets/f483f48c-6af0-4027-a993-01c108a50933)


## Algorithm
1. Start by initializing the visited array to track visited nodes.
2. Initialize a queue and enqueue the starting node.
3. Mark the starting node as visited.
4. While the queue is not empty:
   - Dequeue the front element and print it.
   - For every adjacent unvisited node, mark it as visited and enqueue it.
5. Repeat until the queue is empty.   

## Program:
```
/*
Program to traverse graph using BFS
Developed by: MONISH R
RegisterNumber: 212223220061 
*/
void printQueue(struct queue* q) {
  int i = q->front;
 
  if (isEmpty(q)) {
    printf("Queue is empty");
  } else { 
    printf("Queue contains ");
    for (i = q->front; i < q->rear + 1; i++) {
      printf("%d ", q->items[i]);
    }
   }
}
```

## Output:

![Screenshot 2025-05-16 203633](https://github.com/user-attachments/assets/ab2ec6ad-eec7-4752-b031-5ad64a120f34)


## Result:
Thus, the code for the printQueue function of the following graph that is to be traversed in the breadth first manner is implemented successfully.
