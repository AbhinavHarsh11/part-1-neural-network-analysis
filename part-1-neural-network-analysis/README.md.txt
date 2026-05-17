# Part 1: Neural Network Fundamentals and Training Behavior Analysis

## Project Overview

This project builds a feed-forward neural network to predict customer churn using structured customer data. The objective is to demonstrate how neural networks learn through forward propagation, loss calculation, backpropagation, and parameter updates.

The model predicts whether a customer will leave the company (`churn = 1`) or remain (`churn = 0`).

---

## Dataset Information

This project uses the `customer_churn_nn.csv` dataset from the synthetic dataset pack provided for the assignment.

Dataset documentation states that the target column is `churn`, where `1 = customer churned` and `0 = customer retained`, and `customer_id` should not be used as a predictive feature. :contentReference[oaicite:0]{index=0}

### Target Variable
- `churn` (Binary Classification)

### Categorical Features
- region
- plan_type
- contract_type
- payment_method

### Numerical Features
- tenure
- monthly_charges
- login_days_last_30
- support_tickets
- avg_response_delay
- data_usage_gb
- satisfaction_score
- days_since_last_complaint
- discounts_used
- referrals

### Identifier
- customer_id (dropped before training)

---

## Tasks Completed

1. Dataset exploration and statistical summary
2. Missing value analysis
3. Target distribution visualization
4. Data preprocessing
5. Neural network model building
6. Model training and evaluation
7. Hyperparameter experimentation
8. Final conceptual reflection

---

## Data Preprocessing

- Removed `customer_id`
- Checked for missing values
- One-hot encoded categorical variables
- Standardized numerical features
- Split data into training and testing sets (80/20)

---

## Neural Network Architecture

- Input Layer
- Hidden Layer 1: 64 neurons, ReLU activation
- Hidden Layer 2: 32 neurons, ReLU activation
- Output Layer: 1 neuron, Sigmoid activation

### Loss Function
- Binary Crossentropy

### Optimizer
- Adam

### Evaluation Metric
- Accuracy

---

## Model Performance

The model was evaluated using:
- Training Accuracy and Loss
- Testing Accuracy and Loss
- Classification Report
- Confusion Matrix

Training and validation curves were also plotted to monitor learning behavior.

---

## Hyperparameter Experiments

Three experiments were conducted by changing:
- Number of neurons
- Learning rate
- Batch size
- Number of epochs
- Activation function

Results were saved in:
- `results/model_comparison.csv`

---

## Final Reflection

### Weights and Biases
Weights determine the importance of each feature. Biases shift the neuron activation threshold.

### Activation Functions
Activation functions introduce non-linearity, enabling the model to learn complex patterns.

### Learning Rate
- Too high: training becomes unstable and may not converge.
- Too low: training is very slow and may get stuck.

### Underfitting and Overfitting
Underfitting occurs when the model is too simple to learn patterns. Overfitting occurs when the model performs well on training data but poorly on unseen test data.

---

## Repository Structure

```text
part-1-neural-network-analysis/
│
├── notebook.ipynb
├── README.md
├── requirements.txt
└── results/
    ├── target_distribution.png
    ├── confusion_matrix.png
    ├── training_curves.png
    ├── model_comparison.csv
    └── sample_predictions.csv