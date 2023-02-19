# graphTriangleCounting

This paper implements several exact and approximate triangle counting algorithms from the literature using Python and explores their scalability properties on different real-world data sets. The implemented exact algorithms include the **brute force** algorithm, the **node iterator** algorithm, and the **compact forward** algorithm, while the **DOULION** algorithm is used for approximate triangle counting. Additionally, the streaming algorithm **TRIEST** is explored for triangle counting in dynamic graphs. Our experiments evaluate the performance of each algorithm on different data sets and compare their efficiency in terms of time and space complexity. The results of our study provide a comprehensive evaluation of each algorithm and their scalability properties, which will be valuable for researchers and practitioners who work with large graphs and are interested in efficient triangle counting algorithms.

## The Data

We apply the algorithms to three SNAP datasets. More precisely, we choose two collaboration networks and one spatial network: 
- **Arxiv GR-QC** (General Relativity and Quantum Cosmology) is an undirected collaboration net-work and it regards scientific collaborations between authors of papers submitted to the category of General Relativity and Quantum Cosmology of the e-print Arxiv . Two authors are connected with a link if they are co-authors of a paper.
- **Arxiv COND-MAT** (Condensed Matter Physics) is another undirected collaboration network, where nodes represent authors and links represent co-authorship of papers submitted to Condense Matter category.
- **roadNet-CA**. A road network of California, where nodes repre-sent intersections and undirected edges represent the roads that connect these intersections.

## Conclusions

Firstly, we apply three baseline algorithms, Brute-Force, Node-Iterator, and Compact-Forward, checking the runtimes of all three, while concluding that espe-cially Brute-Force is extremely time-consuming, espe-cially for the largest, road network. We note here that the extremely small clustering coefficient of the last dataset leads to Compact-Forward demanding more time than Node-Iterator – which, in general, is much faster - that needs fewer checks of the neighbors, while additionally, as future work we would suggest trying different sorting methods for Compact-Forward as this part takes up a large amount of the process running time and we would suggest that it could reduce even more time complexity.

We then apply the Doulion algorithm both with No-deIterator and Compact Forward algorithms for differ-ent values of p. The values of accuracy are high (with low variance across our runs), even in the case we keep only 10% of the edges. Regarding the speedups achieved by Doulion, the highest speedup is achieved for p=0.1, which is, in all cases, much higher than those for larger values of p. It is consistently higher when Doulion is combined with NodeIterator than with Compact Forward and the values achieved are higher as the graph gets smaller.

The TRIEST algorithm for estimating the number of triangles in a graph depends on several factors, includ-ing the size of the graph, the sampling rate, and the size of the memory reservoir used by the algorithm. The relationship between these factors and accuracy can be complex and dependent on other factors, but both re-search studies and applications have shown that the algorithm can be effective and accurate in a variety of real-world settings with the appropriate tuning of these parameters. Overall, the TRIEST algorithm offers a powerful and efficient approach to triangle counting in large, dynamic graphs, and can be a valuable tool for data scientists and researchers working with network data.



