# Least-Common-Multiple-adding-datetime-with-Python

I use **a** for Aga and **b** for Bian. Aga start running at 12.00 with speed 7m/s and Bian start running at 13.00 with speed 10m/s.
**QUESTION:** What time they will meet in a same point?
```python
def lcm(a,b):
  x=1
  y=1
  p=a*x
  q=b*y
  while p!=q:
    while p>q:
      y=y+1
      q=b*y
    while p<q:
      x=x+1
      p=a*x
  if p==q:
      print(p)
lcm(7,10) 
```
### The result should be **70**

So here we get 70 minutes (calculated from the first one go off) for them to meet and having the same point.

# Creating Aga time and lcm in hours format 

```python
import datetime
from datetime import datetime, timedelta
meet = timedelta(hours=12, minutes=00, seconds=00, microseconds=00)+timedelta(hours=0, minutes=70, seconds=00, microseconds=00)
print(meet)
```
### Finally, we found the time when they meet and stand in the same point, exactly at **13:10:00**
