# LIST

### No. 1
Mencari nilai runner-up (no.2 terbesar). Input baris pertama berisi jumlah data dan baris kedua adalah angkanya (berspasi). Misal listnya: [4, 3, 5, 2, 1, 1], maka outputnya adalah 4. Gunakan **sorted(set(** !

Input:
```python
6
4 3 5 2 1 1
```
```python
n   = int(input())
arr = map(int, input().split())
print(sorted(set(arr))[-2])
```
Output:
```
4
```
---
### No. 2
Dimensi kubus terdiri dari integer **x, y, z**. Koordinat yang mungkin, terbentuk dari **i, j, k**, dengan syarat:
- i+j+k tidak sama dengan 0
- 0 <= i <= x
- 0 <= j <= y
- 0 <= k <= z

Misalnya: x=1, y=1, z=2, n=3

Semua permutasi [i, j, k] yang mungkin adalah:
[[0,0,0], [1,0,0], [0,1,0], [0,0,1], [0,0,2], [1,1,0], [1,0,1], [1,0,2], [1,1,1], [1,1,2], [0,1,1], [0,1,2]]



---
### No. 3
Mengurutkan nilai anak dari nested list. Input baris pertama berisi jumlah anak, baris kedua adalah nama anak, dan baris ketiga adalah nilai anak tersebut. Carilah siapa yang memiliki nilai terendah nomor kedua! Jika hasilnya terdapat 2 orang dengan nilai yang sama, maka print keduanya dengan urutan abjad!

Input:
```python
5
Intan
87.55
Hary
99.20
Isma
95.37
Mia
87.55
Alisha
75.68
```
```python
if __name__ == '__main__':
    student_n_score = []
    for _ in range(int(input())):
        name  = input()
        score = float(input())
        student_n_score.append([name, score])
        
    # Urutan scorenya dari kecil ke besar
    second_lowest = sorted(set([i[1] for i in student_n_score]))[1]
    sorted_name   = sorted(set([i[0] for i in student_n_score if i[1] == second_lowest]))
    print("\n".join(sorted_name))
```
Output:
```
Intan
Mia
```
---
### No. 4
Input pertama berisi jumlah murid. Baris berikutnya berisi nama dan skornya. Baris terakhir berisi **query_name**. Query_name ini akan memberikan output berupa **rata-rata** nilai yang dimiliki. Contohnya adalah:
```
3
Krishna 67 68 69
Arjun 70 98 63
Malika 52 56 60
Malika

Output:
56.00
```
Input:
```python
5
Harry 70 88 94
Mia 99 80 89
Hana 88 79 87
Tian 60 68 100
Dita 77 86 92
Hana
```
```python
if __name__ == '__main__':
    n = int(input())
    nilai = {}
    for _ in range(n):
        name, *line = input().split()
        score = list(map(float, line))
        nilai[name] = score
    query_name = input()
   
    avg = sum(nilai[query_name])/ len(nilai[query_name])
    print("%.2f" % avg)
```
Output:
```
84.67
```
---
### No. 5

Input
```python
12
insert 0 5
insert 1 10
insert 0 6
print
remove 6
append 9
append 1
sort
print
pop
reverse
print
```
```python
