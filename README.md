We have a feature matrix of nonnegative values and want to reduce the dimensionality, Use non-negative matrix factorization (NMF) to reduce the dimensionality of the feature matrix, NMF is an unsupervised technique for linear dimensionality reduction that factorizes (i.e., breaks up
into multiple matrices whose product approximates the original matrix) the feature matrix into matrices
representing the latent relationship between observations and their features. Intuitively, NMF can reduce
dimensionality because in matrix multiplication, the two factors (matrices being multiplied) can have
significantly fewer dimensions than the product matrix. Formally, given a desired number of returned
features, r, NMF factorizes our feature matrix such that:
where V is our n × d feature matrix (i.e., d features, n observations), W is a n × r, and H is an r × d
matrix. By adjusting the value of r we can set the amount of dimensionality reduction desired.
One major requirement of NMA is that, as the name implies, the feature matrix cannot contain negative
values. Additionally, unlike PCA and other techniques we have examined, NMA does not provide us
with the explained variance of the outputted features. Thus, the best way for us to find the optimum
value of n_components is by trying a range of values to find the one that produces the best result in our
end model.
