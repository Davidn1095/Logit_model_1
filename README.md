# Logit_model_1
Logit models with quantitative explanatory variables.

This code is a comprehensive analysis involving the creation of a statistical model to understand the relationship between diastolic blood pressure and coronary events, followed by model diagnostics and evaluation.

### Data Creation:

- `diastolica`, `coronarios0`, and `coronarios1` are vectors created using the `c()` function. Each vector contains numerical data.
- `diastolica` seems to represent diastolic blood pressure measurements.
- `coronarios0` and `coronarios1` might represent counts of coronary events under different conditions or for different groups.

### Creating a DataFrame:

- `Presion` is a DataFrame created using the `data.frame()` function. It comprises the vectors `diastolica`, `coronarios0`, and `coronarios1`.
- This structure allows for organizing and handling the data more effectively for analysis.

### Displaying Data:

- The code displays the first few rows of the `Presion` DataFrame. This is often done to verify the structure and contents of the data.

### Generalized Linear Model (GLM):

- `Ajuste.Presion` is a GLM fitted using the `glm()` function.
- The model predicts `Coronarios1` and `Coronarios0` (as a binomial response) based on `Diastolica`. This suggests analyzing the relationship between diastolic blood pressure and the occurrence of coronary events.

### Model Summary and Predictions:

- `summary(Ajuste.Presion)` shows a summary of the model, including coefficients and their statistical significance.
- Various `predict()` and `fitted.values()` functions are used to get predictions from the model under different settings (like response type and standard error).

### Predicting New Data:

- New data (`Nuevas.Presion`) is created and predictions are made for this new data using the fitted model.

### Hosmer-Lemeshow Test:

- The `hoslem.test()` from the `ResourceSelection` library is used for goodness-of-fit testing of the model. This test compares observed and predicted values to evaluate the model's fit.

### Confidence Intervals:

- `confint.default()` is used to calculate confidence intervals for the model's parameters. These intervals are then exponentiated (using `exp()`) to be on the original scale of the data.

### Model Comparison:

- Two models (`Ajuste.Presion` and `Ajuste.Presion.0`) are compared using `anova()`. This comparison helps in understanding whether adding `Diastolica` as a predictor significantly improves the model.

### Residuals and Influence Measures:

- Various functions (`residuals()`, `hatvalues()`, `rstandard()`, `cooks.distance()`) are used to evaluate residuals and influential observations in the model. This is crucial for diagnostics and understanding the model's behavior.

