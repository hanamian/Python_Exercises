# If Elif Else
---
## 1. If - Else
```python
room = "kit"
area = 14.0

if room == "kit" :
    print("looking around in the kitchen.")
else :
    print("looking around elsewhere.")

if area > 15 :
    print("big place!")
else:
    print("pretty small.")
```
Result:
```
looking around in the kitchen.
pretty small.
```

---
## 2. If - Elif - Else
```python
area = 14.0

if area > 15 :
    print("big place!")
elif area > 10:
    print("medium size, nice!")
else :
    print("pretty small.")
```
Result:
```
medium size, nice!
```

---
## 3.
Given an integer n, perform the following conditional actions:

If n is odd, print Weird
If n is even and in the inclusive range of 2 to 5, print Not Weird
If n is even and in the inclusive range of 6 to 20, print Weird
If n is even and greater than 20, print Not Weird

Answer:
```python
n = int(raw_input().strip())
if n%2==0 and (n in range (2,6) or n>20):
    print('Not Weird')
else:
    print('Weird')
```
```
input:
3

output:
Weird
```

---
## 4. IF NOT 
```python
z = 55

if not z== 77:
    print('z bukan 77')
```
