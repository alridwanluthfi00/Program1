# NAMA  : LUTHFI AL RIDWAN
# NIM   : 312010112
# KELAS : TI.20.A.1
------------------------------------------------------------------------------------------
# UAS BAHASA PEMROGRAMAN

## Assalamualaikum Warahmatullahi Wabarakatuh
## Disini saya akan menjelaskan tugas UAS, berikut adalah gambar dari soal yang telah diberikan :

![1](https://user-images.githubusercontent.com/73066008/104170411-a8621e80-5433-11eb-845c-9a6c28f36bc3.png)

# Langkah - langkah
- Pertama kita buka aplikasi PyCharm, lalu kita buat package file seperti gambar berikut :

![2](https://user-images.githubusercontent.com/73066008/104176497-ec582200-5439-11eb-800b-09b834a5053d.png)

- Langkah selanjutnya adalah kita lakukan coding pada file dengan ekstensi .py

## Input code untuk file daftar_nilai.py

    from data import data



    print("Aplikasi Penilaian Mahasiswa")
    while True:
    print("")
    c =input("(L)lihat, (T)ambah, (U)bah, (H)apus, (K)eluar : ")
    if c.lower() == 't':
        print("======= Tambah Data =======")
        nama = input("Nama                :  ")
        nim = input("Nim                 :  ")
        tugas = int(input("Masukan Nilai Tugas :  "))
        uts = int(input("Masukan Nilai UTS   :  "))
        uas = int(input("Masukan Nilai UAS   :  "))
        akhir = (0.30 * tugas) + (0.35 * uts) + (0.35 * uas)
        data[nama] = nim, tugas, uts, uas, akhir
     elif c.lower() == 'u':
        print('=======Ubah Data Mahasiswa=======')
        nama = input('Nama                :  ')
        if nama in data.keys():
            nim = input('Nim                 :  ')
            tugas = int(input("Masukan Nilai Tugas :  "))
            uts = int(input("Masukan Nilai UTS   :  "))
            uas = int(input("Masukan Nilai UAS   :  "))
            akhir = (0.30 * tugas) + (0.35 * uts) + (0.35 * uas)
            data[nama] = nim, tugas, uts, uas, akhir
        else:
            print("Data Nilai Tidak Ada".format(nama))

        elif c.lower() == 'l':
        print("=======Daftar Nilai Mahasiswa=======")
        print("================================================================================================")
        print(" |NO   |     NAMA      |    NIM    |     TUGAS    |     UTS     |       UAS    |    AKHIR     | ")
        print("================================================================================================")
        i = 0
        for x in data.items():
            i += 1
            print(
                " | {6:2}  |  {0:12s} | {1:9s} | {2:11}  | {3:11} | {4:11}  |  {5:11} |".format(x[0], x[1][0], x[1][1],
                                                                                                x[1][2], x[1][3],
                                                                                                x[1][4], i))
            print("============================================================================================")

      elif c.lower() == 'h':
        print("=======Hapus Data Mahasiswa=======")
        nama = input("Nama :  ")
        if nama in data.keys():
            del data[nama]
        else:
            print("Data Nilai Tidak Ada".format(nama))

      elif c.lower() == 'k':
        print("Keluar")
        break
        
- Seperti inilah output codenya : 

![3](https://user-images.githubusercontent.com/73066008/104183273-507fe380-5444-11eb-9ff2-69f5967a102d.png)

- Penjelasan :

Pada coding file daftar_nilai.py kita sudah membuat menu tambah data, lihat data, hapus data, ubah data dan keluar


        
## Input code untuk file input_nilai.py

    from data import data


    while True:
        print("")
        c =input("(T)ambah : ")
        if c.data() == 't':
            print("=======Tambah Data=======")
            nama = input("Nama                :  ")
            nim = input("Nim                 :  ")
            tugas = int(input("Masukan Nilai Tugas :  "))
            uts = int(input("Masukan Nilai UTS   :  "))
            uas = int(input("Masukan Nilai UAS   :  "))
            akhir = (0.30 * tugas) + (0.35 * uts) + (0.35 * uas)
            data[nama] = nim, tugas, uts, uas, akhir

            break
            
 - Seperti inilah output codenya :
 
 ![4](https://user-images.githubusercontent.com/73066008/104186114-81faae00-5448-11eb-844c-be7a0165bfdd.png)
            
 ## Input code untuk file view_nilai.py
 
    from data import data



    while True:
        print("")
        c =input("(L)lihat, : ")
    if data():
        print("=======Daftar Nilai Mahasiswa=======")
        print("================================================================================================")
        print(" |NO   |     NAMA      |    NIM    |     TUGAS    |     UTS     |       UAS    |    AKHIR     | ")
        print("================================================================================================")
        i = 0
        for x in data.items():
            i += 1
            print(
                " | {6:2}  |  {0:12s} | {1:9s} | {2:11}  | {3:11} | {4:11}  |  {5:11} |".format(x[0], x[1][0], x[1][1],
                                                                                                x[1][2], x[1][3],
                                                                                                x[1][4], i))
            print("============================================================================================")
            
 - Seperti inilah output codenya :
 
 ![5](https://user-images.githubusercontent.com/73066008/104186557-2977e080-5449-11eb-9381-856186746af9.png)

## Mungkin seperti itu yang bisa saya jelaskan, mohon maaf jika ada kesalahan karena saya masih dalam tahap pembelajaran. Tetap semangat, sekian dari saya dan terima kasih.
## Wassalamu'alaikum Warahmatullahi Wabarakatuh.