# CODSOFT
# simple calculator

print('''
      1.ADDITION (+)
      2.SUBTRACTION (-)
      3.MULTIPLICTION (x)
      4.DIVISION (/)
      5.MODULUS (%)
      6.POWER (^) '''
      )

num1 = int(input("Enter first number : "))
num2 = int(input("Enter second number: "))

ch = int(input("Enter choice :"))

match ch:
    case 1:
        print("Performing Addition")
        print(f"Result : {num1}+{num2} = ", num1 + num2)
    case 2:
        print("Performing Subtraction")
        print(f"Result : {num1}-{num2} = ", num1 - num2)
    case 3:
        print("Performing Multiplication")
        print(f"Result : {num1}*{num2} = ", num1 * num2)
    case 4:
        if num1 == num2 == 0:
            print("Can't divide by zero")
        else:
            print("Performing Division")
            print(f"Result : {num1}/{num2} = ", num1 / num2)
    case 5:
        print("Performing Modulus")
        print(f"Result : {num1}%{num2} is ", num1 % num2)
    case 6:
        print("Performing Power")
        print(f"Result :  {num1}**{num2} is ", num1 ** num2)
    case _:
        print("invalid choise")



