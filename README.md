# ✈️ AeroPulse AI – Flight Delay Prediction System

## 📌 Overview

**AeroPulse AI** is an intelligent flight delay prediction system that uses machine learning and AI-powered assistance to predict flight delays and provide insights. The system combines:

* 📊 Machine Learning model (trained on flight data)
* 🤖 AI Agent (RAG-based assistant)
* 🌐 Interactive Streamlit Web App

---

## 🚀 Features

* ✈️ Flight delay prediction using trained ML model
* 🤖 AI assistant for flight-related queries (RAG-based)
* 📊 Data-driven insights using real dataset
* 🎨 Clean and responsive Streamlit UI
* ⚡ Fast predictions with pre-trained models

---

## 📁 Project Structure

```
FlightDelayPredictor/
│
├── app.py                     # Main Streamlit application
├── build_rag_store.py        # Builds vector database (FAISS)
├── requirements.txt          # Dependencies
├── .env                      # API keys (not shared)
├── env.example               # Example env file
│
├── backend/
│   ├── agents.py             # AI agent logic
│   ├── test.py               # Testing file
│
├── models/
│   ├── flight_delay_model.pkl
│   ├── scaler.pkl
│   ├── le_origin.pkl
│   ├── le_dest.pkl
│   ├── le_carrier.pkl
│
├── data/
│   ├── flights_dataset.csv
│   ├── ann_parameters.csv
│   ├── best_model_parameters.csv
│
├── flight_rag_store/
│   ├── index.faiss
│   ├── index.pkl
│
├── training/
│   ├── train_model.py
│   ├── trim_dataset.ipynb
│
├── assets/
│   ├── aircraft.jpg
│   ├── image.jpg
```

---

## ⚙️ Installation

### 1️⃣ Clone the repository

```bash
git clone <your-repo-link>
cd FlightDelayPredictor
```

### 2️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

---

## 🔑 Environment Variables

Create a `.env` file in the root folder:

```
GROQ_API_KEY=your_api_key_here
```

👉 Without this key, AI agent features will not work.

---

## ▶️ Running the Application

Run the Streamlit app:

```bash
streamlit run app.py
```

Then open in browser:

```
http://localhost:8501
```

---

## 🧠 How It Works

### 🔹 Machine Learning Model

* Trained using historical flight dataset
* Uses features like:

  * Origin
  * Destination
  * Carrier
  * Time-related inputs

### 🔹 AI Agent (RAG)

* Uses FAISS vector store (`flight_rag_store`)
* Retrieves relevant information
* Generates intelligent responses using LLM

### 🔹 Streamlit UI

* User inputs flight details
* Displays:

  * Delay prediction
  * AI-based suggestions

---

## ⚠️ Common Issues

### ❌ App stuck on "Running get_agent(...)"

* Missing or invalid API key
* Slow FAISS loading
* Agent initialization issue

👉 Fix:

* Add correct `GROQ_API_KEY`
* Use caching (`@st.cache_resource`)
* Check `agents.py`

---

### ❌ Module not found

```bash
pip install streamlit python-dotenv scikit-learn pandas
```

---

### ❌ Model file not found

Make sure `/models` folder contains `.pkl` files.

---

## 🛠️ Technologies Used

* Python 🐍
* Streamlit 🌐
* Scikit-learn 🤖
* FAISS 🔍
* Pandas 📊
* dotenv 🔑

---

## 📊 Dataset

* Flight dataset (`flights_dataset.csv`)
* Includes:

  * Flight routes
  * Airlines
  * Delay information

---

## 📌 Future Improvements

* Add real-time flight data API
* Improve model accuracy
* Deploy on cloud (Streamlit Cloud / AWS)
* Add visualization dashboards

---

## 👩‍💻 Team Member

**Rughma MAlik**
**Nimra Mursleen**
BSE (Software Engineering) – Semester 6

---

## 📜 License

This project is for academic and learning purposes.

