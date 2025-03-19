# Banking Website

The **Banking Website** is a simple web application that allows users to perform basic banking operations such as balance checking, withdrawal, and money transfer. This project demonstrates how core web technologies like **HTML**, **CSS**, **JavaScript**, **PHP**, and **MySQL** can be used to create a functional banking system.

## Features:
- **Balance Check**: Users can log in and check their current account balance.
- **Withdrawal**: Allows users to withdraw a specified amount from their account.
- **Money Transfer**: Users can transfer money between accounts within the system.
- **Transaction History**: Displays a log of all transactions performed by the user.
- **User Authentication**: Simple login system for secure access.

## Technologies Used:
- **HTML**: For structuring the web pages.
- **CSS**: For styling and making the website responsive.
- **JavaScript**: For client-side interactivity.
- **PHP**: For server-side scripting and handling database operations.
- **MySQL**: For storing user data, account balances, and transaction history.

## Database Setup
Before running the website, you'll need to set up the MySQL database:

1. **Create the Database**  
   Open your MySQL client (e.g., phpMyAdmin, MySQL Workbench) and run the following SQL query to create the database:
   ```sql
   CREATE DATABASE banking_system;
   ```

2. **Create the Users Table**  
   Run the following SQL query to create a table for storing user account information:
   ```sql
   CREATE TABLE users (
       id INT AUTO_INCREMENT PRIMARY KEY,
       username VARCHAR(50) NOT NULL,
       password VARCHAR(100) NOT NULL,
       balance DECIMAL(10,2) DEFAULT 0.00
   );
   ```

3. **Create the Transactions Table**  
   Create a table for recording transaction history:
   ```sql
   CREATE TABLE transactions (
       id INT AUTO_INCREMENT PRIMARY KEY,
       user_id INT,
       type VARCHAR(50),
       amount DECIMAL(10,2),
       date TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
       FOREIGN KEY (user_id) REFERENCES users(id)
   );
   ```

4. **Insert Sample User Data (Optional)**  
   You can add a few users for testing purposes:
   ```sql
   INSERT INTO users (username, password, balance) VALUES
   ('user1', 'password1', 5000.00),
   ('user2', 'password2', 3000.00);
   ```

## Installation & Setup

Follow these steps to set up the project locally:

### 1. Clone the Repository
Open your terminal and clone the repository:
```bash
git clone https://github.com/111faizan/banking_website.git
```

### 2. Navigate to the Project Directory
```bash
cd banking-website
```

### 3. Set Up the Server
Make sure you have a local server running (e.g., **XAMPP**, **WAMP**, or **MAMP**). Place the project folder inside the server’s root directory (e.g., `htdocs` for XAMPP).

### 4. Configure the Database Connection
In the project folder, open the `config.php` file and configure the database connection:
```php
<?php
$host = 'localhost';
$dbname = 'banking_system';
$username = 'root';  // Use your MySQL username
$password = '';      // Use your MySQL password

try {
    $conn = new PDO("mysql:host=$host;dbname=$dbname", $username, $password);
    $conn->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
} catch (PDOException $e) {
    echo "Connection failed: " . $e->getMessage();
}
?>
```

### 5. Run the Website
1. Open your browser and go to `http://localhost/banking-website`.

## How to Use

- **Login**: Enter your username and password to access your account.
- **Check Balance**: Once logged in, the current balance will be displayed on the dashboard.
- **Withdraw Money**: Enter the amount you wish to withdraw and submit the form to update your balance.
- **Transfer Money**: Select a recipient and enter the amount to transfer funds between accounts.
- **View Transaction History**: You can view your past transactions under the transaction history section.

## File Structure

- `index.html`: The login page.
- `dashboard.php`: The main page where users can check their balance, withdraw money, and transfer funds.
- `withdraw.php`: The script handling withdrawal operations.
- `transfer.php`: The script handling money transfer.
- `transaction-history.php`: Displays the user's transaction history.
- `config.php`: The database connection file.

## Future Improvements
- Adding proper authentication (password hashing).
- Implementing a robust validation system for transactions.
- Adding email notifications for transactions.

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





