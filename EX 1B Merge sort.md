# EX 1B Merge Sort
## DATE:22.02.2025

## AIM:
To write a python program to sort the first half of the list using merge sort.

## Algorithm:
```
 1.Initialize an empty list arr
 2.Read an integer n (number of elements) from the user
 3.Repeat n times:
  • Read each integer and append it to the list arr
 4.Display the original array
 5.Define a function merge(arr, l, m, r) to merge two sorted halves:
    • Create two temporary arrays L and R for the left and right subarrays
    • Copy data into temporary arrays
    • Merge the two temporary arrays back into arr[l..r]
    • Copy any remaining elements of L[] and R[], if any
 6.Define a recursive function mergeSort(arr, l, r) to sort an array segment:
  • If l < r:
    – Find middle point m
    – Recursively call mergeSort(arr, l, m)
    – Recursively call mergeSort(arr, m+1, r)
    – Call merge(arr, l, m, r) to merge sorted parts
 7.Sort only the first half of the list:
  • Call mergeSort(arr, 0, (n//2) - 1)
 8.Display the modified array
  
```
## Program:
```
Program to implement Merge Sort
Developed by: SANTHOSH L
Register Number:  212222100046

def merge(arr, l, m, r):
    n1 = m - l + 1
    n2 = r - m
    L = [0] * (n1)
    R = [0] * (n2)
    for i in range(0, n1):
        L[i] = arr[l + i]
 
    for j in range(0, n2):
        R[j] = arr[m + 1 + j]
 

    i = 0     
    j = 0     
    k = l     
 
    while i < n1 and j < n2:
        if L[i] <= R[j]:
            arr[k] = L[i]
            i += 1
        else:
            arr[k] = R[j]
            j += 1
        k += 1
 
    # Copy the remaining elements of L[], if there
    # are any
    while i < n1:
        arr[k] = L[i]
        i += 1
        k += 1
 
    while j < n2:
        arr[k] = R[j]
        j += 1
        k += 1

def mergeSort(arr, l, r):
    if l < r:
        m = l+(r-l)//2
        mergeSort(arr, m+1, r)
        merge(arr, l, m, r)
 
 

arr =[]               #[12, 11, 13, 5, 6, 7]
n =int(input())
for i in range(n):
    arr.append(int(input()))
print("Given array is")
for i in range(n):
    print("%d" % arr[i],end=" ")
 
mergeSort(arr, 0, n-1)
print("\n\nSorted array is")
for i in range(n):
    print("%d" % arr[i],end=" ")
 
```
## Output:

![Screenshot 2025-04-29 110300](https://github.com/user-attachments/assets/75c8bd61-dc76-4d03-a607-82483fb2a918)

## Result:
The program successfully sorts the first half of the given array using merge sort. where only the first half is sorted, and the second half remains unchanged.
