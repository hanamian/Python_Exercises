# No. 1
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
# No. 2
The provided code stub reads and integer, n, from STDIN. For all non-negative integers i<n, print i^2

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
