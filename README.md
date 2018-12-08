# Effective-Tax-Rate-Calc

#This is a calculator to determine your effective tax rate currently just for federal taxes. I am going to add state taxes as well. 

my_income = int(input("What is your income? "))
my_state = input("What state do you live in? (Use 2 Digit State Code): ")
marital_status = input("Are you married, filing jointly? Y/N: ")


if marital_status == "N":
    if my_income <= 9525:
        my_fed_tax = my_income*.1
    elif 9525 < my_income <= 38700:
        my_fed_tax = (((my_income - 9525)*.12)+ 952.50)
    elif 38700 < my_income <= 82500:
        my_fed_tax = (((my_income - 38700)*.22)+ 4453.50)
    elif 82500 < my_income <= 157500:
        my_fed_tax = (((my_income - 82500)* .24)+ 14089.50)
    elif 157500 <my_income <= 200000:
        my_fed_tax = (((my_income - 157500)*.32)+ 32089.50)
    elif 200000 < my_income <= 500000:
        my_fed_tax = (((my_income - 200000)*.35)+ 45689.50)
    elif my_income > 500000:
        my_fed_tax = (((my_income - 500000)*.37)+ 150689.50)
        
if marital_status == "Y":          
    if my_income <= 19050:
        my_fed_tax = my_income*.1
    elif 19050 < my_income <= 77400:
        my_fed_tax = (((my_income - 19050)*.12) + 1905)
    elif 77400 < my_income <= 165000:
        my_fed_tax = (((my_income - 77400)*.22) + 8907)
    elif 165000 < my_income <= 315000:
        my_fed_tax = (((my_income - 165000)*.24) + 28179)
    elif 315000 < my_income <= 400000:
        my_fed_tax = (((my_income - 315000)*.32) + 64179)
    elif 400000 < my_income <= 600000:
        my_fed_tax = (((my_income - 400000)*.35) + 91379)
    elif my_income < 600000:
        my_fed_tax = (((my_income - 600000)*.37) + 161379)
        
fed_tax_rate = my_fed_tax/my_income

print("Your Federal Effective Tax Rate Is " + "{:.2%}".format(fed_tax_rate));
