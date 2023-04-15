# Tugas Praktikum { Pertemuan ke 6 } <img src=https://logos-download.com/wp-content/uploads/2016/05/MySQL_logo_logotype.png width="130px" >


|**Nama**|**NIM**|**Kelas**|**Matkul**|
|----|---|-----|------|
|Muhammad Ikhsan Fakhrudin|312210019|TI.22.A2|Basis Data|

# Soal Latihan Praktikum

Berdasarkan table Mahasiswa pada praktikum sebelumnya: (nim, nama, jenis_kelamin, tgl_lahir, jalan, kota, kodepos, no_hp, kd_ds)

***Isi data pada table tersebut sebanyak minimal 5 record data. Tampilkan semua isi/record tabel!***

- Ubah data tanggal lahir mahasiswa yang bernama Ari menjadi: 1979-08-31!

- Tampilkan satu baris / record data yang telah diubah tadi yaitu record dengan nama Ari saja!

- Hapus Mahasiswa yang bernama Dina!

- Tampilkan record atau data yang tanggal kelahirannya lebih dari atau sama dengan 1996-1-2!

- Tampilkan semua Mahasiswa yang berasal dari Bekasi dan berjenis kelamin perempuan!

- Tampilkan semua Mahasiswa yang berasal dari Bekasi dengan kelamin laki-laki atau Mahasiswa yang berumur lebih dari 22 tahun dengan kelamin wanita!

- Tampilkan data nama dan alamat mahasiswa saja dari tabel tersebut

- Tampilkan data mahasiswa terurut berdasarkan nama.

**1. Mengisi tabel dengan minimal 5 record data :**
```
insert into mahasiswa (nim, nama, jenis_kelamin, tgl_lahir, jalan, kota, kodepos, no_hp, kd_ds) values -> (11223344,"ari santoso","Laki-laki","1998-10-12","","Bekasi","","",""), -> (11223345,"ario talib","Laki-laki","1999-11-16","","Cikarang","","",""), -> (11223346,"dina marlina","Perempuan","1997-12-01","","Karawang","","",""), -> (11223347,"lisa ayu","perempuan","1996-01-02","","Bekasi","","",""), -> (11223348,"tiara wahidah","perempuan","1980-02-05","","Bekasi","","",""), -> (11223349,"anton sinaga","laki-laki","1988-03-10","","Cikarang","","","");
```

![gambar1](screenshot/ss1.png)

**2. Menampilkan semua isi/record pada tabel bisa menggunakan kode berikut :**

`select*from mahasiswa;`

![gambar2](screenshot/ss2.png)

**3. Mengubah data tanggal lahir mahasiswa yang bernama Ari menjadi : 1979-08-31 menggunakan kode berikut :**

`update mahasiswa set tgl_lahir='1979-08-31' where nim=11223344;`

![gambar3](screenshot/ss3.png)

**4. Menampilkan satu baris / record data yang telah diubah tadi yaitu record dengan nama Ari saja dengan cara sebagai berikut :**

`select*from mahasiswa where nim=11223344;`

![gambar4](screenshot/ss4.png)

**5. Menghapus Mahasiswa yang bernama Dina dengan cara sebagai berikut:**

`delete from mahasiswa where nim=11223346;`

![gamar5](screenshot/ss5.png)

**6. Menampilkan record atau data yang tanggal kelahirannya lebih dari atau sama dengan 1996-1-2 dengan cara sebagai berikut :**

`select*from mahasiswa where tgl_lahir<='1996-1-2';`

![gambar6](screenshot/ss6.png)

**7. Menampilkan semua Mahasiswa yang berasal dari Bekasi dan berjenis kelamin perempuan dengan cara sebagai berikut :**

`select * from mahasiswa where kota='bekasi' and jenis_kelamin='Perempuan';`

![gambar7](screenshot/ss7.png)

**8. Menampilkan semua Mahasiswa yang berasal dari Bekasi dengan kelamin laki-laki atau Mahasiswa yang berumur lebih dari 22 tahun dengan kelamin wanita dengan cara sebagai berikut :**
```
select * from mahasiswa where kota='Bekasi' and jenis_kelamin='Laki-laki' or tgl_lahir<='1997-01-02' and jenis_kelamin='Perempuan';
```

![gambar8](screenshot/ss8.png)

**9. Menampilkan data nama dan jalan mahasiswa saja dari tabel tersebut dengan cara sebagai berikut :**

`select nama, jalan from mahasiswa;`

![gambar9](screenshot/ss9.png)

**10. Menampilkan data mahasiswa terurut berdasarkan nama dengan cara sebagai berikut :**

`select * from mahasiswa -> order by nama asc;`

![gambar10](screenshot/ss10.png)

# Evaluasi