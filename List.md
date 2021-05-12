# LIST

### No. 1
Mencari nilai runner-up (no.2 terbesar). Input baris pertama berisi jumlah data dan baris kedua adalah angkanya (berspasi). Misal listnya: [4, 3, 5, 2, 1, 1], maka outputnya adalah 4. Gunakan **sorted(set(**!

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
Mengurutkan nilai anak dari nested list. Input baris pertama berisi jumlah anak, baris kedua adalah nama anak, dan baris ketiga adalah nilai anak tersebut. Carilah siapa yang memiliki nilai terendah nomor kedua. Jika hasilnya terdapat 2 orang dengan nilai yang sama, maka print keduanya dengan urutan abjad!

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
```



