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
* [t-SNE](http://bindog.github.io/blog/2016/06/04/from-sne-to-tsne-to-largevis/)
  - 在高维空间相似的数据点，映射到低维空间距离也是相似的。常规的做法是用欧式距离表示这种相似性，而SNE把这种距离关系转换为一种条件概率来表示相似性.
  - t-SNE算法在SNE的基础上增加了两个改进：一是把SNE变为对称SNE，二是(拥挤问题)在低维空间中采用了t分布代替原来的高斯分布，高维空间不变,对于高维空间中相距较近的点，为了满足p<sub>ij</sub>=q<sub>ij</sub>，低维空间中的距离需要稍小一点；而对于高维空间中相距较远的点，为了满足p<sub>ij</sub>=q<sub>ij</sub>，低维空间中的距离需要更远.
* [Implementations](https://lvdmaaten.github.io/tsne/)

**KL divergence**
* [Kullback–Leibler divergence](https://www.jianshu.com/p/43318a3dc715) (also called relative entropy) is a measure of how 
one probability distribution diverges from a second, expected probability distribution
