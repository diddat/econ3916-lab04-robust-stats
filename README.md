# econ3916-lab04-robust-stats
Objective

I wanted to see how outliers distort standard summary statistics and compare two different methods for catching them in the California Housing dataset.

Methodology
Computed standard and resistant-to-outliers summary statistics (mean, median, trimmed mean, standard deviation, IQR, MAD) on the California Housing dataset (20,640 observations)
Built Tukey Fences by hand to flag price outliers using the IQR
Ran Isolation Forest to flag outliers using all features at once, not just price
Compared which observations each method flagged and found they didn't agree on the same points
Ran a contamination experiment by injecting 5% corrupted values and tracking how each statistic responded
Key Findings
The mean shifted by 67.1% after contamination, while the median shifted by only 3.6%
Tukey Fences and Isolation Forest flagged different sets of observations, since one looks at price alone and the other looks at the full feature set
The statistics that hold up under corruption (median, trimmed mean, MAD) stayed close to their original values, while the mean and standard deviation moved sharply
