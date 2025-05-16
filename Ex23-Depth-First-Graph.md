# Ex23 Depth First Graph
## DATE: 16.5.25
## AIM:
To compose the code for the function createNode to traverse the graph below in the depth first fashion.

![image](https://github.com/user-attachments/assets/63552824-d0a3-49c6-a473-6db27d1f03e4)

## Algorithm
1. Create a node structure using a linked list to store graph nodes.
2. Initialize the graph using adjacency list representation.
3. Use `createNode()` function to build the adjacency list.
4. Use DFS recursive logic to visit unvisited adjacent nodes.
5. Mark each visited node and print during traversal.  

## Program:
```
/*
Program to traverse the graph below in the depth first fashion
Developed by: MONISH R
RegisterNumber:  212223220061
*/
struct node* createNode(int v) {
  struct node* newNode = malloc(sizeof(struct node));
  newNode->vertex = v;
  newNode->next = NULL;
  return newNode;
}

```

## Output:

![Screenshot 2025-05-16 203839](https://github.com/user-attachments/assets/64b1460f-7592-4206-a0a1-99eeae6e9578)


## Result:
Thus, the C code for the function createNode to traverse the graph below in the depth first fashion is implemented successfully
