### Correlations among nuisance regressors

Plot of correlations among confound regressors. This can be used to guide selection of a confound model or to assess the extent to which tissue-specific regressors correlate with global signal. 

The left-hand panel shows the matrix of correlations among selected confound time series as a heat-map. Note the zero-correlation blocks near the diagonal; these correspond to each CompCor decomposition. The right-hand panel displays the correlation of selected confound time series with the mean global signal computed across the whole brain; the regressors shown are those with greatest correlation with the global signal. This information can be used to diagnose partial volume effects. (how?)

High correlations can maybe explained by a motion that caused a signal change in one tissue type that affects the other.

Similarly, the bar chart shows the extent of correlation between the different tissue specific regressors and the global signal.

The components shows high correlation could be considered as the nuisance regressors and used in the model.