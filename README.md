```plaintext
+---📁 input_data -- subfolders represent different methodological combinations
|   +---📁 {TCP|ACP}_{ST|LT}_{IDP|AOF} -- acronyms:
|                                          # TCP: trench collision point | ACP: arc collision point 
|                                          # ST: short-term approach | LT: long-term approach 
|                                          # IDP: individual data points | AOF: area of formation
|            📄 data.csv
|
+---📁 resources
|        📄 aseismic_ridge_related_parameters.csv
|        📄 PCD_data.csv
|
+---📁 results_restricted -- models trained using a constrained hyperparameter space
|   +---📁 {TCP|ACP}_{ST|LT}_{IDP|AOF}
|       |    📄 final_hyperparameters.json -- best hyperparameters found after tuning
|       |    📄 performance_metrics.csv -- model performance results for each cross-validation (N=1000)
|       |
|       \---📁 shap_values
|           |    📄 aggregated_shaps.csv -- median SHAP values per sample and parameter
|           |    📄 ci_lower_bounds.csv -- 95% confidence interval lower limit around the median
|           |    📄 ci_upper_bounds.csv -- 95% confidence interval upper limit around the median
|           |
|           \---📁 shaps_per_sample -- individual SHAP values per sample (deposits/regions) stored as separated CSV files
|                    📄 sample_0.csv -- data structure:
|                                        # rows: normal convergence rate, subducting ocean floor age, obliquity of subduction, migration rate x distance
|                                        # columns: individual cross-validation results (N=1000)
|                    ...
|
+---📁 results_wide -- models trained using a wide hyperparameter space 
|   +---📁 {TCP|ACP}_{ST|LT}_{IDP|AOF}
|       |    📄 final_hyperparameters.json -- best hyperparameters found after tuning
|       |    📄 model_predictions.csv -- main model's predictions within our defined spatiotemporal window
|       |    📄 performance_metrics.csv -- model performance results for each cross-validation (N=1000)
|       |
|       \---📁 shap_values
|           |    📄 aggregated_shaps.csv -- median SHAP values per sample and parameter
|           |    📄 ci_lower_bounds.csv -- 95% confidence interval lower limit around the median
|           |    📄 ci_upper_bounds.csv -- 95% confidence interval upper limit around the median
|           |
|           \---📁 shaps_per_sample -- individual SHAP values per sample (deposits/regions) stored as separated CSV files
|                    📄 sample_0.csv -- data structure:
|                                        # rows: normal convergence rate, subducting ocean floor age, obliquity of subduction, migration rate x distance
|                                        # columns: individual cross-validation results (N=1000)
|                    ...
|
\---📁 scripts
         📄 hyperparameter_tuning.ipynb -- find best hyperparameters for each input data file
         📄 shap_values.ipynb -- compute SHAP values and performance metrics
         📄 environment.yml -- recreate full conda environment and install all dependencies

This work is licensed under a [Creative Commons Attribution-NonCommercial 4.0 International License] (http://creativecommons.org/licenses/by-nc/4.0/).
```
