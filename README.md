# Power Output Prediction using Artificial Neural Network

## Overview
This project builds a regression model using a **PyTorch Artificial Neural Network (ANN)** to predict the energy output of a power plant based on environmental conditions.

The model learns the relationship between atmospheric variables and the electrical power output.

---

## Dataset

The dataset contains environmental measurements and the corresponding power output.

### Features
- **AT** – Atmospheric Temperature  
- **V** – Exhaust Vacuum  
- **AP** – Atmospheric Pressure  
- **RH** – Relative Humidity  

### Target
- **PE** – Power Output

---

## Project Workflow

1. Load dataset using **Pandas**
2. Split the dataset into **training and testing sets**
3. Apply **feature scaling using StandardScaler**
4. Convert data to **PyTorch tensors**
5. Use **DataLoader** for batch training
6. Build an **Artificial Neural Network**
7. Train the model and track **training & validation loss**
8. Save the **best model during training**
9. Evaluate the model using **MSE and R² score**

---

## Model Architecture

Neural Network structure:

```
Input Layer → Hidden Layer → Hidden Layer → Output Layer
4 → 6 → 6 → 1
```

Activation Function:
```
ReLU
```

Loss Function:
```
Mean Squared Error (MSE)
```

Optimizer:
```
Adam
```

---

## Training Details

- Epochs: **100**
- Batch Size: **32**
- Best model saved as: **best_model.pt**
- Validation loss monitored during training

---

## Results

Training MSE: **~20**

Testing MSE: **~18**

R² Score: **0.93**

The model explains about **93% of the variance** in the target variable.

---

## Project Structure

```
.
├── ANN.ipynb
├── Powerplant dataset.csv
├── best_model.pt
└── README.md
```

---

## Technologies Used

- Python
- PyTorch
- Pandas
- Scikit-learn
- Matplotlib

---

## How to Run

Clone the repository:

```
git clone https://github.com/yourusername/repository-name.git
```

Install dependencies:

```
pip install torch pandas scikit-learn matplotlib
```

Run the notebook:

```
ANN.ipynb
```

---
