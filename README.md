# 💰 Cuarta: Personal Finance Management System

A web-based **personal financial management system** built with **Python, Django, and MySQL**. The system helps users plan, track, and analyze their finances using the **50/30/20 budgeting rule**, while providing tools for expense tracking, savings goals, budgeting, and financial analytics.

---

## 📌 Overview

Managing money can be difficult, especially when income or allowance needs to be divided among daily necessities, personal wants, and savings.

This system provides a centralized platform where users can:

* Set their total allowance or income
* Automatically allocate funds using the **50/30/20 rule**
* Record and categorize expenses
* Monitor remaining funds
* Track savings and financial goals
* Review spending history
* Analyze their financial habits
* Generate financial reports

The **50/30/20 rule** serves as the default budgeting framework:

| Category                 | Allocation |
| ------------------------ | ---------: |
| 🏠 Necessities           |        50% |
| 🎮 Wants                 |        30% |
| 💰 Savings / Investments |        20% |

The percentages can also be customized to accommodate different financial situations.

---

## 🎯 Project Goals

The system aims to provide a simple and practical way to:

1. **Plan finances** before spending.
2. **Track expenses** and understand where money goes.
3. **Monitor budgets** in real time.
4. **Encourage saving** through financial goals.
5. **Analyze spending habits** using historical data.
6. **Provide personalized financial information** through dashboards and reports.

---

## ✨ Features

### 📊 Dashboard

Provides an overview of the user's current financial situation, including:

* Total income or allowance
* Remaining balance
* Total expenses
* Budget allocation
* Category spending
* Recent transactions
* Savings progress

---

### 💵 Budget Management

Users can enter their total allowance or income and automatically divide it according to the 50/30/20 rule.

Example:

```text
Total Allowance: ₱10,000

Necessities:       ₱5,000
Wants:             ₱3,000
Savings:           ₱2,000
```

Users can also customize the allocation percentages when the default 50/30/20 distribution does not fit their situation.

---

### 💳 Expense Tracking

Users can record expenses and automatically update their available balance.

Each expense may contain:

* Amount
* Category
* Date
* Description
* Payment method
* Budget classification

Example:

```text
Food
₱150
Necessity
October 2, 2026
```

The system automatically deducts the expense from the user's total remaining balance and the corresponding budget category.

---

### 🏷️ Expense Categories

Expenses can be organized into categories and subcategories.

**Necessities**

* Food
* Transportation
* School
* Rent
* Utilities
* Health

**Wants**

* Entertainment
* Games
* Shopping
* Eating out
* Hobbies

**Savings / Investments**

* Emergency Fund
* Bank Savings
* Investments
* Other Financial Goals

Users may also create custom categories.

---

### 🎯 Savings Goals

Users can create specific savings goals and monitor their progress.

Example:

```text
Goal: New Laptop

Target:     ₱40,000
Current:    ₱12,500
Remaining:  ₱27,500

Progress: 31.25%
```

Possible goals include:

* Emergency fund
* Laptop
* Phone
* Tuition
* Travel
* Investment capital

---

### 📈 Financial Analytics

The system can analyze historical financial data and display information such as:

* Monthly spending
* Category distribution
* Savings progress
* Income vs. expenses
* Budget utilization
* Spending trends

Example:

```text
Target Allocation

Necessities     50%
Wants           30%
Savings         20%

Actual Spending

Necessities     47%
Wants           36%
Savings         17%
```

---

### 🔔 Budget Alerts

The system can notify users when they are approaching or exceeding their allocated budget.

Example:

> ⚠️ You have used 85% of your Wants budget.

> 🔴 Your Wants budget has been exceeded by ₱350.

> 🟢 You have reached 90% of your monthly savings goal.

---

### 📅 Financial Calendar

Users can view their income and expenses based on their transaction dates.

This allows users to understand **when** they tend to spend money and monitor upcoming recurring expenses.

---

### 🔄 Recurring Expenses

Users can record recurring expenses such as:

* Monthly subscriptions
* Internet bills
* Rent
* Transportation
* Regular school expenses

This allows the system to account for predictable expenses when planning a budget.

---

### 📄 Financial Reports

Users can generate summaries of their financial activity.

Reports may include:

* Total income
* Total expenses
* Total savings
* Category breakdown
* Monthly spending
* Budget performance

Future versions may support **PDF and CSV exports**.

---

### 🧮 What-If Budget Simulator

Users can experiment with different financial scenarios without changing their actual budget.

For example:

```text
Current Allowance: ₱10,000

What if allowance becomes ₱15,000?

Necessities: ₱7,500
Wants:       ₱4,500
Savings:     ₱3,000
```

This can help users understand how changes in income or spending affect their overall budget.

