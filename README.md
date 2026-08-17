# Heart Disease Neural Network


A heart disease prediction project using a neural network implemented from scratch with NumPy.


## Overview


This project implements a small feed-forward neural network from scratch using NumPy.


The goal is to demonstrate the main components of a neural network without relying on high-level machine learning frameworks for model training.


The implementation includes:


- Parameter initialization
- Forward propagation
- ReLU and sigmoid activation functions
- Binary cross-entropy loss
- Backpropagation
- Gradient descent
- Learning-rate tuning
- Classification-threshold tuning
- Final evaluation using multiple classification metrics


## Neural Network Architecture


The neural network uses the following architecture:

22 → 16 → 8 → 1
Input layer: 22 features
Hidden layer 1: 16 neurons with ReLU activation
Hidden layer 2: 8 neurons with ReLU activation
Output layer: 1 neuron with sigmoid activation

The model is intentionally small given the limited dataset size.

Data Split

The available training data is divided into:

80% training data
20% validation data

A separate held-out test set is kept untouched until final evaluation.

The split is stratified and uses a fixed random state of 42.

Hyperparameter Tuning

The learning rate is selected using the validation set based on F1-score.

The classification threshold is also selected using the validation set based on F1-score.

The held-out test set is not used for selecting either of these values.

Selected Values
Learning rate: 0.005
Classification threshold: 0.70
Training epochs: 1000

Among the evaluated thresholds, 0.70 achieved the highest validation F1-score.

Results

The final model was evaluated on the held-out test set.

Metric    	Score
Accuracy	85.25%
Precision	95.24%
Recall	    71.43%
F1-score	81.63%
ROC-AUC	    92.42%

The model achieved a test accuracy of approximately 85.2% on the held-out test set.

Evaluation

The final evaluation includes:

Accuracy
Precision
Recall
F1-score
ROC-AUC
Confusion matrix
ROC curve
Limitations

This is an educational machine learning project.

The dataset is relatively small, so the reported performance should not be interpreted as evidence of real-world clinical effectiveness.

The model has not been clinically validated and should not be used for medical diagnosis or treatment decisions.

Project Structure
heart-disease-neural-network/
│
├── data/
├── notebooks/
│   ├── 01_eda.ipynb
│   └── 02_nnfs.ipynb
├── results/
├── src/
├── .gitignore
└── README.md

How to Run

Clone the repository and open the notebooks using Jupyter Notebook or VS Code.

Install the required Python packages and run the notebooks from top to bottom.

The neural network implementation is contained in:

notebooks/02_nnfs.ipynb
Disclaimer

This project is intended for educational and research purposes only.

The model is not designed, validated, or approved for real-world medical diagnosis or clinical use.

The reported metrics were obtained on a small held-out test set and should not be interpreted as clinical performance.
