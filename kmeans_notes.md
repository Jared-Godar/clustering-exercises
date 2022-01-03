# Clustering

## Kmeans

- Randomly place k centroids into x,y fields 
- Label points to nearest centroid, recenter, relabel
- Iterative
- Simple, scales easily
- `random_state` sets the seed for reproducibility
- Using linear distances, so essential to scale data first

### Pros

- Tight clusters
- Centroids can be recomputed driving an observation to another cluster
  
### Cons

- Fails when clusters are not circular
- Hard to predict what k should be
- Initial seeds can dramatically affect the results
- Order of the data can affect the results
- Extremely sensitive to scale of the data

## DB Scan

## Hierarchical Clustering

- **Bottom-up** - hierarchical agglomerative clustering
- **Top-down** hierarchical divisive clustering
- Good fits for hierarchical clustering: Customers' preferred support channels, classifying biological species, like the animal species, shopping cart analysis.
