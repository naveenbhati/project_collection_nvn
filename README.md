# project_collection_nvn
First repository 

# factorial finder
"""Using a loop"""
n=input("please enter a number")
try:
   val = int(n)
   for k in range(1,val):
     val=val*k
   print(f"the factorial of n is {val}")

except ValueError:
   print("That's not an int!")

""" using recursion"""

def facto(n):
  if n>1:
    return facto(n-1)*n
  else:
    return 1

k=input("please enter a new number")
try:
   val = int(k)
   val = facto(val)
   print(f"the factorial of n is {val}")

except ValueError:
   print("That's not an int!")
   
   
   
   
   
# Sieve of Eratosthenes

numb = input("Enter the number upto which prime number to be found")
check=[]
try:
  val= int(numb)
  for k in range(2,val+1):
    check.append("true")

  for k in range(2,int(pow(val,0.5))+1):
    if check[k-2] =="true":
      for m in range(k*k,val+1,k):
        check[m-2]="false"

  print("the list ofall prime number upto k is")
  for k in range(2,val+1):
    if check[k-2] =="true":
     print(k)

except(ValueError):
  print("Enter a valid number")
