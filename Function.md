# Function
---

## No. 1 
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
```

---
