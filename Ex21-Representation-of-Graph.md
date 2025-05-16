# Ex21 Representation of Graph
## DATE: 16.5.25
## AIM:
To write a C program to display the adjacency matrix of the given graph by supplying the edges and the number of vertices.

## Algorithm
1. Start the program and input the number of vertices and edges.
2. Initialize an adjacency matrix with all elements set to 0.
3. For each edge, input the pair of vertices (source and destination).
4. Set the corresponding matrix entries to 1 (for undirected graph, mark both [i][j] and [j][i]).
5. Print the final adjacency matrix.
## Program:
```
/*
Program to display the adjacency matrix of the given graph
Developed by: MONISH R
RegisterNumber:  212223220061
*/
void printAdjMatrix(int arr[][V])
{
     int i, j;
      for(i = 0; i < V; i++)
     {  
         for(j = 0; j < V; j++)
         {   
             printf("%d ", arr[i][j]);
         }
         printf("\n");
     }
}


```

## Output:
![Screenshot 2025-05-16 203343](https://github.com/user-attachments/assets/c4bda52b-7808-449b-b08e-3ea7236c4da2)




## Result:
Thus, the C program to print the adjacency matrix of the given graph is implemented successfully.
