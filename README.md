```plaintext
+---📁 input_data -- subfolders represent different methodological combinations
|   +---📁 {TCP|ACP_{ST|LT}_{IDP|AOF}    Acronyms:
|                                         # TCP: trench collision point | ACP: arc collision point 
|                                         # ST: short-term approach | LT: long-term approach 
|                                         # IDP: individual data points | AOF: area of formation
|            📄 data.csv
|
+---📁 resources
|        📄 aseismic_ridge_related_parameters.csv
|        📄 PCD_data.csv
|
+---📁 results
|   +---📁 {TCP|ACP_{ST|LT}_{IDP|AOF}
|       |    📄 final_hyperparameters.json
|       |    📄 model_predictions.csv
|       |    📄 performance_metrics.csv
|       |
|       \---📁 shap_values
|           |    📄 aggregated_shaps.csv
|           |    📄 ci_lower_bounds.csv
|           |    📄 ci_upper_bounds.csv
|           |
|           \---📁 shaps_per_sample
|                    📄 sample_0.csv
|                    📄 sample_1.csv
|                    ...
|
\---📁 scripts
         📄 hyperparameter_tuning.ipynb
         📄 shap_values.ipynb
```
