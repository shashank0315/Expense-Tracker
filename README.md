# ExpenseOrbit

## Expense Tracker CLI App (with Budget Alerts, Reports & Group Sharing)

A simple command-line based Python app to help users track their daily expenses, categorize them, set monthly budgets, and receive alerts when approaching or exceeding budget limits. It also supports shared expenses within groups and generates budget vs spending reports. Data is stored using SQLite and SQLAlchemy.

---

## 📁 Project Structure

```
Expense Tracker/
├── README.md
├── main.py                # Entry point of the app
├── models.py              # ORM models for users, budgets, expenses
├── db.py                  # Database setup and config
├── expense.py             # Expense logic
├── budget.py              # Budget management and alerts
├── group.py               # Group expense sharing
├── report.py              # Reports generation
├── email_utils.py         # Email alerts
├── requirements.txt       # Dependencies
```

---

## ✅ Features Implemented

- Log daily expenses with category and description
- Set monthly budgets per category
- Alerts when 90% of budget is reached or budget is exceeded
- View total monthly spending
- Compare spending vs. budget with clear indicators
- Set custom budgets per month
- Email notifications for alerts (SMTP)
- Share expenses among users in a group (Splitwise-like)
- SQLite DB using SQLAlchemy ORM


---

## ⚙️ Setup & Run Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/shashank0315/Expense-Tracker.git
cd Expense-Tracker
```

### 2. Create a Virtual Environment (Recommended)

```bash
python -m venv venv
source venv/bin/activate        # On Linux/macOS
venv\Scripts\activate           # On Windows
```

### 3. Install the Dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the Application

```bash
python main.py
```

---

## 🧪 Test Steps

- ✅ Log an expense under "Food"
- ✅ Set budget for "Food" as ₹1000
- ✅ Log ₹950 → get a 90% alert
- ✅ Log ₹1100 → get a budget exceeded alert
- ✅ Create and view a monthly report
- ✅ Add group members and log a shared expense
- ✅ Configure email → receive alerts in mailbox

---

## 🧠 Edge Cases Handled

- Negative amount entries
- Missing or invalid category handling
- Setting different budgets for each month
- User not configured with email – app skips email gracefully
- Group member leaving before split is finalized

---

## 📊 Reports Example

**April 2025:**
| Category     | Budget (₹) | Spent (₹) | Status         |
|--------------|------------|-----------|----------------|
| Food         | 1000       | 1350      | ❌ Exceeded     |
| Transport    | 800        | 720       | ✅ Within Budget|
| Shopping     | 1200       | 1170      | ✅ Within Budget|

---

## 📬 Sample Email Alert

> **Subject**: ⚠️ Budget Alert: Food  
> Hi, you've spent ₹900 out of your ₹1000 budget for **Food**. Just 10% left!

---

## 🧾 SQL/ORM Implementation

- Built using SQLAlchemy ORM.
- Tables:
  - `User`
  - `Expense`
  - `Category`
  - `Budget`
  - `GroupExpense`
  - `GroupMembers`

---



---

## 📜 License

MIT License © 2025

---


