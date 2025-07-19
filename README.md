# 🔍 Aave V2 Wallet Credit Scoring

Predict responsible behavior across decentralized wallets using deep learning!  
This project builds a wallet-level credit scoring system based on transaction history from the Aave V2 protocol.

---

## 🚀 Objective

Score each wallet (0–1000 scale) based on its interaction with Aave V2 — rewarding responsible patterns and flagging risky behavior using data-driven insights.

---

## 🧠 How It Works

1. 📦 **Input**: `transactions.json` containing Aave V2 wallet activity
2. 📊 **Feature Extraction**: Calculates behavior metrics per wallet (deposits, repays, liquidations, amount trends, time gaps)
3. 🧪 **Labeling**: Heuristic pseudo-labels reflect responsible usage
4. 🤖 **Model Training**: Deep learning model learns to predict behavioral scores
5. 📈 **Output**: `wallet_scores.csv` with each wallet's credit score

---

## 📂 Project Structure
from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import Dense, Dropout
model = Sequential([
    Dense(128, activation='relu', input_shape=(X_scaled.shape[1],)),
    Dropout(0.3),
    Dense(64, activation='relu'),
    Dropout(0.2),
    Dense(1, activation='sigmoid') 
])

model.compile(optimizer='adam', loss='mse', metrics=['mae'])
y = (
    features.get("deposit", 0) +
    features.get("repay", 0) -
    features.get("liquidationcall", 0)
).clip(lower=0)
from sklearn.preprocessing import MinMaxScaler
y_scaled = MinMaxScaler().fit_transform(y.values.reshape(-1, 1)).flatten()
model.fit(X_scaled, y_scaled, epochs=50, batch_size=32, validation_split=0.2, verbose=1)
