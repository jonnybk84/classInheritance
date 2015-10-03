# classInheritance
#object orientated programming test

class Account:
   def __init__(self, accNumber, balance):
      self.accNumber = accNumber
      self.balance = balance

   def __str__(self):
      return "Account #: " + str(self.accNumber)
      return "Balance: " + str(self.balance)
      

class Checking(Account):
   def __init__(self, accNumber, balance, fee):
      Account.__init__(self, accNumber, balance)
      self.fee = fee

   def __str__(self):
      retStr = "Account type: Checking \n";
      retStr += Account.__str__(self) 
      return retStr

   def getFee (self):
      return self.fee

   def deposit (self, amount):
      self.balance += amount

ac1 = Checking("1234", 1000, .50)
print (ac1)
ac1.deposit(500)
print(ac1)

