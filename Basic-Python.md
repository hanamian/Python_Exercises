# Basic Python
### 1. Append di List
```python
buah = ['apel', 'semangka', 'durian', 'nanas']
buah.append('pepaya')

buah[0] = 'jambu'

print(buah)
```
Result:
```
'jambu', 'semangka', 'durian', 'nanas', 'pepaya'
```
### 2. IF NOT
```python
x = 8

if not x==7:
  print('itu bukan 7')
```
Result:
```
itu bukan 7
```
### 3. DICTIONARY
```python
fruits = {'apel': 'apple', 'jeruk': 'orange', 'anggur': 'grape'}      
fruits['mangga']='mango'  

print(fruits['jeruk'])
print('Bahasa Inggris apel adalah ', fruits['apel'])
print(fruits)

# Looping
for i in fruits:
    print(i + " adalah " + fruits[i] + " dalam bahasa Inggris")
```
Result:
```
orange
Bahasa Inggris apel adalah apple
{'apel': 'apple', 'jeruk': 'orange', 'anggur': 'grape', 'mangga':'mango'}

apel adalah apple dalam bahasa Inggris
jeruk adalah orange dalam bahasa Inggris
anggur adalah grape dalam bahasa Inggris
mangga adalah mango dalam bahasa Inggris
```
### 4. BREAK and CONTINUE
```python
angka = [50, 78, 99, 30]
for i in angka:
    print(angka)
    if i == 99:
        break
```
Result:
```
50
78
99
```
```python
angka = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
for i in angka:
    # Lewatkan loop untuk angka yang dapat di bagi 2
    if i % 2 == 0: continue
    print(i)
```
Result:
```
1
3
5
7
9
```
### 5. CLASS
```python
class Menu():
  pass

menu1 = Menu()
```

