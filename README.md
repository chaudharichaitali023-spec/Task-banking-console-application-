# Task-banking-console-application-

balance = 10000

while True:
    print("\n--- Banking Menu ---")
    print("1. Check Balance")
    print("2. Deposit Money")
    print("3. Withdraw Money")
    print("4. Exit")

    choice = input("Enter your choice: ")

    if choice == "1":
        print("Balance: Rs.", balance)

    elif choice == "2":
        try:
            deposit = float(input("Enter deposit amount: "))
            if deposit > 0:
                balance += deposit
                print("Updated Balance: Rs.", balance)
            else:
                print("Invalid deposit amount!")
        except ValueError:
            print("Please enter a valid number!")

    elif choice == "3":
        try:
            withdraw = float(input("Enter withdrawal amount: "))
            if withdraw <= 0:
                print("Invalid withdrawal amount!")
            elif withdraw <= balance:
                balance -= withdraw
                print("Updated Balance: Rs.", balance)
            else:
                print("Insufficient balance!")
        except ValueError:
            print("Please enter a valid number!")

    elif choice == "4":
        print("Thank you for banking with us!")
        break

    else:
        print("Invalid choice! Try again.")
        
