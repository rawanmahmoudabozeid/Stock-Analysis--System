# 📈 Stock Market Analysis System

An interactive Streamlit web app for real-time stock data visualization and analysis.

## Features
- 🔍 Real-time stock lookup via **yfinance**
- 📊 **Candlestick** and **Line** charts (7-day & 1-month windows)
- 📉 Moving Averages overlay (MA5, MA10)
- 📋 Full OHLCV data table
- 🗄️ MySQL search history logging
- 🌙 Premium dark-mode UI

## Setup

### 1. Install dependencies
```bash
pip install -r requirements.txt
```

### 2. Configure MySQL (optional)
- Import `schema.sql` into your MySQL server:
  ```bash
  mysql -u root -p < schema.sql
  ```
- Update `DB_CONFIG` at the top of `app.py` with your credentials.

### 3. Run the app
```bash
streamlit run app.py
```

## Project Structure
```
stock_market_app/
├── app.py           ← Main Streamlit application
├── schema.sql       ← MySQL database schema + seed data
├── requirements.txt ← Python dependencies
└── README.md        ← This file
```

## DB_CONFIG (in app.py)
```python
DB_CONFIG = {
    "host":     "localhost",
