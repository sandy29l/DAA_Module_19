# EX 1D Linear search
## DATE:01.03.2025
## AIM:
To write a python program for a search function with parameter list name and the value to be searched using string values.

## Algorithm
```
1.Define a function search(List, n)
  • For each element in List:
    – If the current element is equal to n, return True
  • If no match is found after the loop, return False
2.Initialize an empty list List
3.Read an integer x from the user (number of elements in the list)
4.Repeat x times:
  • Read a string from the user and append it to List
5.Read the string n to be searched from the user
6.Call the search(List, n) function
  • If it returns True, print "Found"
  • Else, print "Not Found" 
```
## Program:
```

Program to implement a search function with parameter list name and the value to be searched using string values.
Developed by: SANTHOSH L
Register Number:  212222100046

def search(List,n):
    for i in range(len(List)):
        if(List[i]==n):
            return True
    return False

List=[]
x=int(input())
for i in range(x):
    List.append(input())

n=input()

if search(List,n):
    print("Found")
else:
    print("Not Found")
```

## Output:

![Screenshot 2025-04-29 112017](https://github.com/user-attachments/assets/352869b4-1700-4ce0-8664-b04ac343c5d2)


## Result:
The program was executed successfully, and it correctly checks if the input element is present in the list, printing "Found" if the element exists or "Not Found" if it does not.
