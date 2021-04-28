# Looping
---
## No. 1 - For (Looping)
The provided code stub reads and integer, n, from STDIN. For all non-negative integers i<n, print i**2!
Example: n=3
The list of non-negative integers that are less than n=3 is [0,1,2]. Print the square of each number on a separate line.

Answer:
I use in range(n) because it will automatically started from 0 to n-1
```python
n = int(input().strip())
for i in range(n):
    print i**2
```
```
input:
5

output:
0
1
4
9
16
```

# No. 3 (Function)
Given a year, determine whether it is a leap year. If it is a leap year, return the Boolean True, otherwise return False.
Note that the code stub provided reads from STDIN and passes arguments to the **is_leap** function. It is only necessary to complete the is_leap **function**. The years 2000 and 2400 are leap years, while 1800, 1900, 2100, 2200, 2300 and 2500 are NOT leap years.

Answer:
Leap years can be divided by 4
```python
def is_leap(year):
    leap = False
  
    if year<=(10**5) and year>=1900:
        if year%4!=0:
            return leap

year = int(raw_input())
```
```
input:
1990

output:
False
