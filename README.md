# 📈 Cuarta — Stock Investment Simulator

> A virtual stock market simulator that models how investors, brokers, companies, and a stock exchange interact within a simulated financial market.

## 📌 System Overview

**Cuarta** is an educational stock investment simulator designed to recreate the basic processes involved in participating in a stock market without using real money.

The system provides users with **virtual funds** that they can use to purchase and sell shares of simulated companies. Users can monitor their investments, manage their portfolios, review transaction records, and observe how changes in stock prices affect the value of their holdings.

The simulator models the interaction between **investors, brokers, companies, and the stock exchange**, creating a simplified representation of a functioning stock market.

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| **Python** | Core programming language and business logic |
| **Django** | Web framework and backend |
| **MySQL** | Relational database for storing system data |
| **HTML** | Web page structure |
| **CSS** | User interface styling |
| **JavaScript** | Client-side interactions and dynamic features |
| **Pandas** | Financial and market data processing |
| **Matplotlib** | Stock price and portfolio data visualization |
| **Git** | Version control |
| **GitHub** | Source code hosting and collaboration |

### Architecture

```text
┌─────────────────────────────────────────────┐
│                  FRONTEND                   │
│          HTML • CSS • JavaScript            │
└──────────────────────┬──────────────────────┘
                       │
                       ↓
┌─────────────────────────────────────────────┐
│                   DJANGO                    │
│                                             │
│  Authentication • Trading • Portfolio      │
│  Market Logic • Orders • Transactions       │
└──────────────────────┬──────────────────────┘
                       │
             ┌─────────┴─────────┐
             ↓                   ↓
┌────────────────────┐  ┌────────────────────┐
│       MySQL        │  │      Pandas        │
│                    │  │                    │
│ Users              │  │ Market Data        │
│ Companies          │  │ Calculations       │
│ Holdings           │  │ Analysis            │
│ Orders             │  │                    │
│ Transactions       │  └────────────────────┘
└────────────────────┘
             │
             ↓
┌─────────────────────────────────────────────┐
│                 Matplotlib                  │
│        Charts • Price History • P/L         │
└─────────────────────────────────────────────┘
