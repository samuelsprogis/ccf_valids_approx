# Description
This code defines an R function that computes cross-correlation values for lags from −2 to 2, using only valid (non-NA) observations at each lag. Cross-correlations are calculated using Pearson’s method. The function also calculates approximate confidence intervals separately for each lag based on the number of valid observations available.

# Usage
Copy the code, paste it into an R session, and run it. The function ccf_valids_approx() can then be called to compute cross-correlations.

The function takes two arguments:
- x: the reference series
- y: the shifted series

A positive lag indicates that y occurs after x, while a negative lag indicates that y occurs before x.

# Output
The function prints a data frame to the console containing the following columns:
- lag: the lag values
- ccf: the cross-correlation at each lag
- n_pairs: the number of valid observations used at each lag
- limit_lower: values for the lower limits of the approximate confidence interval at each lag
- limit_higher: values for the upper limits of the approximate confidence interval at each lag
