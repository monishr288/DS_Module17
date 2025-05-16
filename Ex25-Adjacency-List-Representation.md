# Ex25 Adjacency List Representation
## DATE: 16.5.25
## AIM:
To write a C program to represent the given graph using the adjacency list.

## Algorithm
1. Define a structure for a node in the adjacency list.
2. Create an array of pointers for each vertex.
3. For each edge (u, v), create a node for `v` and add it to the adjacency list of `u`.
4. Repeat for all edges.
5. Display the adjacency list for all vertices.
## Program:
```
/*
Program to find and display the priority of the operator in the given Postfix expression
Developed by: MONISH R
RegisterNumber:  212223220061
*/
void printGraph(struct Graph* graph)
{
  int v;
  for (v = 0; v < graph->numVertices; v++)
  {
    struct node* temp = graph->adjLists[v];
    printf("Vertex %d: -> ", v);
    while (temp->next!=NULL)
    {
      printf("%d -> ", temp->vertex);
      temp = temp->next;
    }
    printf("%d", temp->vertex);
    printf("\n");
  }
}
```

## Output:

![Screenshot 2025-05-16 204404](https://github.com/user-attachments/assets/831e7afd-7084-4169-a097-d4e42a1496bc)


## Result:
Thus, the C program to represent the given graph using the adjacency list is implemented successfully
