# praktikum.5
codingan praktikum 5

# Program untuk menambahkan data ke dalam sebuah list

# List untuk menyimpan data mahasiswa
data_mahasiswa = []

while True:
    # Meminta input dari user
    nama = input("Nama: ")
    nim = input("NIM: ")
    nilai_tugas = float(input("Nilai Tugas: "))
    nilai_uts = float(input("Nilai UTS: "))
    nilai_uas = float(input("Nilai UAS: "))
    
    # Menghitung nilai akhir
    nilai_akhir = (0.3 * nilai_tugas) + (0.35 * nilai_uts) + (0.35 * nilai_uas)
    
    # Menambahkan data ke list data_mahasiswa
    data_mahasiswa.append({
        "Nama": nama,
        "NIM": nim,
        "Tugas": nilai_tugas,
        "UTS": nilai_uts,
        "UAS": nilai_uas,
        "Akhir": nilai_akhir
    })
    
    # Menanyakan apakah user ingin menambah data lagi
    tambah_data = input("Tambah data(y/t)? ")
    if tambah_data.lower() != 'y':
        break

# Menampilkan daftar data mahasiswa
print("\n| No | Nama      | NIM   | Tugas | UTS | UAS | Akhir |")
print("=======================================================")
for i, mhs in enumerate(data_mahasiswa, start=1):
    print(f"| {i:<2} | {mhs['Nama']:<9} | {mhs['NIM']:<5} | {mhs['Tugas']:<5} | {mhs['UTS']:<3} | {mhs['UAS']:<3} | {mhs['Akhir']:.2f} |")

codingn latihan pertemuan 9
# 1. Membuat list dengan 5 elemen
print("1. Membuat list dengan 5 elemen:")
list_A = [50, 60, 70, 80, 90]
print("List A:", list_A)
print()

# 2. Akses list
print("2. Akses list:")
# Tampilkan elemen ke 3
print("Elemen ke 3:", list_A[2])
# Ambil nilai elemen ke 2 sampai ke 4
print("Elemen ke 2 sampai ke 4:", list_A[1:4])
# Ambil elemen terakhir
print("Elemen terakhir:", list_A[-1])
print()

# 3. Ubah elemen list
print("3. Ubah elemen list:")
# Ubah elemen ke 4 dengan nilai lainnya
list_A[3] = 75
print("Setelah mengubah elemen ke 4:", list_A)
# Ubah elemen ke 4 sampai elemen terakhir
list_A[3:] = [75, 95]
print("Setelah mengubah elemen ke 4 sampai akhir:", list_A)
print()

# 4. Tambah elemen list
print("4. Tambah elemen list:")
# Ambil 2 bagian dari list pertama (A) dan jadikan list ke 2 (B)
list_B = list_A[0:2]
print("List B yang diambil dari 2 bagian list A:", list_B)

# Tambah list B dengan string
list_B.append("hiii bos")
print("List B setelah ditambah string:", list_B)

# Tambah list B dengan 3 nilai
list_B.extend([90, 100, 110])
print("List B setelah ditambah 3 nilai:", list_B)

# Gabungkan list B dengan list A
list_gabungan = list_B + list_A
print("Hasil penggabungan list B dengan list A:", list_gabungan)


