# Tugas-Uas-AI

Nama  : Rizky Adi Ryanto<br>
Nim   : 19.01.013.044<br>
Kelas : AI B <br>

# Program menghitung luas persegi panjang, segitiga, dan lingkaran menggunakan fungsi

```
def persegipanjang(panjang,lebar):
    return panjang * lebar

def segitiga(alas,tinggi):
    return (0.5 * (alas * tinggi))

def lingkaran(r):
    return (3.14 * (r ** 2))

print("1. Luas Persegi Panjang\n2. Luas Segitiga\n3. lingkaran")
pilih = int(input("Masukan Pilihan :"))

luas = None

if pilih == 1:
    panjang = int(input("masukan panjang :"))
    lebar = int(input("masukan lebar :"))
    luas = persegipanjang(panjang,lebar)
elif pilih == 2:
    alas = int(input("masukan alas :"))
    tinggi = int(input("masuk tinggi :"))
    luas = segitiga(alas,tinggi)
elif pilih == 3:
    r = float(input("masukan jari - jari :"))
    luas = lingkaran(r)

print(float(luas))
```

# Modifikasi problem di atas dengan mengakses function berbeda file 

  <b> main.py </b>
```
import function as fl

print("1. Luas Persegi Panjang\n2. Luas Segitiga\n3. lingkaran")
pilih = int(input("Masukan Pilihan :"))

luas = None

if pilih == 1:
    panjang = int(input("masukan panjang :"))
    lebar = int(input("masukan lebar :"))
    luas = fl.persegipanjang(panjang,lebar)
elif pilih == 2:
    alas = int(input("masukan alas :"))
    tinggi = int(input("masuk tinggi :"))
    luas = fl.segitiga(alas,tinggi)
elif pilih == 3:
    r = float(input("masukan jari - jari :"))
    luas = fl.lingkaran(r)

print(float(luas))
```

<b> function.py </b>
```
def persegipanjang(panjang,lebar):
    return panjang * lebar

def segitiga(alas,tinggi):
    return (0.5 * (alas * tinggi))

def lingkaran(r):
    return (3.14 * (r ** 2))
```

# Hitung Luas Segitiga menggunakan Fungsi
```
def segitiga(alas,tinggi):
    return (0.5 * (alas * tinggi))

alas = int(input("masukan alas :"))
tinggi = int(input("masuk tinggi :"))
luas = segitiga(alas,tinggi)
print("Luas Segitiga adalah :",luas)
```

# Hitung nilai tertinggi dari sekelompok data yang di tampung di dalam sebuah list

jika menggunakan fungsi max maka 10 dan 11 akan di anggap bilangan tunggal.
```
def proses(deret_bilangan):
    nilai_terbesar = deret_bilangan[0]

    for nilai in deret_bilangan:
        if nilai > nilai_terbesar:
            nilai_terbesar = nilai

    return nilai_terbesar
 
def cetakhasil(hasil):
    print("bilangan terbesar adalah :",proses(hasil))       

def inputdata():
    bilangan = []
    n = int(input("masukan banyak data yang di inginkan :"))
    for i in range(n):
        masukandata = float(input("masukan bilangan :"))
        bilangan.append(masukandata)
    cetakhasil(bilangan)
    
inputdata()
```

# Menampilkan bilangan kelipatan dari inputan user
```
def cetakhasil(cetak):
    print("bilangan kelipatan :", cetak)

def proses(nilai,kelipatan):
    for i in nilai:
        if i % kelipatan == 0:
            cetakhasil(i)
            
def inputdata():
    bilangan = []
    for i in range(5):
        masukandata = int(input("masukan bilangan :"))
        bilangan.append(masukandata)

    kelipatan = int(input("masukan kelipatan :"))
    
    hasil = proses(bilangan,kelipatan)
    cetakhasil(hasil)
    
inputdata()
```

# Program menghitung faktorial sebuah bilangan(input) menggunakan fungsi 

```
def faktorial(n):
    if n > 2:
        return n * faktorial(n - 1)
    
    return 2

bilangan = int(input("bilangan :"))
faktor = faktorial(bilangan)
print(f'{bilangan}! = {faktor}')
```

# Program menjumlahkan List, Disini akan saya demokan dalam bentuk matriks
```
def cetak_matriks(matriks):
    for row in matriks:
        print(row)
 
def pjg_matriks(matriks):
    return len(matriks[0])
 
def lbr_matriks(matriks):
    return len(matriks)
 
def jumlahkan_matriks(mat_a, mat_b):
    temp_row = []
    temp_mat = []
 
    for i in range(0, lbr_matriks(mat_a)):
        for j in range(0, pjg_matriks(mat_a)):
            temp_row.append(mat_a[i][j] + mat_b[i][j])
        temp_mat.append(temp_row)
        temp_row = []
    return temp_mat
 
list_a = [[1, 2, 3, 5], [1, 2, 3, 5], [1, 2, 3, 5]]
list_b = [[1, 1, 1, 1], [1, 1, 1, 1], [1, 1, 1, 1]]
 
print("list_a : ")
cetak_matriks(list_a)
 
print("\nlist_b : ")
cetak_matriks(list_b)
 
print("\nhasil penjumlahan :")
hasil = jumlahkan_matriks(list_a, list_b)
cetak_matriks(hasil)
```
# Program menghitung persamaan kuadrat
```
print("Persamaan: ax^2 + bx + c = 0")
a = float(input("a = "))
b = float(input("b = "))
c = float(input("c = "))
print("-----------------------------")
det = b * b - 4 * a * c
if (det<0) :
  print("Akar Imajiner.")
else :
  x1 = (b + math.sqrt(det))/(2 * a)
  x2 = (b - math.sqrt(det))/(2 * a)
  print("x1 =", x1)
  print("x2 =", x2)
```
