# Ex24 Topological Sort
## DATE: 16.5.25
## AIM:
To compose the code to determine whether the topological ordering for the following graph is possible or not.

![image](https://github.com/user-attachments/assets/c74a7111-9b59-475c-aad4-9baf23d50ec0)


## Algorithm
1. Create a graph using an adjacency list representation.
2. Calculate the in-degree (number of incoming edges) for all vertices.
3. Use a queue to enqueue vertices with 0 in-degree.
4. Perform the topological sort using Kahn's Algorithm:
   - Dequeue vertex, print/store it.
   - Decrease in-degree of adjacent vertices.
   - If in-degree becomes 0, enqueue them.
5. If the number of visited nodes equals the total vertices, topological order is possible. Else, the graph has a cycle.
 

## Program:
```
/*
Program to determine whether the topological ordering for the following graph is possible or not
Developed by: MONISH R
RegisterNumber: 212223220061 
*/
int main()
{
        int i,v,count,topo_order[MAX],indeg[MAX];

        create_graph();

        /*Find the indegree of each vertex*/
        for(i=0;i<n;i++)
        {
                indeg[i] = indegree(i);
                if( indeg[i] == 0 )
                        insert_queue(i);
        }

        count = 0;

        while(  !isEmpty_queue( ) && count < n )
        {
                v = delete_queue();
        topo_order[++count] = v; /*Add vertex v to topo_order array*/
                /*Delete all edges going from vertex v */
                for(i=0; i<n; i++)
                {
                        if(adj[v][i] == 1)
                        {
                                adj[v][i] = 0;
                                indeg[i] = indeg[i]-1;
                                if(indeg[i] == 0)
                                        insert_queue(i);
                        }
                }
        }

        if( count < n )
        {
                printf("No topological ordering possible, graph contains cycle\n");
                exit(1);
        }
        printf("Vertices in topological order are :\n");
        for(i=1; i<=count; i++)
                printf( "%d ",topo_order[i] );
        printf("\n");

        return 0;
}/*End of main()*/
```

## Output:


![Screenshot 2025-05-16 203951](https://github.com/user-attachments/assets/93d0d9f4-73ab-4eba-b01e-ec0fa741c953)

## Result:
Thus, the C program for determining whether the topological ordering for the following graph is possible or not, is implemented successfully.
