# Kelompok3_Tugas_Algoritma


Kelompok terdiri dari 4 orang. Masing-masing mengerjakan satu function atau procedure. Setiap orang harus melihat Clue untuk pengerjaan dan dikerjakan dalam bentuk PASCAL bukan Algoritma. Sebelum mengerjakan clue, copy script dasar dari program disini : Script_Dasar.pas

Setelah itu baru kerjakan clue didalam script tersebut dan tes programnya (compile). Sesudah mengerjakan clue-nya, tolong pastekan hasil pengerjaannya di Pastebin.com dengan settingan-nya diatur! Terakhir berikan link hasil generate copasinnya ke LINE saya. Setelah selesai semua, script tadi akan digabungkan dan akan dipost disini.

Contoh:

A1. Clue

    Type: Procedure
    Nama: HitungPerkalian
    Parameter: bilangan1, bilangan2 (Input-Integer), hasil (Output-Integer)
    Algoritma:

    hasil <- bilangan1 * bilangan2

A2. Hasil Pengerjaan

procedure HitungPerkalian(bilangan1, bilangan2 : Integer; var hasil : Integer);
{I.S. : }
{F.S. : }
begin
    hasil := bilangan1 * bilangan2;
end;

Alur Program

Pertama, program akan meminta data tentang berapa jumlah baris (M) dan Kolom (N) untuk nilai matkul yang dibutuhkan. 
Kedua, program akan menampilkan baris pertama tabel untuk di isi oleh user dengan nama mata kuliah. 
Ketiga, dibaris kedua user memasukkan kolom NIM dan nilai mata kuliah di masing-masing kolom; setiap nilai mata kuliah akan di konversikan ke INDEX (A-E) ketika tombol enter ditekan. 
Keempat, setelah user memasukkan semua data disetiap baris; user akan diberi opsi apakah ingin mengisi Kamus Keterangan yang berfungsi sebagai penjelas makna dari kolom judul mata kuliah - ini dikarenakan kolom mata kuliah Maks. 5 Karakter sehingga user harus menyingkat nama mata kuliah yang menyebabkan ketidakjelasan maksud kolom.

Clue Tambahan : maksimal data baris yang boleh di inputkan adalah 50 (MaksM) dan maksimal kolom adalah 8 (MaksN)

Clue
1. Clue - Naufal

    Type: Procedure
    Nama: BacaOrdo
    Parameter: M, N (Output-Integer)
    Contoh: Buka Gambar 1, Buka Gambar 2, Buka Gambar3
    Algoritma:

    Output('Masukkan Jumlah Data Anda (M x N) : ')
    Output('M (Baris): ')
    Input(M)
    Output('N (Kolom)')
    Input(N)

    // melakukan pengulangan apabila M melebihi Maksimal M yang ditentukan
    While (M > MaksM) do
        Output('Nilai M tidak boleh lebih dari ', MaksM)
        Input(M)    
    EndWhile

    // melakukan pengulangan apabila N melebihi Maksimal N yang ditentukan
    While (N > MaksN) do
        Output('Nilai N tidak boleh lebih dari ', MaksN)
        Input(N)
    EndWhile
    
2. Clue - Ikbal

    Type: function
    Nama: NilaiToIndex
    Parameter: Nilai (Input-Integer)
    Result: Char
    
    Algoritma:

    DependOn (Nilai)
    
        80..100 : NilaiToIndex <- 'A'
        70..79  : NilaiToIndex <- 'B'
        60..69  : NilaiToIndex <- 'C'
        50..59  : NilaiToIndex <- 'D'
        0..49   : NilaiToIndex <- 'E'
        
    EndDepend

3. Clue - Rizky

    Type: Procedure
    Nama: BuatKamusKeterangan
    Parameter: MK (Input-Larik1), N (Input-Integer)
    Kamus Lokal: i (Integer), Ket (Larik1)
    Contoh: Gambar1
    Algoritma:

    Output('Kamus Keterangan:')
    for i <- 1 to N do
        Output('- ', MK[i], ' : ')
        Input(Ket[i])
    endfor

4. Clue - Yudi

Menampilkan tabel dan memanggil berbagai fungsi & procedure dari clue-clue sebelumnya.
