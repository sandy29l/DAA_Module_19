# EX 1C Quick Sort
## DATE:25.02.2025
## AIM:
To write a python program to implement quick sort using tha last element as pivot on the list of float values.

## Algorithm:
```
1.Initialize an empty list arr
2. Read an integer n from the user (number of float elements)
3.Repeat n times:
  • Read a float value from the user and append it to arr
4.Define the function partition(arr, low, high)
  • Set pivot = arr[high] (choose last element as pivot)
  • Initialize index i = low - 1
  • For each j from low to high - 1:
    – If arr[j] <= pivot:
      • Increment i
      • Swap arr[i] and arr[j]
  • After loop, swap arr[i+1] and arr[high]
  • Return i + 1 as partition index
5.Define the recursive function quickSort(arr, low, high)
  • If low < high:
    – Call partition() to get the partition index pi
    – Recursively call quickSort(arr, low, pi - 1)
    – Recursively call quickSort(arr, pi + 1, high)
6.Call quickSort(arr, 0, n - 1)
7.Print the sorted array 
```

## Program:
```

Program to implement implement quick sort using the last element as pivot on the list of float values.
Developed by: SANTHOSH L
Register Number:  212222100046


def partition(arr, low, high):
    i = (low-1)
    pivot = arr[high]

    for j in range(low, high):
        if arr[j] <= pivot:
            i = i+1
            arr[i], arr[j] = arr[j], arr[i]

    arr[i+1], arr[high] = arr[high], arr[i+1]
    return (i+1)

def quickSort(arr, low, high):
    if len(arr) == 1:
        return arr
    if low < high:
        pi = partition(arr, low, high)
        quickSort(arr, low, pi-1)
        quickSort(arr, pi+1, high)

arr = []
n = int(input())
for i in range (n):
    arr.append(float(input()))
#print("Original array is:")
#for i in arr:
#    print(i)
quickSort(arr, 0, n-1)
print("Sorted array is:")
for i in arr:
    print(i)
 

```

## Output:

![Screenshot 2025-04-29 111628](https://github.com/user-attachments/assets/0af2738d-f7e3-45f6-8323-022867f30cf0)


## Result:
The program successfully sorts the input array using the QuickSort algorithm, arranging the elements in ascending order.
