def add(a, b):
    return a + b

def subtract(a, b):
    return a - b

def multiply(a, b):
    return a * b

def divide(a, b):
    return a / b

while True:
    print("\nSelect operation.")
    print("1.Add")
    print("2.Subtract")
    print("3.Multiply")
    print("4.Divide")

    choice = input("Enter choice(1/2/3/4): ")
    if choice not in ['1', '2', '3', '4']:
        print("Invalid Input")
        continue

    try:
        a = float(input("Enter first number: "))
        b = float(input("Enter second number: "))
    except ValueError:
        print("Invalid Input")
        continue

    if choice == '1':
        result = add(a, b)
        print(f"{a} + {b} = {result}")
    elif choice == '2':
        result = subtract(a, b)
        print(f"{a} - {b} = {result}")
    elif choice == '3':
        result = multiply(a, b)
        print(f"{a} * {b} = {result}")
    elif choice == '4':
        if b == 0:
            print("Cannot divide by zero.")
            continue
        result = divide(a, b)
        print(f"{a} / {b} = {result}")

    next_calc = input("Let's do next calculation? (yes/no): ").lower()
    if next_calc != 'yes':
        break
