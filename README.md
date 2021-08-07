# SelfOrganizingFeatureMap

Version: 1.0
Simple SOFM built using python numpy, pandas, and scipy. Applied to two datasets from The UCI repository.

This SOFM includes a concept I contrived: "hoodarea".
The values "hoodarea" and "hoodweight" work together to improve clustering accurracy and help ensure that
no neuron remains isolated during the algorithm's execution. It works like this:
whenever a neuron is selected to approach a data point, other neurons close to this "winning" neuron (maintaining a
euclidean distance less than the engineer's specified hoodarea) are also engaged and brought closer to the data point.
Their engagement, however, is scaled by hoodweight, which should be less than one.

The absenteeism dataset is organized relative to all variables but reduced to 2 dimensions for display, while 
buddymove dataset is reduced to 2 dimensions prior to organization by the algorithm.

In version 1.0, chosen datasets are semi-arbitrary and do not provide useful results. Variables chosen during
dimensionality reduction are also arbitrary. Future versions will perform regression or similar mathematical operations
to determine best variables for reduction, and more suitable datasets will be applied.
