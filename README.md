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
