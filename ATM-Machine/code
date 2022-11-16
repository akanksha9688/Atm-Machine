import random
import sys 
import time as t

class ATM():
    def __init__(self, name, account_number, balance = 0,check_balance1=5000):
        self.name = name
        self.account_number = account_number
        self.balance = balance
     #account details    
    def account_detail(self):
        print("\n----------ACCOUNT DETAIL----------")
        print(f"Account Holder: {self.name.upper()}")
        print(f"Account Number: {self.account_number}")
        print(f"Available balance: Nu.{self.balance}\n")
     # To deposit money    
    def deposit(self, amount):
        self.amount = amount
        self.balance = self.balance + self.amount
        print("Current account balance: Nu.", self.balance)
        print()
 #Withdrawl
    def withdraw(self, amount):
        self.amount = amount
        #if withdrawl amount is more than balance
        if self.amount > self.balance:
           
            print("Insufficient fund!")
            print(f"Your balance is Nu.{self.balance} only.")
            print("Try with lesser amount than balance.")
            print()
        #amount to be withdrawn is less than equal to balance
        else:
            self.balance = self.balance - self.amount
            print(f"Nu.{amount} withdrawal successful!")
            print("Current account balance: Nu.", self.balance)
            print()
     #transfer funds from checking balance to saving account
    def transfer_funds(self,check_balance):
        self.check_balance1=5000
        self.check_balance=check_balance
        self.balance=self.balance+self.check_balance
        self.check_balance1=self.check_balance1-self.check_balance
        print(self.balance)
        print(self.check_balance1)


     #transaction Menu
    def transaction(self):      
        print("""
            TRANSACTION 
        *******
            Menu:
            1. Account Detail
            2. Deposit
            3. Withdraw
            4. Transfer Funds
        *******
        """)
        
        while True:
            try:
                option = int(input("Enter 1, 2, 3, 4 :"))
            except:
                print("Error: Enter 1, 2, 3, 4 only!\n")
                continue
            else:
                if option == 1:
                    atm.account_detail()
                elif option == 2:
                    amount = int(input("How much you want to deposit(Nu.):"))
                    atm.deposit(amount)
                elif option == 3:
                    amount = int(input("How much you want to withdraw(Nu.):"))
                    atm.withdraw(amount)
                elif option ==4:
                    check_balance=int(input("Amount to be addedL:"))
                    if (check_balance>5000):
                      print("Enter Amount below 5000")
                    else:
                      atm.transfer_funds(check_balance)
#Final calling
print("**WELCOME TO BANK OF PSIT**")
print("_____________________\n")
print("----------ACCOUNT CREATION----------")
name = input("Enter your name: ")
account_number = input("Enter your account number: ")
print("Congratulations! Account created successfully......\n")
 
atm =ATM(name, account_number)
while True:
  #enter pin
  n=int(input("Enter Pin:"))
  #reenter pin
  m=int(input("Re-Enter Pin:"))
  #checking pin if it is same 
  if n==m:
    #pin is same then ask if user want to do transaction
    trans = input("Do you want to do any transaction?(y/n):")
    if trans == "y":
      #if yes then move to transaction menu
        atm.transaction()
    elif trans == "n":
      #if no then print this
        print("Thanks for choosing us as your bank...Visit us again!")
        break
    else:
      #choice is wrong
        print("Wrong command!  Enter 'y' for yes and 'n' for NO.\n")
  else:
    #pin is not same
    print("Wrong Command!")
