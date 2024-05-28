# banking_website
banking website built with HTML, CSS, PHP, JavaScript, and a MySQL database. It allows users to view their account balance and make basic transactions.

Components:

Frontend (HTML, CSS, JavaScript):

Login page for user authentication.
Dashboard displaying current account balance.
Transaction form for depositing or withdrawing funds.
JavaScript might handle basic form validation and user interactions.
Backend (PHP):

Connects to the MySQL database to verify user login credentials.
Retrieves account balance information based on the logged-in user.
Processes transaction requests (deposit or withdrawal) and updates the balance in the database.
Sends error messages or confirmation messages back to the frontend.
Database (MySQL):

Stores user accounts with login information (username, password) and a balance field.
Stores transaction history with details like date, amount, and type (deposit/withdrawal).
Workflow:

User logs in with username and password.
PHP script validates credentials against the database.
Upon successful login, the user is directed to the dashboard.
The dashboard displays the current balance retrieved from the database for the specific user.
User enters an amount and selects deposit or withdrawal in the transaction form.
PHP script processes the transaction:
Deposits: Adds the entered amount to the user's balance.
Withdrawals: Subtracts the entered amount from the user's balance (with proper checks to prevent negative balances).
The script updates the user's balance in the database.
The user receives a confirmation or error message based on the transaction status.
Security Considerations:

This is a basic example and doesn't include crucial security features like secure password hashing and data encryption.
Implementing proper security measures is essential for any real-world banking application.
Further Enhancements:

Transaction history showing past deposits and withdrawals.
Transferring funds between accounts (requires additional functionalities).

home page
![p1](https://github.com/111faizan/banking_website/assets/95275307/d7cbcdf5-a97f-4011-a148-bfa772ae79eb)
![p2](https://github.com/111faizan/banking_website/assets/95275307/88bad81a-9a3e-4234-bd16-0156ffbb2ca7)

![p3](https://github.com/111faizan/banking_website/assets/95275307/7413f056-3800-4677-a279-2ed671c323ef)
![p4](https://github.com/111faizan/banking_website/assets/95275307/66d7c5d6-dab8-4e8f-8bab-c3f487a39f62)
login page
![loginpage](https://github.com/111faizan/banking_website/assets/95275307/7722b4a2-f128-433a-8bbf-b9246e744885)

dashboard

![dashboard](https://github.com/111faizan/banking_website/assets/95275307/809d5cd6-5fbf-40d5-afdc-9c6bd84552c7)

analytics
![analytics](https://github.com/111faizan/banking_website/assets/95275307/e108ef4c-807c-4ba2-9a9e-0f50c408e1c7)





