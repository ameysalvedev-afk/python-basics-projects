# python-basics-projects
My first Python project! A simple Flask-based API that greets users and performs basic math operations. Perfect for learning how APIs work in Python.
A beginner-friendly calculator built using Python that performs basic arithmetic operations like addition, subtraction, multiplication, and division.
It runs in the terminal and provides clear, interactive prompts for users.


# 🧮 Simple Calculator in Python
# Author: amey
# Description: A basic calculator that performs addition, subtraction, multiplication, and division.

def add(a, b):
    return a + b

def subtract(a, b):
    return a - b

def multiply(a, b):
    return a * b

def divide(a, b):
    if b == 0:
        return "Error! Division by zero."
    else:
        return a / b

def calculator():
    print("Welcome to Simple Python Calculator!")
    print("Operations: +, -, *, /")

    while True:
        # Taking user input
        num1 = float(input("\nEnter first number: "))
        operator = input("Enter operator (+, -, *, /): ")
        num2 = float(input("Enter second number: "))

        # Perform calculation
        if operator == '+':
            result = add(num1, num2)
        elif operator == '-':
            result = subtract(num1, num2)
        elif operator == '*':
            result = multiply(num1, num2)
        elif operator == '/':
            result = divide(num1, num2)
        else:
            print("Invalid operator! Please try again.")
            continue

        print(f"Result: {result}")

        # Option to continue or exit
        choice = input("\nDo you want to calculate again? (yes/no): ").lower()
        if choice != 'yes':
            print("Thank you for using the calculator! Goodbye 👋")
            break

# Run the calculator
if __name__ == "__main__":
    calculator()
