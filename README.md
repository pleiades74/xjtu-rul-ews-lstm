# xjtu-rul-ews-lstm
"Cross-condition bearing remaining useful life prediction using Early Warning Signal (EWS) features and LSTM architectures with attention and domain adaptation"
# Cross-Condition Bearing RUL Prediction with EWS Features and LSTM

Code for the paper: *"Cross-Condition Bearing Prognostics Using Early Warning Signal Features: A Comparative Study of Attention Mechanisms and SHAP-Based Spectral Attribution"*

Thuraya Shaheen – Peter the Great St. Petersburg Polytechnic University

---

## Overview

- 6 LSTM architectures (simple, attention, bidirectional, domain adaptation)
- Wavelet-based Early Warning Signal (EWS) features
- XJTU-SY dataset (15 bearings, 3 operating conditions)
- Multi-seed validation (15 seeds), Bayesian analysis, SHAP interpretability

---
# Usage
Run on Kaggle (recommended):
The notebook was developed and tested on Kaggle with GPU enabled.


## Requirements

```bash
pip install torch numpy pandas scipy scikit-learn matplotlib seaborn pywavelets shap pymc arviz
Usage
Run the notebook xjtu-rul-codes.ipynb and select from the menu:

Option	Description
1-3	Run Split 1/2/3 with LSTM+Attention+DA
4-6	Run splits with Bidirectional LSTM+Attention
14	Run Simple LSTM (baseline)
19	Raw vibration ablation
26-29	Validation suite
Dataset
XJTU-SY bearing dataset: http://biaowang.tech/xjtu-sy-bearing-datasets/

Key Results
Split	Best Model	MAE (min)	R²
40 Hz	bilstm_attn	2.36 ± 0.12	0.412
37.5 Hz	lstm_da	0.712 ± 0.038	0.184
35 Hz	simple_lstm	0.275 ± 0.020	0.556
