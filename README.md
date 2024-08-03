class BankAccount:
    def __init__(self, accountNumber, name, balance):
        self.accountNumber = accountNumber
        self.name = name
        self.balance = balance

    def deposit(self, amount):
        if amount > 0:
            self.balance += amount
            print(f"Deposited ${amount}. New balance: ${self.balance}")
        else:
            print("Amount must be greater than 0.")

    def withdrawal(self, amount):
        if 0 < amount <= self.balance:
            self.balance -= amount
            print(f"Withdrew ${amount}. New balance: ${self.balance}")
        else:
            print("Invalid amount or insufficient balance.")

    def bankFees(self):
        fee = self.balance * 0.05
        self.balance -= fee
        print(f"Bank fees (5%): ${fee}. New balance: ${self.balance}")

    def display(self):
        print(f"Account Number: {self.accountNumber}")
        print(f"Account Holder Name: {self.name}")
        print(f"Balance: ${self.balance}")


# Example usage:
account = BankAccount("1234567890123", "John Doe", 1000)
account.deposit(500)
account.withdrawal(200)
account.bankFees()
account.display()

# Create a Python class called BankAccount which represents a bank account, having as 
# attributes: accountNumber (numeric type), name (name of the account owner as string 
# type), balance.
# Create a constructor with parameters: accountNumber, name, balance.
# Create a Deposit() method which manages the deposit actions.
# Create a Withdrawal() method which manages withdrawals actions.
# Create an bankFees() method to apply the bank fees with a percentage of 5% of the 
# balance account.
# Create a display() method to display account details.
# Give the complete code for the BankAccount class.
# Create a validation for Account number input (Should be equal to 13 length and integer 
# only) Use while loop. Deposit,withdrawal,bankfees inputs should be integer
class bankAccount:
    def _init_(self):
        self.balance=0
        
        print("hello!!! welcome to the deposit and withdrawal machine")
    def accountnumber(self):
        accountnumber=input("enter your account number")
        while not accountnumber.isdigit():
            print("invalid number")
            accountnumber=input("please, enter your account number")
            if not len(accountnumber)==13:
                print("invalid number")
                accountnumber=("enter your account number")
    def name(self):
        name=input("enter your name ")
        while not name.isalpha():
            print("invalid name")
            name=input("enter your name ")
            print(name)
            
            name=input("enter your name").lower()
            print("your name is :" + name)
            
    def deposit(self):
        amount=float(input("enter amount to be deposited: "))
        self.balance += amount
        print("\n amount deposited:",amount)
        
    def withdrawal(self):
        amount= float(input("enter amount to be withdrawn: "))
        if self.balance>=amount:
            self.balance-=amount
            print("\n you withdrewn:", amount)
        else:
            print("\n insufficient balance ")
            
    def display(self):
        print("\n net available balance=",self.balance-5*self.balance/100)
        
        
s= bankAccount()
s.name()
s.accountnumber()
s.deposit()
s.withdrawal()
s.display()
