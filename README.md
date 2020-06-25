# data-science
Data science tools : exploratory data analysis, prediction, visualization

Core functions for visualizing factor & numeric series

The repository is now private.

See some of these functions in practice here: https://colab.research.google.com/drive/1lkvvmK7uVyqG7dg_H8FGeCeaGlwZyL5L

Notable tools:

Core individual functions (located in core_individual_functions.py): 
  - coarse_cdf()        : Useful for numeric variables with discrete values, i.e. many identical values. Allows us to understand the percentiles of a series, by computing, per percentile, the smallest x such that 
  
      (percentage of observations <=x) >= percentile
      
  - numerical_stats()   : computes a variety of statistics for a numerical variable
  - categorical_stats() : computes a variety of statistics for a categorical variable
  - assign_bin()        : splits a numerical variable into bins of roughly equal size. Deals with discrete series with many identical values: it is guaranteed that each unique value of the series is assigned just 1 bin.
  - fillna_factor()     : replaces missing values of a categorical variable with a placeholder, default: "_missing"
  - clip_factor()       : keeps most frequent values of a categorical variable and replaces the rest with a placeholder, default: "_other"
  - get_counts_per_value() : computes a variety of frequency-related statistics of the levels of a categorical variable

Core functions for two variables (located in core_2d_functions.py):
  - cond_stats_num_num() : for inputs (x, y), computes a variety of statistics of y given x. x is numeric and y is numeric
  - cond_stats_cat_num() : for inputs (x, y), computes a variety of statistics of y given x. x is categorical and y is numeric
  
Individual summary functions (located in individuak_summary_functions.py):
  - summarize_numerical()   : plots a variety of statistics for a numerical variable
  - summarize_categorical() : plots a variety of statistics for a categorical variable

