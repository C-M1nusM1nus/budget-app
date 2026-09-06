# Budget App
A simple Python budgeting application that allows you to create spending categories, manage deposits and withdrawals, transfer money between categories, and generate a visual spending chart.

# Features
* Create budget categories.
* Deposit money into a category.
* Withdraw money when sufficient funds are available.
* Check the current balance.
* Transfer money between categories.
* View a formatted ledger for each category.
* Generate a spending chart showing spending percentages by category.

# Category Class
The Category class represents a budget category and keeps track of its transactions.

## \_\_init__(name)
Creates a new category with a name and an empty ledger.

food = Category("Food")

## deposit(amount, description="")
Adds money to the category.

food.deposit(1000, "Paycheck")

## withdraw(amount, description="")
Removes money from the category if there are enough available funds.

food.withdraw(50, "Groceries")

The function returns:
* **True** if the withdrawal was successful.
* **False** if there were not enough funds.

## get_balance()
Returns the current balance of the category.

balance = food.get_balance()

## transfer(amount, category)
Transfers money from one category to another if sufficient funds are available.

food.transfer(100, clothing)

The transfer creates a withdrawal in the first category and a deposit in the second category.

## check_funds(amount)
Checks whether the category has enough money for a withdrawal or transfer.

food.check_funds(50)

Returns **True** if sufficient funds are available and **False** otherwise.

## \_\_str__()
Returns a formatted representation of the category's ledger.

Example:

\*\*\*\*\*\*\*\*\*\*\*\*\*Food*************

Paycheck              1000.00

Groceries               -50.00

Total: 950.00

## create_spend_chart(categories)
Creates a vertical spending chart showing how much each category contributed to total spending.

Only withdrawals are counted as spending.

# Requirements
Python 3.x
No external libraries are required.