---

## 🛠️ Technology Stack

### Backend

* **Python**
* **Django**

### Database

* **MySQL**
* **MySQL Workbench**

### Frontend

* HTML
* CSS
* JavaScript

### Development Tools

* Git
* GitHub
* Visual Studio Code

---

## 🗄️ Basic Data Structure

The application will organize financial information around individual users.

```text
User
│
├── Income
│
├── Budget
│   ├── Budget Allocation
│   └── Budget Categories
│
├── Expenses
│   └── Categories
│
├── Savings Goals
│
└── Recurring Expenses
```

Each user's financial records are associated with their account to ensure that users only access their own financial information.

---

## 🔐 Security

Because the system handles financial information, security is an important consideration.

The application will use Django's built-in security mechanisms and authentication system.

Planned security considerations include:

* User authentication
* Password hashing
* User-specific data access
* CSRF protection
* Input validation
* Secure database configuration
* Environment variables for sensitive credentials
* HTTPS in production

**No real financial transactions or bank account access are performed by this system.**

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/your-username/your-repository.git
cd your-repository
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure MySQL

Create a database in MySQL:

```sql
CREATE DATABASE finance_manager;
```

Configure the database credentials in Django's settings.

Example:

```python
DATABASES = {
    "default": {
        "ENGINE": "django.db.backends.mysql",
        "NAME": "finance_manager",
        "USER": "root",
        "PASSWORD": "your_password",
        "HOST": "localhost",
        "PORT": "3306",
    }
}
```

### 5. Run migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

### 6. Create a superuser

```bash
python manage.py createsuperuser
```

### 7. Start the development server

```bash
python manage.py runserver
```

The application will be available at:

```text
http://127.0.0.1:8000/
```

---

## 📁 Planned Project Structure

```text
finance-management-system/
│
├── manage.py
│
├── config/
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py
│   └── wsgi.py
│
├── accounts/
│   ├── models.py
│   ├── views.py
│   ├── urls.py
│   └── ...
│
├── budgeting/
│   ├── models.py
│   ├── views.py
│   ├── urls.py
│   └── ...
│
├── expenses/
│   ├── models.py
│   ├── views.py
│   ├── urls.py
│   └── ...
│
├── savings/
│   ├── models.py
│   ├── views.py
│   ├── urls.py
│   └── ...
│
├── templates/
│
├── static/
│
├── requirements.txt
├── .gitignore
└── README.md
```

The exact structure may change as development progresses.

---

## 🗺️ Development Roadmap

### Phase 1 — Foundation

* [ ] Create Django project
* [ ] Configure MySQL
* [ ] Set up authentication
* [ ] Create base UI
* [ ] Create navigation

### Phase 2 — Budgeting

* [ ] Allowance/income input
* [ ] 50/30/20 calculation
* [ ] Budget allocation
* [ ] Custom allocation percentages
* [ ] Budget dashboard

### Phase 3 — Expense Tracking

* [ ] Add expenses
* [ ] Expense categories
* [ ] Automatic balance deduction
* [ ] Transaction history
* [ ] Search and filtering

### Phase 4 — Savings

* [ ] Savings goals
* [ ] Savings progress
* [ ] Savings transactions
* [ ] Goal tracking

### Phase 5 — Analytics

* [ ] Spending charts
* [ ] Monthly comparisons
* [ ] Category analysis
* [ ] Budget utilization
* [ ] Financial trends

### Phase 6 — Advanced Features

* [ ] Recurring expenses
* [ ] Budget alerts
* [ ] Financial calendar
* [ ] What-if budget simulator
* [ ] PDF reports
* [ ] CSV export

### Phase 7 — Deployment

* [ ] Production configuration
* [ ] Environment variables
* [ ] Database deployment
* [ ] Static file configuration
* [ ] HTTPS
* [ ] Deploy application

---

## 🌐 Deployment

The application is intended to be deployable using a free or low-cost hosting platform.

Possible deployment architecture:

```text
GitHub
   │
   ▼
Hosting Platform
   │
   ▼
Django Application
   │
   ▼
Production Database
```

The final hosting provider and production database will be selected based on available free-tier resources and Django compatibility.

---

## ⚠️ Disclaimer

This application is intended for **personal financial planning and educational purposes**.

It does not:

* Connect directly to bank accounts
* Process real financial transactions
* Provide financial advice
* Guarantee financial outcomes

All financial decisions remain the responsibility of the user.

---

## 📌 Project Status

🚧 **Currently in Development**

The system is being developed as a personal financial management project using Django, Python, and MySQL.

---

## 📜 License

This project is currently intended for personal and educational use.

A formal open-source license may be added in the future.
