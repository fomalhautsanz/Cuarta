# 📈 Cuarta — Stock Investment Simulator

> A virtual stock market simulator built with **Python, Django, and MySQL** to explore how investors, brokers, companies, and stock markets interact.

Cuarta is an educational stock investment simulator designed to recreate the basic experience of participating in a stock market without using real money.

Users receive virtual funds that they can use to buy and sell simulated company shares, manage their portfolio, monitor transactions, and observe how changes in stock prices affect their investments.

The project is primarily intended as a **learning project for programming, databases, investing concepts, and financial systems**.

---

## 🎯 Project Goals

Cuarta aims to help me understand both the **technical** and **financial** concepts behind stock investing.

### Programming Goals

- Practice Python and Django
- Build a database-driven web application
- Learn Django models, views, URLs, and templates
- Practice CRUD operations
- Implement authentication and authorization
- Learn database transactions
- Practice frontend and backend integration
- Build a simulated trading system
- Implement financial calculations
- Improve Git and GitHub workflow

### Financial Learning Goals

- Understand how stocks work
- Understand buying and selling shares
- Learn how portfolios are managed
- Understand market prices
- Learn about brokers and trading orders
- Understand profit and loss
- Explore how supply and demand can affect prices
- Experiment with investment strategies without risking real money

---

## 🏦 How the Simulator Works

The basic system models several participants in a simplified stock market:

```text
                    STOCK MARKET
                         │
          ┌──────────────┼──────────────┐
          ↓              ↓              ↓
      COMPANIES       BROKERS       INVESTORS
          │              │              │
     Issue Shares    Execute Orders   Buy / Sell
          │              │              │
          └──────────────┼──────────────┘
                         ↓
                  STOCK EXCHANGE
                         │
                         ↓
                    MARKET PRICE
