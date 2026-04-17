# 🚨 Fraud Detection App

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge\&logo=python)
![Streamlit](https://img.shields.io/badge/Streamlit-App-red?style=for-the-badge\&logo=streamlit)
![Machine Learning](https://img.shields.io/badge/ML-Model-green?style=for-the-badge\&logo=scikit-learn)
![Status](https://img.shields.io/badge/Status-Active-success?style=for-the-badge)


---

## 📌 Project Overview

This project is a **Fraud Detection Web Application** built using **Machine Learning** and **Streamlit**.
It predicts whether a financial transaction is fraudulent based on user-provided transaction details.

The model is pre-trained and loaded using `joblib`, enabling fast and efficient predictions in real-time.

---

## 📂 Project Structure

```
fraud-detection/
│
├── models/
│   └── fraud_detection_model.pkl   # Trained ML model
│
├── fraud_detection.py             # Streamlit app
├── fraud_detection.ipynb          # Model training notebook
│
└── README.md
```

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/mohamed-geweida/syntexchub-fraud-detection.git
cd fraud-detection
```

### 2. Create a virtual environment (optional but recommended)

```bash
python -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```


---

## 🚀 Usage

Run the Streamlit app:

```bash
streamlit run fraud_detection.py
```

Then open your browser at:

```
http://localhost:8501
```

---

## 🧠 Features

* 🔍 Real-time fraud prediction
* 📊 Interactive UI using Streamlit
* ⚡ Fast inference using pre-trained model
* 🧾 Simple input form for transaction details
* 🚨 Clear fraud/not-fraud result display

---

## 📥 Input Parameters

The app uses the following features:

| Feature          | Description                                    |
| ---------------- | ---------------------------------------------- |
| `type`           | Transaction type (PAYMENT, TRANSFER, CASH_OUT) |
| `amount`         | Transaction amount                             |
| `oldbalanceOrg`  | Sender’s initial balance                       |
| `newbalanceOrig` | Sender’s balance after transaction             |
| `oldbalanceDest` | Receiver’s initial balance                     |
| `newbalanceDest` | Receiver’s balance after transaction           |

---

## 📊 Example

1. Select transaction type
2. Enter balances and amount
3. Click **Predict**

Output:

* ✅ Not Fraud
* ❌ Fraud Detected

---

## 🔧 Technologies Used

* **Python**
* **Streamlit**
* **Pandas**
* **Scikit-learn**
* **Joblib**

---

## 🧪 Model

The trained model is stored in:

```
models/fraud_detection_model.pkl
```

It is loaded in the app using:

```python
model = joblib.load('models/fraud_detection_model.pkl')
```

---

## 🛠️ Troubleshooting

**Issue:** Model not found
✔️ Ensure the path:

```
models/fraud_detection_model.pkl
```

**Issue:** Streamlit not working
✔️ Try:

```bash
pip install --upgrade streamlit
```

**Issue:** Port already in use
✔️ Run:

```bash
streamlit run fraud_detection.py --server.port 8502
```

---

## 👤 Author

**Mohamed Geweida**
🔗 GitHub: [https://github.com/mohamed-geweida](https://github.com/mohamed-geweida)

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repo
2. Create a new branch
3. Submit a pull request

---

## 📄 License

This project is licensed under the **MIT License**.

---

## ⭐ Support

If you like this project, consider giving it a ⭐ on GitHub!

---

### 🔥 Optional Improvements (if you want to upgrade later)

* Add API deployment (FastAPI)
* Add model evaluation metrics in README
* Deploy on Streamlit Cloud / Hugging Face Spaces
* Add Docker support
