# Clustering

## Kmeans

- Randomly place k centroids into x,y fields 
- Label points to nearest centroid, recenter, relabel
- Iterative
- Simple, scales easily
- `random_state` sets the seed for reproducibility
- Using linear distances, so essential to scale data first
- Non-deterministic
- Greedy algorithm- makes best decision for next step, so possible to get trapped in a local vs global minima - kmeans already does multiple start points under the hood to avoid this happening
- If modeling, split data before clustering and only cluster train dataset.

### Pros

- Tight clusters
- Centroids can be recomputed driving an observation to another cluster
  
### Cons

- Fails when clusters are not circular
- Hard to predict what k should be
- Initial seeds can dramatically affect the results
- Order of the data can affect the results
- Extremely sensitive to scale of the data

## DB Scan: Density-Based Spatial Clustering of Applications with Noise

- Clusters together objects based on the density of the space around them.

- Those with many neighbors will be clustered together, while objects sitting in a low density space will not be placed in a cluster.


## Hierarchical Clustering

- **Bottom-up** - hierarchical agglomerative clustering
- **Top-down** hierarchical divisive clustering
- Good fits for hierarchical clustering: Customers' preferred support channels, classifying biological species, like the animal species, shopping cart analysis.

### Pros of Hierarchical Clustering

- Deciding the number of clusters is intuitive by looking at the dendrogram that is created.
- Relatively easy to implement.

### Cons of Hierarchical Clustering

- Performance does not scale well with amount of data, i.e. the algorithm is quadratic in the number of objects <span class="arithmatex"><span class="MathJax_Preview">O(n)</span><script type="math/tex">O(n)</script></span>

- Less adaptable, i.e. once an instance is assigned to a cluster it cannot be moved around.

- Ability to perform on large datasets is challenging, if not impossible.

- Highly sensitive to outliers.

- The observations which the clustering starts with, i.e. initial seeds, can dramatically affect the results.

- The order of the data can affect the results.