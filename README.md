# PCA-with-and-without-standardization
This code performs principal component analysis (PCA) on a dataset using both standardized and unstandardized data to compare the results.

When the data is standardized, each feature (column) is centered around zero and has unit variance. This is done to ensure that each feature is on the same scale, which is important for PCA since it is sensitive to the scale of the features. In this code, the standardized data is created by subtracting the mean of each column from the values in that column and then dividing by the standard deviation of that column.

After standardizing the data, the covariance matrix is computed, and its eigenvectors and eigenvalues are calculated using NumPy's linalg.eig function. The eigenvectors are sorted by their corresponding eigenvalues in descending order, and the principal components are calculated by multiplying the standardized data by the eigenvectors.

The code then plots the data points in the space of the first and second principal components (PCs) using matplotlib's scatter function. This is done for the standardized data using the first two PCs, as well as for the 6th and 7th PCs and the 9th and 10th PCs. The latter two plots show how the data points look when projected onto different pairs of principal components.

Finally, the code repeats the PCA analysis using the original unstandardized data. The resulting plot shows the data points in the space of the first and second PCs without standardization.

The difference between PCA with and without standardization is that PCA on standardized data ensures that each feature is on the same scale, which can improve the accuracy of the PCA results. Without standardization, the PCA results may be biased towards features with higher variances, which could lead to incorrect conclusions. In this code, you can see how the data points look in different principal component spaces with and without standardization.

PCA without standardization:
----
![PCA without standardization](https://user-images.githubusercontent.com/101024664/224537544-3274276c-cc05-4717-9b35-3cdd72370c41.png)
----
PCA with standardization:
-----
![PCA with standardization](https://user-images.githubusercontent.com/101024664/224537581-3cbffd73-e29d-451e-9188-a10006a1e53a.png)
