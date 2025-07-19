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
