# data-science
Data science tools : exploratory data analysis, prediction, visualization

The repository is now private.

See some of these functions in practice here:
  - Data analysis: https://colab.research.google.com/drive/1lkvvmK7uVyqG7dg_H8FGeCeaGlwZyL5L
  - Prediction : https://colab.research.google.com/drive/1RrmsTrUKPmqrbp9COPfpOT9eX-DNjMah

# Notable tools

<details>
  <summary> Analysis </summary>

  <details>
    <summary> One variable </summary>
  

   - `coarse_cdf`        : Useful for numeric variables with discrete values, i.e. many identical values. Allows us to understand the percentiles of a series, by computing,
    per percentile, the smallest x such that 
    
        (percentage of observations <=x) >= percentile
   - `numerical_stats`   : computes a variety of statistics for a numerical variable
   - `categorical_stats` : computes a variety of statistics for a categorical variable
   - `assign_bin`        : splits a numerical variable into bins of roughly equal size. Deals with discrete series with many identical values: it is guaranteed that each unique value of the series is assigned just 1 bin.
   - `fillna_factor`     : replaces missing values of a categorical variable with a placeholder, default: "_missing"
   - `clip_factor`       : keeps most frequent values of a categorical variable and replaces the rest with a placeholder, default: "_other"
   - `get_counts_per_value` : computes a variety of frequency-related statistics of the levels of a categorical variable
   - `summarize_numerical`   : plots a variety of statistics for a numerical variable
   - `summarize_categorical` : plots a variety of statistics for a categorical variable

  </details>

  <details>
    <summary> Two variables </summary>

   - `cond_stats_num_num` : for inputs (x, y), computes a variety of statistics of y given x. x is numeric and y is numeric
   - `cond_stats_cat_num` : for inputs (x, y), computes a variety of statistics of y given x. x is categorical and y is numeric
  </details>
</details>

<details>
  <summary> Prediction </summary>
  
   - `DesignMatrix`: a comprehensive tool which transforms a Pandas dataframe to a numerical numpy array. `fit` method learns dataset metadata and `transform()` method transforms the dataset to a numerical numpy array according to the metadata. Deals with missing values, categorical and numerical variables. For categorical variables, `fit` method follows [this logic](https://aciupan.github.io/assets/img/Fit.png), and `transform` method follows [this logic](https://aciupan.github.io/assets/img/Transform.png). Essentially, the presence of missing values in the training dataset determines whether we consider missing values to be a natural part of this specific column.
   
   - `BaselinePrediction`: a tool which performs fast linear prediction on Pandas dataframes. Deals with missing values, categorical and numerical variables. It is showcased [here](https://colab.research.google.com/drive/1RrmsTrUKPmqrbp9COPfpOT9eX-DNjMah)
  </details>
</details>

