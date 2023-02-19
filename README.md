# graphTriangleCounting

This paper implements several exact and approximate triangle counting algorithms from the literature using Python and explores their scalability properties on different real-world data sets. The implemented exact algorithms include the **brute force** algorithm, the **node iterator** algorithm, and the **compact forward** algorithm, while the **DOULION** algorithm is used for approximate triangle counting. Additionally, the streaming algorithm **TRIEST** is explored for triangle counting in dynamic graphs. Our experiments evaluate the performance of each algorithm on different data sets and compare their efficiency in terms of time and space complexity. The results of our study provide a comprehensive evaluation of each algorithm and their scalability properties, which will be valuable for researchers and practitioners who work with large graphs and are interested in efficient triangle counting algorithms.

## The Data

We apply the algorithms to three SNAP datasets. More precisely, we choose two collaboration networks and one spatial network: 
- **Arxiv GR-QC** (General Relativity and Quantum Cosmology) is an undirected collaboration net-work and it regards scientific collaborations between authors of papers submitted to the category of General Relativity and Quantum Cosmology of the e-print Arxiv . Two authors are connected with a link if they are co-authors of a paper.
- **Arxiv COND-MAT** (Condensed Matter Physics) is another undirected collaboration network, where nodes represent authors and links represent co-authorship of papers submitted to Condense Matter category.
- **roadNet-CA**. A road network of California, where nodes repre-sent intersections and undirected edges represent the roads that connect these intersections.

## Conclusions




