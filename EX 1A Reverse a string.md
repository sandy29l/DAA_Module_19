# EX 1A Reverse a String
## DATE:18.02.2025
## AIM:
To write a program to create a recursive function to reverse a string.

## Algorithm
```
1. Define a function reverse(reverseme)
2. If the length of reverseme is 0, then return reverseme (base case)
  • Else, return reverse(reverseme[1:]) + reverseme[0] (recursive case)
3. Read a string input from the user and store it in the variable reverseme
4. Call the function reverse(reverseme) and print the result
5. Stop  
```
## Program:
```
Program to implement Reverse a String
Developed by: SANTHOSH L
Register Number:  212222100046

def reverse(reverseme):
    if len(reverseme)==0:
        return reverseme
    else:
        return reverse(reverseme[1:])+reverseme[0]
reverseme=input()
print(reverse(reverseme))

```

## Output:

![Screenshot 2025-04-29 111207](https://github.com/user-attachments/assets/b5812454-1f4d-47fa-a5d1-80c8601f4c98)


## Result:
The program successfully reverses the input string using recursion. When the user provides an input string, the output displays the reversed version of the string
