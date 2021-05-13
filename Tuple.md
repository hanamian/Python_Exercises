# Tuple

### No. 1
Input integer **n**. Input baris pertama adalah nilai dari n. Input baris kedua adalah integer dari n yang terpisah spasi. **t** adalah tuple. Print hash(t)!

Input:
```python
5
1 4 5 2 9
```
```python
if __name__ == '__main__':
    n = int(input())
    integer_list = map(int, input()).split()
    t = tuple(integer_list)
    print(hash(t))
```
Output:
```
7105070165031021912
```
