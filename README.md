🧠 Gold Assay Predictor – AI-Powered Mineral Targeting

This project leverages a machine learning pipeline using XGBoost to predict gold concentrations (Au(ppm)) based on geochemical assay data from drilling samples. It includes spatial and chemical features to identify high-probability gold zones.

🔍 Project Description

The goal of this project is to assist mineral exploration teams in identifying promising drilling targets based on existing assay data. The model predicts the gold content (in ppm) for new samples using features such as lead, zinc, copper, silver, specific gravity, and spatial coordinates.

The model was trained and validated on private client data (not included for confidentiality), achieving:

RMSE ≈ 0.327

R² ≈ 0.585

Predictions are supported by spatial simulations and visualization in both 2D and 3D to assist in field prioritization.

📁 Files

xgb_gold_model.joblib – Trained XGBoost model (regression)

xgb_gold_scaler.joblib – StandardScaler used during training

nuevas_muestras.csv – Template file for input samples (without real data)

predict_new_samples.py – Script to generate predictions from new CSV input

notebooks/ – Contains training notebooks and simulation analysis

🚀 How to Use

Fill out the file nuevas_muestras.csv with new lab samples using the correct headers:

Sample_ID, Pb(%), Zn(%), Cu(%), Ag(ppm), SG(Units), mid_x, mid_y, mid_z

Run the following script to predict gold class:

python predict_new_samples.py

The script will print results and save them to a new file with the predicted class.

🔒 Privacy Notice

This repository does not contain client data. All training and testing was performed locally with confidential datasets. Only the trained model and structure are included.

🧱 Built With

Python 3.10

XGBoost

scikit-learn

Pandas

Matplotlib & Seaborn

📬 Author

César PedrajaToronto, Canada
