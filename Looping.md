# Looping
---
## No. 1 - For
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

---
## No. 2 - While
```python
offset = 8

while offset > 0:
    print('correcting...')
    offset = offset -1
    
    print(offset)
```
Result:
```
correcting...
7
correcting...
6
correcting...
5
correcting...
4
correcting...
3
correcting...
2
correcting...
1
correcting...
0
```

---
## No. 3 - While-If-Else
```python
offset = -6

while offset != 0 :
    print("correcting...")
    if offset > 0:
      offset = offset-1
    else : 
      offset = offset+1
    print(offset)
```
Result:
```
correcting...
-5
correcting...
-4
correcting...
-3
correcting...
-2
correcting...
-1
correcting...
0
```

---
## No. 4 - For
Write a for loop that iterates over all elements of the areas list and prints out every element separately.
```python
areas = [11.25, 18.0, 20.0, 10.75, 9.50]

for wide in areas:
    print(wide)
```
Result:
```
11.25
18.0
20.0
10.75
9.5 
``` 

---
## No. 5 - For (enumerate)
enumerate is used to access index and its element.

Update the print() statement so that on each run, a line of the form "room x: y" should be printed, where x is the index of the list element and y is the actual list element, i.e. the area. Make sure to print out this exact string, with the correct spacing.
```python
areas = [11.25, 18.0, 20.0, 10.75, 9.50]

for x, y in enumerate(areas):
    print("room " + str(x) + ":" + str(y))
```
Result:
```
room 0:11.25
room 1:18.0
room 2:20.0
room 3:10.75
room 4:9.5
```
Room 0 sounds strange, so we need to update it to start from Room 1. Here we go:
```python
areas = [11.25, 18.0, 20.0, 10.75, 9.50]

for index, area in enumerate(areas) :
    print("room " + str(index + 1) + ": " + str(area))
```
Result:
```
room 1: 11.25
room 2: 18.0
room 3: 20.0
room 4: 10.75
room 5: 9.5
```

---
## No. 6 - For in 2D List
```python
house = [["hallway", 11.25], 
         ["kitchen", 18.0], 
         ["living room", 20.0], 
         ["bedroom", 10.75], 
         ["bathroom", 9.50]]
         
for x, y in house:
    print("the " + str(x) + " is " + str(y) + " sqm")
```
Result:
```
the hallway is 11.25 sqm
the kitchen is 18.0 sqm
the living room is 20.0 sqm
the bedroom is 10.75 sqm
the bathroom is 9.5 sqm
```

---
## No. 7 - For in Dictionary
**xxx.items():**
```python
europe = {'spain':'madrid', 'france':'paris', 'germany':'berlin','norway':'oslo', 'italy':'rome', 'poland':'warsaw', 'austria':'vienna' }

for k, v in europe.items():
    print("the capital of " + str(k) + "is " + str(v))
```
Result:
```
    the capital of norwayis oslo
    the capital of polandis warsaw
    the capital of spainis madrid
    the capital of germanyis berlin
    the capital of austriais vienna
    the capital of italyis rome
    the capital of franceis paris
```

---
## No. 8 - For in Numpy Array
**np_nditer(xxx):**
```python
import numpy as np

for x in np.nditer(np_height):
    print(str(x) + " inches")
```
Result:
```
74 inches
74 inches
72 inches
72 inches
73 inches
69 inches
.........
75 inches
73 inches
```

---
## No. 9 - For in DataFrame
**xxx.iterrows():**
Lab is label:
```
US
AUS
JPN
IN
RU
MOR
EG
```
row is the DataFrame rows:
```
cars_per_cap              809
country         United States
drives_right             True
Name: US, dtype: object
cars_per_cap          731
country         Australia
drives_right        False
Name: AUS, dtype: object
........................
cars_per_cap       45
country         Egypt
drives_right     True
Name: EG, dtype: object
```

Using the iterators lab and row, adapt the code in the for loop such that the first iteration prints out "US: 809", the second iteration "AUS: 731", and so on.
The output should be in the form "country: cars_per_cap". Make sure to print out this exact string (with the correct spacing).
```python
import pandas as pd

cars = pd.read_csv('cars.csv', index_col = 0)

for lab, row in cars.iterrows():
    print(lab + ": " + str(row['cars_per_cap']))
```
Result:
```
US: 809
AUS: 731
JPN: 588
IN: 18
RU: 200
MOR: 70
EG: 45
```
  



