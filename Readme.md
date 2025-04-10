# 📈 Stock Market Order Matching System

A web-based stock market order matching system that simulates a real trading platform with support for different order types, price bands, and circuit breakers.

## 🔍 Overview

This project combines a C++ order matching engine with a Flask web interface to demonstrate core stock exchange functionality, including:

- ✅ Multiple order types (LIMIT, MARKET, IOC, FOK)
- ✅ Price-time priority matching algorithm
- ✅ Stock-specific price bands
- ✅ Market-wide circuit breakers
- ✅ Order book visualization
- ✅ Trade history tracking

The system allows users to place orders through a web interface, see the order book, and track trading activity through data visualizations.

## ✨ Features

### 🛒 Order Types

- **LIMIT**: An order to buy or sell at a specified price or better
- **MARKET**: An order to execute immediately at the best available price
- **IOC** (Immediate or Cancel): Execute as much as possible immediately, then cancel the rest
- **FOK** (Fill or Kill): Execute the entire order immediately or cancel it entirely

### 🛡️ Market Protections

- **Stock-specific Price Bands**: Prevent orders outside of allowed price ranges
- **Circuit Breakers**: Automatically halt trading during extreme market movements

### 🖥️ UI Features

- Simple order placement form
 <img width="1470" alt="Screenshot 2025-04-10 at 8 02 29 PM" src="https://github.com/user-attachments/assets/62238ca7-ccd2-44a9-aec2-b478101438a5" />

- Order book visualization
 <img width="1470" alt="Screenshot 2025-04-10 at 8 01 21 PM" src="https://github.com/user-attachments/assets/85d3239e-5416-4181-9aec-b41678ea8185" />

- Trade history with timestamps
 <img width="1454" alt="Screenshot 2025-04-10 at 8 01 44 PM" src="https://github.com/user-attachments/assets/af22036c-9f31-454b-bd6a-c296fcfe1625" />

- Interactive charts for market data

## 🏗️ Architecture

The project follows a hybrid architecture:

- **C++ Backend**: High-performance order matching engine
- **Flask Web Server**: Handles HTTP requests and serves the frontend
- **JavaScript Frontend**: Interactive UI with data visualization


## 🚀 Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/stock-market-matching-system.git
   cd stock-market-matching-system
2. Compile the C++ code:
   ```bash
   cd cpp_src
   g++ -std=c++17 orderbook.cpp -o orderbook
   cd ..
3. Install Python dependencies:
   ```bash
   pip install flask
4. Run the application:
   ```bash
   python app.py

## 📖 Usage

### 📝 Placing Orders

1. Enter a stock symbol (e.g., AAPL, MSFT, RELIANCE)
2. Select order type (BUY/SELL)
3. Choose order variant (LIMIT, MARKET, IOC, FOK)
4. Set price and quantity
5. Click "Place Order"

### 📊 Viewing Order Books

1. Enter a stock symbol
2. Click "View Order Book"

### 🔄 Resetting the System

Click the "Reset Order Book" button to clear all orders and trades.

## 🔧 Technical Details

### 💻 C++ Order Matching Engine

- Time-priority price matching algorithm
- Thread-safe with mutex protection
- In-memory order book data structure
- Supports multiple symbols simultaneously

### 🌐 Flask Web Interface

- RESTful API for order placement and retrieval
- Parses C++ program output for web display
- Maintains state between requests
- Chart.js integration for data visualization

## 🔮 Future Enhancements

- 👤 User authentication and account tracking
- 💾 Persistent storage with database integration
- ⚡ WebSockets for real-time updates
- 📊 Enhanced market data analytics
- 🛠️ More sophisticated circuit breaker mechanisms
