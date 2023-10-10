# MDS-Manifold-Learning
Manifold learning is an approach to non-linear dimensionality reduction. A better option than PCA because it assumes a linear relationship between features.
Multidimensional scaling (MDS) seeks a low-dimensional representation of the data in which the distances respect well the distances in the original high-dimensional space.
In general, MDS is a technique used for analyzing similarity or dissimilarity data. It attempts to model similarity or dissimilarity data as distances in a geometric spaces. The data can be ratings of similarity between objects, interaction frequencies of molecules, or trade indices between countries.

Working with large data presents many challenges, one of them being a loss of efficiency and performance in your models due to too high dimensionality.
Luckily, many dimensionality reduction techniques are available that can help us overcome challenges by enabling us to remove “less important” data.
In general, the metric MDS calculates distances between each pair of points in the original high-dimensional space and then maps it to lower-dimensional space while preserving those distances between points as well as possible.
Note, the number of dimensions for the lower-dimensional space can be chosen by you. Typically, one would choose either 2D or 3D as it allows for the data to be visualized.
Multiple approaches can be used to optimize the above cost function, such as Kruskal’s steepest descent method or De Leeuw’s iterative majorization method. However, 
One important thing to note is that both aforementioned methods are iterative approaches, sometimes giving different results since they are sensitive to the initial starting position.
However, Sklearn’s implementation of MDS allows us to specify how many times we want to initialize the process. In the end, the configuration with the lowest stress is picked as the final result.
Steps used by metric MDS algorithm:
Step 1 — The algorithm calculates distances between each pair of points. 
Step 2 — With the original distances known, the algorithm attempts to solve the optimization problem by finding a set of coordinates in a lower-dimensional space that minimizes the value of Stress.
