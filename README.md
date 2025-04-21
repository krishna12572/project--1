balance = 0

while True:
    print("\n1. Add Income\n2. Add Expense\n3. Show Summary\n4. Reset Data\n5. Quit")
    choice = input("Choose an option: ")

    if choice == '1':
        income = float(input("Enter income amount: "))
        balance += income
        print(f"The total income is {balance}.")
    
    elif choice == '2':
        category = input("Enter expense category (food, rent, transport): ").lower()
        amount = float(input(f"Enter amount for {category}: "))
        balance -= amount
        print(f"Expense of {amount} added to {category}. The total balance is now {balance}.")
    
    elif choice == '3':
        print(f"The total balance is {balance}.")
    
    elif choice == '4':
        balance = 0
        print("Data has been reset. The total balance is now 0.")
    
    elif choice == '5':
        print("Goodbye!")
        break
    
    else:
        print("Invalid option, please try again.")
