# Regex

### No. 1
Input berisi digit 0-9, koma(**,**), dan titik(**.**). Yang harus dilakukan adalah me**re.split()** berdasarkan **, ** dan **.**

Input:
```python
108.016,000,450.002.001
```
```python
regex_pattern = r"[.,]"
import re...
```
Output:
```
108
016
000
450
002
001
```
