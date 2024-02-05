# practice-question-on-classes-and-objects-in-Python
Of course! Here's a practice question on classes and objects in Python:

Practice Question:

You are tasked with implementing a simple banking system. Define a class `BankAccount` to represent a basic bank account.

The `BankAccount` class should have the following attributes and methods:
- Attributes:
  - `account_number` (string): representing the unique account number.
  - `balance` (float): representing the current balance of the account.
- Methods:
  - `__init__(self, account_number, initial_balance)`: constructor to initialize the attributes.
  - `deposit(self, amount)`: method to deposit a specified amount into the account.
  - `withdraw(self, amount)`: method to withdraw a specified amount from the account.
  - `display_balance(self)`: method to display the current balance of the account.

Create an instance of the `BankAccount` class, perform some deposit and withdrawal operations, and display the final balance.

Solution:

```python
class BankAccount:
    def __init__(self, account_number, initial_balance):
        self.account_number = account_number
        self.balance = initial_balance
    
    def deposit(self, amount):
        self.balance += amount
        print(f"Deposited {amount} into account {self.account_number}")
    
    def withdraw(self, amount):
        if amount <= self.balance:
            self.balance -= amount
            print(f"Withdrew {amount} from account {self.account_number}")
        else:
            print("Insufficient funds")
    
    def display_balance(self):
        print(f"Account {self.account_number} balance: {self.balance}")

# Create an instance of BankAccount
account1 = BankAccount("1234567890", 1000.0)

# Perform deposit and withdrawal operations
account1.deposit(500.0)
account1.withdraw(200.0)
account1.withdraw(1500.0)  # Attempting to withdraw more than balance

# Display final balance
account1.display_balance()
```

Explanation:

- The `BankAccount` class is defined with attributes `account_number` and `balance`, along with methods `deposit`, `withdraw`, and `display_balance`.
- The `__init__` method initializes the account number and initial balance when a `BankAccount` object is created.
- The `deposit` method adds the specified amount to the account balance.
- The `withdraw` method deducts the specified amount from the account balance if sufficient funds are available.
- The `display_balance` method prints the current balance of the account.
- An instance of the `BankAccount` class (`account1`) is created with an initial balance of 1000.0.
- Deposit and withdrawal operations are performed on `account1`, and the final balance is displayed.
