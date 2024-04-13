class ExpenseTracker:
    def __init__(self):
        self.expenses = {}

    def add_expense(self, category, amount):
        if category in self.expenses:
            self.expenses[category] += amount
        else:
            self.expenses[category] = amount

    def view_expenses(self):
        total = 0
        print("Expense Tracker:")
        print("----------------")
        for category, amount in self.expenses.items():
            print(f"{category}: ${amount}")
            total += amount
        print("----------------")
        print(f"Total: ${total}")


# Example Usage
tracker = ExpenseTracker()
tracker.add_expense("Food", 50)
tracker.add_expense("Transportation", 30)
tracker.add_expense("Food", 20)
tracker.add_expense("Entertainment", 100)

tracker.view_expenses()
