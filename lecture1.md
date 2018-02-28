# Image Classification Data-driven Approach k-Nearest Neighbor trainvaltest splits
**Data-driven approach**

**Nearest Neighbor Classifier**
* L1 distance
* L2 distance
* differentce: http://www.chioka.in/differences-between-l1-and-l2-as-loss-function-and-regularization/

**k - Nearest Neighbor**
* find the top k closet images, and have them vote on the label of the test image. higher values of k have a smoothing effect that makes the classier more resistant to outliers, likely leading to better
generalization on the test data

**Validation sets for Hyperparameter tuning**
* Evaluate on the test set only a single time, at the very end.
* **cross-validation**: in 5-fold cross-validation, we would split the training data into 5 equal folds, 
use 4 of them for training, and 1 for validation. We would then iterate over which fold is the validation fold,
evaluate the performance, and finally average the performance across the different folds.

**Pros and Cons of Nearest Neighbor classifier**
* takes no time to train
* heavy computational cost at test time

**Approximate Nearest Neighbor(ANN)**
* algorithm and libraries accelerate the nearst neighbor lookup(e.g.[FLANN](http://www.cs.ubc.ca/research/flann/))

**t-SNE(t-Distributed Stochastic Neighbor Embedding)**
* [t-SNE](https://www.youtube.com/watch?v=RJVL80Gg3lA&list=UUtXKDgv1AVoG88PLl8nGXmw), [youtube](https://www.youtube.com/watch?v=RJVL80Gg3lA&list=UUtXKDgv1AVoG88PLl8nGXmw)
* [Implementations](https://lvdmaaten.github.io/tsne/)

**KL divergence**
* [Kullback–Leibler divergence](https://www.jianshu.com/p/43318a3dc715) (also called relative entropy) is a measure of how 
one probability distribution diverges from a second, expected probability distribution
