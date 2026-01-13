# username.github.io
saldo = 0
transaksi = []

while True:
    print("\n=== OSiS CASH MENU ===")
    print("1. Add Income")
    print("2. Add Expense")
    print("3. Show Transactions")
    print("4. Show Balance")
    print("5. Exit")

    pilihan = input("Choose menu (1-5): ")

    if pilihan == "1":
        nama = input("Student name: ")
        jumlah = int(input("Amount: "))
        saldo += jumlah
        transaksi.append(f"Income - {nama} : +{jumlah}")
        print("Income added.")

    elif pilihan == "2":
        keterangan = input("Expense description: ")
        jumlah = int(input("Amount: "))
        saldo -= jumlah
        transaksi.append(f"Expense - {keterangan} : -{jumlah}")
        print("Expense added.")

    elif pilihan == "3":
        print("\n--- Transaction List ---")
        if not transaksi:
            print("No transactions yet.")
        else:
            for i, t in enumerate(transaksi, start=1):
                print(f"{i}. {t}")

    elif pilihan == "4":
        print(f"\nCurrent Balance: {saldo}")

    elif pilihan == "5":
        print("Program finished.")
        break

    else:
        print("Invalid choice!")
