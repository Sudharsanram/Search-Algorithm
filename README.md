# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```
''' 
Program for linear search method to match the item in a list
Developed by: SUDHARSAN RAM M
RegisterNumber: 212222110048
'''
def linearSearch(array,n,k):
    for i in range(0,n):
        if(array[i]==k):
            return i
    return -1
array = eval(input())
# sort the array
n=len(array)
array.sort()
k = eval(input()) # k-item to be seared for
# get the length of array and store in the variable n
result = linearSearch(array,n,k) # use the function for linear search
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result
if result==-1:
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
    



```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: SUDHARSAN RAM M
RegisterNumber: 212222110048
'''
def binarySearchIter(array, k, low, high):
    if high>=low:
        mid=low+(high-low)//2
        if arr[mid]==k:
            return mid
        elif arr[mid]>k:
            return binarySearchIter(arr,k,low,mid-1)
        else:
            return binarySearchIter(arr,k,mid+1,high)
    else:
        return -1
arr = eval(input())
arr.sort()
# sort the array
k = eval(input()) #k-item to be searched
result = binarySearchIter(arr,k,0,len(arr)-1)
if result ==-1:
    print(arr)
    print("Element not found")
else:
    print(arr)
    print("Element found at index: ",result)




```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: SUDHARSAN RAM M
RegisterNumber: 212222110048
'''
def BinarySearch(arr, k, low, high):
    while low<=high:
        mid=low+(high-low)//2
        if arr[mid]==k:
            return mid
        elif arr[mid]<k:
            low=mid+1
        else:
            high=mid-1
    return -1
    
arr = eval(input())
arr.sort()
k = eval(input()) # k is the element to be searched for
result= BinarySearch(arr, k,0,len(arr)-1)
# use the binary search function to find the result
if result ==-1:
    print(arr)
    print("Element not found")
else:
    print(arr)
    print("Element found at index: ",result)

# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result

```
## Sample Input and Output

i)	#Use a linear search method to match the item in a list.
![image](https://github.com/Sudharsanram/Search-Algorithm/assets/119393980/e62961c0-1a5d-48b3-9ac2-f2d4e1e0b37f)

ii)	# Find the element in a list using Binary Search(Iterative Method).
![image](https://github.com/Sudharsanram/Search-Algorithm/assets/119393980/9c2d473e-20cd-462e-ab39-89df155c8916)

iii)	# Find the element in a list using Binary Search (recursive Method).
![image](https://github.com/Sudharsanram/Search-Algorithm/assets/119393980/81b9a664-55a8-4d45-97e9-e535088dba29)


## Result
Thus the linear search and binary search algorithm is implemented using python programming.
