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
luas = fl.segitiga(alas,tinggi)
print("Luas Segitiga adalah :",luas)
```

# Hitung nilai tertinggi dari sekelompok data yang di tampung di dalam sebuah list
```
def proses(a):
    return max(a)
 
def cetakhasil(hasil):
    print("bilangan terbesar adalah :",hasil)       

def inputdata():
    bilangan = []
    n = int(input("masukan banyak data yang di inginkan :"))
    for i in range(n):
        masukandata = input("masukan bilangan :")
        bilangan.append(masukandata)
        
    hasil = proses(bilangan)
    cetakhasil(hasil)
    
inputdata()
```

# Menampilkan bilangan kelipatan dari inputan user
