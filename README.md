# A-Bike-Rental-System
#A full fledged bike rental system implemented in Python using object oriented programming.
class bikerental():
  stock=100
  def __init__(self):
    print("Welocome to rental bike shop")
  def displaystock(self):
    print("Stock available in inventory ",self.stock)
bike_shop=bikerental()
bike_shop.displaystock()
class customer(bikerental):
  bill =0
  def __init__(self,number_of_bike,rentalbasis,number_of_days_or_weeks):
    self.nub=number_of_bike
    self.red=rentalbasis
    self.numb=number_of_days_or_weeks
  def rentbike(self):
    if self.nub <=0:
      print("Number of Bike should be Positive")
    elif self.nub > self.stock :
      print('Number of bikes available',self.stock)
    else :
      print("Number of bike you have rented",self.nub)
    stock=self.stock-self.nub

  def returnbike(self):
    if self.red=='day':
      if self.nub>=3 and self.nub<=5:
        d=(self.nub*100)*0.30
        self.bill=(self.nub*100)-d
        print("Your discounted price is",self.bill)
      else:
        self.bill=self.nub*100
        print("Your bill",self.bill)
    else:
      if self.nub>=3 and self.nub<=5:
        d=(self.nub*500)*0.30
        self.bill=(self.nub*500)-d
        print("Your discounted price is",self.bill)
      else:
        self.bill=self.nub*500
        print("Your bill",self.bill)

bike_shop=bikerental()
customer_1 = customer(2,'day',5)
customer_1.rentbike()
customer_1.returnbike()


