
---
Federated ClinicalBERT: Privacy-First Multi-Hospital Disease Prediction
---

Healthcare
AIPrivacy 
Built with PyTorch,NLP

---
Overview

This repository implements a Federated Learning framework for disease prediction from clinical notes—enabling multiple hospitals to collaboratively develop a powerful, privacy-preserving NLP model using ClinicalBERT. Patient data remains securely on-site, while only model weights are shared, ensuring HIPAA compliance and real-world healthcare viability.

---
Features

Multi-Hospital Federated Learning: Trains ClinicalBERT models across 5+ hospitals with configurable (uneven) data splits

Privacy-Preserving by Design: Raw data never leaves any site; only encrypted model parameters are exchanged

Automated Multi-Disease Classification: Predicts 13 disease categories (incl. no_disease) from real clinical notes

Advanced Training Pipeline:

Dynamic layer freezing of transformer encoder layers

Model pruning and quantization (for efficient communication)

Macro F1 scoring and class weighting for imbalanced data

Early stopping and progress visualization

Plug-and-play for synthetic or real datasets

---

Business Impact
Improves clinical decision support: faster, more accurate disease detection from unstructured text

Enables HIPAA-compliant collaboration across institutions

Reduces manual review workload and operational costs

Scalable architecture for deployment in real-world healthcare networks

---
Tech Stack
Python 3.12+

PyTorch

HuggingFace Transformers (ClinicalBERT)

Scikit-learn

Matplotlib & Seaborn (visualization)

Jupyter Notebook (development)

MIMIC-III dataset (or your custom CSV data)

---
Getting Started
1. Clone the Repository
bash
git clone https://github.com/Prajwalv28/Federated-Healthcare.git
cd Federated-Healthcare

2. Prepare Your Data
Place your clinical notes CSV file (with disease labels) in the project directory.

Update the notebook’s DATA_PATH variable as needed.

4. Run the Notebook
Open Federated_Uneven.ipynb in Jupyter/Colab as it requires GPU computation

Configure the number of clients, disease classes, federated rounds, and hyperparameters

Run all cells to reproduce the full training, evaluation, and visualizations

5. Visualize and Interpret Results
Data and model distribution plots are auto-generated

Final metrics, confusion matrix, and business impact estimates available in output folder

---

**Example Output**

🚀 STARTING FEDERATED TRAINING
=======================================
ROUND 1/20
🏥 Hospital 1/5 (1990 samples): Loss=1.43
...
🔄 Aggregating...
📈 Round Results: Accuracy=0.79, Macro F1=0.81, Sparsity=30%

---

Project Structure
text
.
├── Federated_Uneven.ipynb         # Main notebook (federated learning pipeline)
├── .csv                           # Example data file (clinical notes w/ disease_label)
├── /output                        # Visualizations, saved models, histories

---

License

MIT License

---
Citation

Emily Alsentzer et al. "Publicly Available Clinical BERT Embeddings", NAACL 2019.

---
Contact
Author: Prajwal Venkat Venkatesh

Questions, feedback, and collaboration proposals: [prajwalvenkatv@gmail.com]

---

Empowering healthcare with scalable, privacy-first AI for better patient outcomes.

---

