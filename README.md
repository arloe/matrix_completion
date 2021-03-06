### Matrix Completion considering heterogeneity
iterative clustering-SoftImpute

### Introduction
Matrix completion for collaborative filtering used in the recommendation system is a problem that has received a lot of attention recently. Among them, softImpute(Mazumder et al, 2010) show excellent performance. Since the recommendation system is actually composed of several groups of people, heterogeneity within the matrix is ​​easily observed. However, SoftImpute is not a way to actively reflect this heterogeneity.
Therefore, in this study, we propose an iterative clustering-SoftImpute method that can improve the performance of SoftImpute when there is intra-matrix heterogeneity.

### Usage
```R
source("make_simulation_matrix.R")
source("cluster_softImpute.R")

# generate matrix with heterogeneity
mat_org  <- make_simulation_matrix(n = 500, p = 50, group = 4)
# missing value
mat_NA   <- matrix_NA(x = mat_org, prob = .8)
# iterative clustering-softImpute
mat_pred <- cluster_softImpute(X = movielen)
```
### Simulation study
Experiments were conducted using three scenarios and actual data(movielen 100K). As a result of the experiment, it was confirmed that the proposed method has improved performance compared to the existing method.

![graph](https://github.com/arloe/iterative_clustering_softImpute/blob/main/img/simulation%20study.PNG)

### Reference
 * R Mazumder, T Hastie, R Tibshirani, Spectral Regularization Algorithms for Learning Large Incomplete Matrices, Journal of Machine Learning Research, 11:2287–2322, 2010
 * T Hastie, R Mazumder, J Lee, R Zadeh, Matrix Completion and Low-Rank SVD via Fast Alternating Least Squares, Journal of Machine Learning Research, 16:3367-3402, 2015
