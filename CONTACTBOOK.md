dict={}

def display():
    print("{Name : [Phone number, Email, Address]}")
    for i in dict:
        print(i,":",dict[i])

def add_details():
  c=[]

  num = int(input("Enter number of details you want to enter: "))
  for i in range(num):
    name = input("Enter name: ")
    phn = input("Enter phone number: ")
    c.append(phn)
    email = input("Enter email: ")
    c.append(email)
    address = input("Enter address: ")
    c.append(address)
    dict[name] = c
    c = []
    print("\n")

def search_Name():
  n1=input("Enter name to be searched :")
  if n1 in dict:
    print(dict[n1])
  else:
    print("No Such Contact Exist")
  print("\n")

def update():
  n2=input("Enter name of the person whose details has to be updated :")
  if n2 in dict:
    print('''
    1. Change phone number
    2. Change email
    3.change address''')
    ch=int(input("Enter your choice :"))
    x=dict[n2]
    match ch:
      case 1:
        x[0]=int(input("Enter new number: "))
      case 2:
        x[1]=input("Enter new email: ")
      case 3:
        x[2]=input("Enter new address: ")
    print("\n")
  else:
    print("No such contact exist\n")
  print(dict[n2])

def delete():
  n3=input("Enter name of the person you want to remove: ")
  if n3 in dict:
    del dict[n3]
    display()
  else:
    print('No such contact exist')
  print("\n")
def Option():
  print('''
  1.ADD DETAILS
  2.DISPLAY
  3.UPDATE DETAILS
  4.SEARCH NAME
  5.DELETE DETAILS''')
  c = int(input("Enter your choice: "))
  match c:
    case 1:
      add_details()
    case 2:
      display()
    case 3:
      update()
    case 4:
      search_Name()
    case 5:
      delete()

  print("Go to option :")
  C = input("ENTER YES(Y) OR NO(N) ")
  if C == "Y":
    Option()
  else:
    pass

Option()
