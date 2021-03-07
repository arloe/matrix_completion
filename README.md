# Matrix Completion considering heterogeneity
==================================================

Matrix completion for collaborative filtering used in the recommendation system is a problem that has received a lot of attention recently.

Among them, softImpute(Mazumder et al, 2010) show excellent performance.

Since the recommendation system is actually composed of several groups of people, heterogeneity within the matrix is ​​easily observed

However, SoftImpute is not a way to actively reflect this heterogeneity.

Therefore, in this study, we propose an iterative clustering-SoftImpute method that can improve the performance of SoftImpute when there is intra-matrix heterogeneity.