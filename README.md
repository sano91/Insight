# Unsupervised learning Guide
### Introduction
Unsupervised learning subsumes all kinds of machine
learning where there is no known output, no teacher to instruct the learning algorithm. In unsupervised learning, the learning algorithm is just shown the input data
and asked to extract knowledge from this data. So there is no way for us to “tell” the algorithm what we
are looking for, and often the only way to evaluate the result of an unsupervised algorithm is to inspect it manually.
### Purpose
Hopefully and maybe, there is some setups, when we can find useful separations, and groupings in the result.
# Scalers
Common practice is to adjust
the features so that the data representation is more suitable for these algorithms.
Often, this is a simple per-feature rescaling and shift of the data.
![alt text](https://i.imgur.com/zREei0h.png "Scalers")
### Standard Scaler
The StandardScaler in scikit-learn ensures that for each
feature the mean is 0 and the variance is 1, bringing all features to the same magni‐
tude. However, this scaling does not ensure any particular minimum and maximum
values for the features.
### Min-Max Scaler
The MinMaxScaler , on the other hand, shifts the data such that all features are exactly
between 0 and 1. For the two-dimensional dataset this means all of the data is con‐
tained within the rectangle created by the x-axis between 0 and 1 and the y-axis
between 0 and 1.
### Robust Scaler
The RobustScaler works similarly to the StandardScaler in
that it ensures statistical properties for each feature that guarantee that they are on the
same scale. However, the RobustScaler uses the median and quartiles, 1 instead of
mean and variance. This makes the RobustScaler ignore data points that are very
different from the rest (like measurement errors). These odd data points are also
called outliers, and can lead to trouble for other scaling techniques.
### Normalizer
Finally, the Normalizer does a very different kind of rescaling. It scales each data
point such that the feature vector has a Euclidean length of 1. In other words, it
projects a data point on the circle (or sphere, in the case of higher dimensions) with a
radius of 1. This means every data point is scaled by a different number (by the
inverse of its length). This normalization is often used when only the direction (or
angle) of the data matters, not the length of the feature vector.
