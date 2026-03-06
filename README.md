# Proximal Sensing for Bean Nutrient Prediction

📋 **Overview**
This repository contains the code and analysis for predicting mineral nutrient concentrations in common bean (Phaseolus vulgaris L.) grains using proximal sensing techniques. The study combines pXRF (Portable X-ray Fluorescence) and Vis-NIR-SWIR spectroscopy with chemometric modeling to estimate macronutrients (N, P, K, Ca, S) and micronutrients (Mn, Fe, Cu, Zn, Se) in 144 bean samples.

🎯 **Objectives**
Evaluate the potential of pXRF and Vis-NIR-SWIR sensors for rapid nutrient prediction

Compare three machine learning algorithms: PLS, SVR, and Random Forest

Assess the benefit of combining both sensor datasets

Validate models using rigorous 10×5-fold cross-validation

📊 **Dataset**
The repository uses three CSV files (semicolon-separated):

*icp_oes.csv: Reference concentrations from ICP-OES analysis

+pxrf.csv: Elemental data from portable X-ray fluorescence

*nir.csv: Spectral data from Vis-NIR-SWIR spectroscopy

All files share a common ID column for sample matching.

🧪 **Methodology**
### Data Preprocessing
*PCA dimensionality reduction applied to Vis-NIR-SWIR spectra

*Components explaining ≥95% variance retained (typically 5-10 PCs)

*No additional spectral pretreatments applied

### Models Evaluated
| Model | Description | Key Parameters |
|-------|-------------|----------------|
| PLS | Partial Least Squares regression | n_components ≤ 5 |
| SVR | Support Vector Regression | RBF kernel, C=10, gamma='scale' |
| RF | Random Forest | n_estimators=100, max_depth=10 |

📈 **Key Visualizations**
*Mean NIR Spectrum
*PCA scree plot showing explained variance
*Score plots for PC1 vs PC2
*R² heatmaps across all element-model-instrument combinations
*RPD heatmaps with color-coded interpretation thresholds
*Best models performances
