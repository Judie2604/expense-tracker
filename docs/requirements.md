# Expense Tracker — Requirements

## 1. Project Overview
A personal Expense Tracker application for recording transactions and monitoring account balances and spending.

## 2. Version 1 Scope
Version 1 will focus on two features:
- Home
- Tracker Tables

The application will initially be developed for a single user.

## 3. Home

### 3.1 New Transaction
The user can enter:
- Transaction name
- Amount
- Transaction type: Credit or Debit
- Account

Rules:
- Credit adds money to the selected account.
- Debit subtracts money from the selected account.
- A transaction cannot be created if no account exists.
- The transaction date is automatically taken from the system date.

### 3.2 Total Amount Spent
Display total debit transactions across all accounts.

The user can select a period using a dropdown:
- Today (default)
- Weekly
- Monthly
- Yearly

The displayed amount updates according to the selected period.

### 3.3 Total Money Present
Display the combined current balance across all accounts.

## 4. Tracker Tables

### 4.1 Create Account
When no accounts exist, prominently display an **Add Account** button in the centre of the page.

The form contains:
- Account name
- Starting balance
- Save
- Cancel

After an account is created, its transaction table is displayed.

### 4.2 Transaction Table
Each account's table contains:

| Column | Description |
|---|---|
| Date | Automatically recorded transaction date |
| Transaction Name | Name supplied when creating the transaction |
| Amount | Credit displayed as positive; debit displayed as negative |
| Balance | Account balance after the transaction |

Display the account's current balance at the top of its Tracker Tables view.

## 5. Balance Rules
- Credits increase the account balance.
- Debits decrease the account balance.
- Each transaction records the resulting account balance for display in the transaction history.
- Dashboard total balance represents the combined current balances of all accounts.
- Spending totals include debit transactions only.

## 6. Development Approach
1. Finalize the requirements and architecture.
2. Design the database and relationships.
3. Build the backend using Java, Spring Boot, Maven, SQL, and MyBatis/XML.
4. Create and test APIs using Postman.
5. Build the frontend using React.
6. Test the complete application.

## 7. Out of Scope for Now
- Multiple tracker tables and their detailed behaviour
- Additional features not listed in Version 1

These requirements may be updated when new decisions are agreed upon.
