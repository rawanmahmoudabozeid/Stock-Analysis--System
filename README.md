📈 Stock Market Analysis System
An interactive Streamlit web app for real-time stock data visualization and analysis.

Features
🔍 Real-time stock lookup via yfinance
📊 Candlestick and Line charts (7-day & 1-month windows)
📉 Moving Averages overlay (MA5, MA10)
📋 Full OHLCV data table
🗄️ MySQL search history logging
🌙 Premium dark-mode UI
Setup
1. Install dependencies
pip install -r requirements.txt
2. Configure MySQL (optional)
Import schema.sql into your MySQL server:
mysql -u root -p < schema.sql
Update DB_CONFIG at the top of app.py with your credentials.
3. Run the app
streamlit run app.py
Project Structure
stock_market_app/
├── app.py           ← Main Streamlit application
├── schema.sql       ← MySQL database schema + seed data
├── requirements.txt ← Python dependencies
└── README.md        ← This file
DB_CONFIG (in app.py)
DB_CONFIG = {
    "host":     "localhost",
    "port":     3306,
    "user":     "root",       # ← your MySQL username
    "password": "",           # ← your MySQL password
    "database": "stock_db",
}
The app works fully without MySQL — DB logging is silently skipped if the connection fails.
