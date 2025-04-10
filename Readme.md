Stock Market Order Matching System
A web-based stock market order matching system that simulates a real trading platform with support for different order types, price bands, and circuit breakers.
Overview
This project combines a C++ order matching engine with a Flask web interface to demonstrate core stock exchange functionality, including:

Multiple order types (LIMIT, MARKET, IOC, FOK)
Price-time priority matching algorithm
Stock-specific price bands
Market-wide circuit breakers
Order book visualization
Trade history tracking

The system allows users to place orders through a web interface, see the order book, and track trading activity through data visualizations.
Features
Order Types

LIMIT: An order to buy or sell at a specified price or better
MARKET: An order to execute immediately at the best available price
IOC (Immediate or Cancel): Execute as much as possible immediately, then cancel the rest
FOK (Fill or Kill): Execute the entire order immediately or cancel it entirely

Market Protections

Stock-specific Price Bands: Prevent orders outside of allowed price ranges
Circuit Breakers: Automatically halt trading during extreme market movements

UI Features

Simple order placement form
Order book visualization
Trade history with timestamps
Interactive charts for market data

Architecture
The project follows a hybrid architecture:

C++ Backend: High-performance order matching engine
Flask Web Server: Handles HTTP requests and serves the frontend
JavaScript Frontend: Interactive UI with data visualization

Screenshots
[Insert screenshots of your UI here]
Installation

Clone the repository:
bashgit clone https://github.com/yourusername/stock-market-matching-system.git
cd stock-market-matching-system

Compile the C++ code:
bashcd cpp_src
g++ -std=c++17 orderbook.cpp -o orderbook
cd ..

Install Python dependencies:
bashpip install flask

Run the application:
bashpython app.py

Access the web interface at http://127.0.0.1:5000/

Usage
Placing Orders

Enter a stock symbol (e.g., AAPL, MSFT, RELIANCE)
Select order type (BUY/SELL)
Choose order variant (LIMIT, MARKET, IOC, FOK)
Set price and quantity
Click "Place Order"

Viewing Order Books

Enter a stock symbol
Click "View Order Book"

Resetting the System
Click the "Reset Order Book" button to clear all orders and trades.
Technical Details
C++ Order Matching Engine

Time-priority price matching algorithm
Thread-safe with mutex protection
In-memory order book data structure
Supports multiple symbols simultaneously

Flask Web Interface

RESTful API for order placement and retrieval
Parses C++ program output for web display
Maintains state between requests
Chart.js integration for data visualization

Future Enhancements

User authentication and account tracking
Persistent storage with database integration
WebSockets for real-time updates
Enhanced market data analytics
More sophisticated circuit breaker mechanisms

License
[Insert your license information here]
Acknowledgements
This project was created as a demonstration of stock exchange matching engine principles and does not use real money or securities.
Contact
[Your contact information]