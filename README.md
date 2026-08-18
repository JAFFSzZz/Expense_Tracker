# Expense_Tracker
you can track all your expenses !
<b\>
expense_dict = []
print("Welcome to your Expense Tracker!")

while True:
    print("\n*---Menu---*")
    print("1. Add expense")
    print("2. view all expense")
    print("3. view total expense")
    print("4. Exit!")

    ch = int(input("Enter your choice:"))

    if(ch == 1):
        date = input("Enter the date of your expense:")
        thing = input("Enter what item you have purchased in your expense:")
        amt = float(input("Enter the amount of the expense:"))

        all = {
            "date" : date,
            "thing" : thing,
            "amt": amt
        }

        expense_dict.append(all)
        print("Expense added successfully!")

    elif (ch == 2):
        if(len(expense_dict) == 0):
            print("there's no expenses added yet ! , please add expense first.")
        else:
            print(" \n*----your expenses ----*")
            count =1 
            for i in expense_dict:
                print (f"{count} -> {i["date"]} , {i["thing"]} , {i["amt"]}")
                count = count + 1 

    elif ( ch == 3):
        total = 0 
        for see in expense_dict:
            total = total + see["amt"]
        print("\n total amt = ",total)         

    elif ( ch == 4):
        print("Thank you !")
        print("Exiting!")
        break
    else:
        print("invaid choice!")
        break