```
Group members:
Dinank Vashistha | 2018B5A71055H
Jamal | 2018A8PS1092H
```

## Block 1
This is same for both algorithms  
Libraries needed:

- networkx
- matplotlib
- numpy
- time
## PageRank
### Block 2

Power Iteration Method Core function  

1. Takes input as transition matrix
2. Initializes a starting probability vector with weights as 1/N
3. Applies power iteration for a default 10,000 rounds, in which it multiplies the transition matrix T and result vector, normalize it, check for convergence and repeat. 

### Block 3

Linear Equation solver method core function  

1. Takes input as transition matrix
2. Finds eigenvector of matrix using eig function of numpy package
3. Selects the left eigenvector based on eigen value as 1

### Block 4

1. Creates a networkx graph, makes it directed.
2. Count the number of nodes and plot the graph.  

### Block 5

1. Graph G is converted to adjacency matrix A.
2. Based on hyperparameter of teleportation, a new adjacency matrix is also created with teleportation enabled.

### Block 6

1. All four combinations are computed and stored.  
   1.1 Power iteration without teleportation  
   1.2 Power iteration with teleportation with prob = 0.1  
   1.3 Linear equation solving without teleportation  
   1.4 Linear equation solving with teleportation with prob = 0.1   
2. Creates dictionaries with node and pagerank values for each methods, and then displays them beautifully, in decreasing order of pagerank values along with node numbers  

### Block 7

1. Creates a random matrix ranging from size 10 to 500.  
2. Runs both, power iteration and linear solving methods on all of these matrices.
3. Running time of each matrix is stored along with number of edges.
4. Plots for both methods are drawn for time taken vs No. of edges.  

---

## HITS
### Block 2

HITS method core function  

1. Takes input as graph
2. Initializes starting hubs and authorities dictionaries.
3. Applies HITS algorithm for given no. of iterations, summing over all the values of hubs and authorities, and then normalizing them.
4. After each iteration the results are checked with tolerance levels  s

### Block 3

1. Initializes the graph from gpickle file and plots it.  

### Block 4

1. Takes the query term, creates root and base sets.
2. Sorts the root and base sets, and also prints the removed nodes.
3. Removes the nodes from actual graph, and runs hits algorithm on resulting graph, with iterations = 100  

### Block 5
1. Dictionaries are created to store node's (in base set) hub and auth scores.  
2. These values are sorted in decreasing values of scores.
3. Top 5 are selected to display the results, along with node numbers and calculated hub and auth scores.  
4. Total time taken to calcualte the result is shown, and the graph G is plotted again after node removal.

### Block 6

1. Creates the whole graph
2. Removes varying number of nodes from the graph, to decrease the number of edges.
3. Runs HITS algorithm on the resulting graph
4. Time taken is stored along with the number of edges in the graoh.
5. Time taken vs No. of edges graph is plotted.