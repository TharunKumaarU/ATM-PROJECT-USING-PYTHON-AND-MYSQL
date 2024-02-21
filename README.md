# ATM-PROJECT-USING-PYTHON-AND-MYSQL

Here is my first Python project with MySQL, which serves as a sample program demonstrating the functionality of an advanced ATM machine. This program stores and retrieves customer data.

## What we have done using MySQL:

We have created a database named "atm" that includes two tables: "account" and "customer."

The "account" table contains the following fields: CID, ACCOUNT_NO, ACCOUNT_TYPE, AMOUNT, PIN.  
The "customer" table contains the following fields: CID, CNAME, ADDRESS, PHONE.  
In both tables, CID is used as both the primary key and foreign key.

## What we have done with Python:

Initially, we established a connection between Python and MySQL using the following code:

```python
myConnection = mysql.connector.connect(host="localhost", user="userName", passwd="password", database='atm', auth_plugin='mysql_native_password')
```

Subsequently, we created various user-defined functions, including:

- `newCustomer()`
- `displayAllCustomer()`
- `searchCustomer()`
- `newAccount()`
- `displayAllAccounts()`
- `searchAccount()`
- `withdrawAmount()`

Each of these functions contains code to perform their designated tasks.




## overall description 

1. Importing Required Module:
   - The code starts by importing the `mysql.connector` module for MySQL database connectivity.

2. Global Variables:
   - Global variables like `myConnection`, `cursor`, `password`, and `cid` are declared for use throughout the code.

3. MySQL Connection Check Function:
   - `MYSQLconnectionCheck` function is defined to check and establish a connection to the MySQL database. It takes the username and password as input, connects to the 'atm' database on the localhost, and returns the connection if successful.

4. New Customer Function:
   - The `newCustomer` function is defined to create a new customer entry in the 'CUSTOMER' table. It takes input for customer details, creates the 'CUSTOMER' table if not exists, and inserts the customer information.

5. Display All Customer Function:
   - The `displayAllCustomer` function retrieves and prints all records from the 'CUSTOMER' table.

6. Search Customer Function:
   - The `searchCustomer` function searches for a specific customer in the 'CUSTOMER' table based on the provided customer ID.

7. New Account Function:
   - The `newAccount` function allows the user to open a new bank account. It checks if the customer exists, creates the 'ACCOUNT' table if not exists, and inserts account information.

8. Display All Accounts Function:
   - The `displayAllAccounts` function retrieves and prints all records from the 'ACCOUNT' table.

9. Search Account Function:
   - The `searchAccount` function searches for a specific account in the 'ACCOUNT' table based on the provided customer ID and account number.

10. Withdraw Amount Function:
    - The `withdrawAmount` function allows the user to withdraw an amount from their account after verifying the ATM PIN. It includes a PIN validation mechanism with a limited number of attempts.

11. Help Function:
    - The `helpMe` function prints a message directing the user to visit the branch for a manual.

12. Main Program:
    - The main program starts by printing information about the ATM project and its designer.
    - It then checks and establishes a connection to the MySQL database using the `MYSQLconnectionCheck` function.
    - Inside a while loop, the user is presented with a menu of options:
        - New User Registration
        - Display All Customers
        - Search Customer
        - Open New Account
        - Display All Accounts
        - Search Account
        - Withdraw Amount
        - Exit
        - Help
    - The user is prompted to enter their choice, and the corresponding function is called based on the input.
    - The loop continues until the user chooses to exit.

13.  End of Project:
    - The code includes a closing message thanking the user.

Please note that there are a few typographical errors in the code, such as `myConnnection` should be corrected to `myConnection` for consistency. Additionally, the indentation in the last else statement might need adjustment for proper execution flow.
