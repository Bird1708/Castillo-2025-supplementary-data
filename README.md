```plaintext
+---📁 input_data
|   +---📁 ACP_LT_AOF
|            📄 data.csv
|
+---📁 resources
|        📄 aseismic_ridge_related_parameters.csv
|        📄 PCD_data.csv
|
+---📁 results
|   +---📁 TCP_ST_IDP
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
|
\---📁 scripts
         📄 hyperparameter_tuning.ipynb
         📄 shap_values.ipynb
```
