# SQL Study II
SQL adalah bahasa database untuk pengaturan dan analisis data. Dalam pelajaran ini Anda akan mempelajari dasar-dasar pengunaan SQL.

## **1. Apa itu database?**
Solusi: 
1. Klik tab Database, lihat data yang ada 
2. Klik tombol Kirim 


## **2. Apa itu Kueri?**

exercise1.sql 
``` sql
-- Akses kolom "name" dari tabel "purchases" 
SELECT name 
FROM purchases; 
```

exercise2.sql 
``` sql
-- Akses kolom "price" dari table "purchases"
SELECT price 
FROM purchases;
```

## **3. Memilih Banyak Kolom** 
exercise1.sql 
``` sql
```

exercise1.sql 
``` sql
-- Akses kolom "name" dan "price" dari tabel "purchases" 
SELECT name, price
FROM purchases;
```

exercise2.sql 
``` sql
-- Akses semua kolom dari tabel "purchases" 
SELECT * 
FROM purchases;
```

## **4. WHERE (1)**
exercise1.sql 
``` sql
/*
Dibawah "FROM purchases" tambahkan code untuk mengambil baris dengan
nilai "makanan" dikolom "category" 
*/

SELECT *
FROM purchases
WHERE category = "makanan";
```

## **5. WHERE (2)**
exercise1.sql 
``` sql
/*
dibawah baris "FROM purchases" tambahkan code untuk
mendapatkan baris dengan nilai "10" dikolom "price" 
*/

SELECT *
FROM purchases
WHERE price = 10;
```
exercise2.sql 
``` sql
/*
dibawah baris "FROM purchases" tambahkan code untuk
mendapatkan baris dengan nilai "2018-10-10" dikolom "purchased_at" 
*/

SELECT *
FROM purchases
WHERE purchased_at = '2018-10-10';
```


## **6. Operator Perbandingan**

exercise1.sql 
```sql
/*
dibawah "FROM purchases" tambahkan code untuk
mengambil baris dengan nilai "10" atau lebih dari kolom "price" 
*/

SELECT *
FROM purchases
WHERE price >= 10;  
```
execise.sql 
```sql
 /*
dibawah "FROM purchases" tambahkan code untuk mengambil baris dengan
nilai tanggal "2018-11-01" dan sebelumnya dari kolom "purchased_at"
*/

SELECT *
FROM purchases
WHERE purchased_at <= '2018-11-01';
```
## **7. LIKE (1)**
exercise.sql 
```sql 
/*
dibawah "FROM purchases" tambahkan code untuk mengambil
baris dimana nilai "name" mengandung kata "puding"
*/

SELECT *
FROM purchases
WHERE name LIKE "%puding%"; 
```

## **8. LIKE (2)**
exercise1.sql
```sql
/*
dibawah "FROM purchases" tambahkan code untuk
mengambil baris dimana nilai "name" dimulai dengan kata "puding"
*/

SELECT *
FROM purchases
WHERE name LIKE "puding%";
```

exercise2.sql 
```sql
/*
dibawah "FROM purchases" tambahkan code untuk
mengambil baris dimana nilai "name" diakhiri dengan kata "puding"
*/

SELECT *
FROM purchases
WHERE name LIKE "%puding";
```

## **9. NOT**
exercise1.sql
```sql
/*
dibawah "FROM purchases" tambahkan code untuk mendapatkan semua baris dimana
kolom "character_name" bukanlah "Ninja Ken"
*/

SELECT *
FROM purchases
WHERE NOT character_name = 'Ninja Ken'; 
```

exercise2.sql 
```sql
/*
dibawah "FROM purchases" tambahkan code untuk mendapatkan semua baris dimana
kolom "name" tidak mengandung kata "puding"
*/

SELECT *
FROM purchases
WHERE NOT name LIKE "%puding%";
```

## **10. IS NULL IS NOT NULL**
exercise1.sql
```sql 
/*
dibawah "FROM purchases" tambahkan code untuk mengambil baris
dimana kolom  "price" adalah NULL
*/

SELECT *
FROM purchases
WHERE price IS NULL; 
```

exercise2.sql 
```sql
/*
dibawah "FROM purchases" tambahkan code untuk mengambil baris
dimana kolom "price" adalah NOT NULL
*/

SELECT *
FROM purchases
WHERE price IS NOT NULL; 
```

## **11. AND OR**
exercise1.sql
```sql
/*
dibawah "FROM purchases" tambahkan code untuk mengambil baris
dimana nilai kolom "category" adalah "makanan"
dan nilai kolom "character_name" adalah "Guru Domba"
*/

SELECT *
FROM purchases
WHERE category = 'makanan'
AND character_name = 'Guru Domba'; 
```

exercise2.sql 
```sql
/*
dibawah "FROM purchases" tambahkan code untuk mengambil baris
dimana nilai kolom "category" adalah "makanan"
atau nilai kolom "character_name" adalah "Ninja Ken"
*/

SELECT *
FROM purchases
WHERE category = 'makanan'
OR character_name = 'Ninja Ken'; 
```

## **12. ORBER BY**
exercise1.sql 
```sql
/* 
dibawah "FROM purchases" tambahkan code untuk
menampilkan baris dari nilai yang terbesar dikolom "price"
*/

SELECT *
FROM purchases
ORDER BY price DESC; 
```
exercise2.sql
```sql
/*
dibawah WHERE character_name = "Ninja Ken", tambahkan code untuk
menampilkan baris dari nilai terkecil dikolom "price"
*/

SELECT *
FROM purchases
WHERE character_name = "Ninja Ken"
ORDER BY price ASC; 
```

## **13. LIMIT**
exercise1.sql 
```sql
/*
dibawah "FROM purchases" tambahkan code untuk
menampilkan maksimum 5 baris hasil
*/

SELECT *
FROM purchases
LIMIT 5;  
```

exercise2.sql
```sql
/*
dibawah WHERE character_name = "Ninja Ken",
tambahkan code untuk menampilkan hasil maksimum 10 baris
*/

SELECT *
FROM purchases
WHERE character_name = "Ninja Ken"
LIMIT 10; 
```

## **14. Mempraktikkan Hal Yang Sudah Anda Pelajari**
exercise1.sql 
```sql
/*
Dibawah "FROM purchases" tambahkan code untuk mengambil baris
dengan nilai tanggal "2018-11-01" dan sebelumnya, dari kolom "purchased_at"
*/

SELECT *
FROM purchases
WHERE purchased_at <= '2018-11-01'; 
```

exercise2.sql
```sql
/*
Dibawah "FROM purchases" tambahkan code untuk baris dimana
kolom "name" mengandung string "puding"
*/

SELECT *
FROM purchases
WHERE name LIKE "%puding%"; 
```

exercise3.sql 
```sql
/*
dibawah "FROM purchases" gunakan operator NOT untuk menambahkan code untuk
mengambil baris dimana nilai kolom "character_name" adalah bukan "Ninja Ken"
*/

SELECT *
FROM purchases
WHERE NOT character_name = 'Ninja Ken'; 
```
exercise4.sql 
```sql
/*
dibawah "FROM purchases" tambahkan code untuk
menambahkan baris dimana kolom "price" adalah NULL
*/

SELECT *
FROM purchases
WHERE price IS NULL;  
```
exercise5.sql 
```sql
/*
setelah "FROM purchases" tambahkan code untuk mengambil baris dimana nilai
kolom "category" adalah "makanan" dan kolom "character_name" adalah "Guru Domba"
*/

SELECT *
FROM purchases
WHERE category = 'makanan'
AND character_name = 'Guru Domba';  
```
exercise6.sql 
```sql
 /*
dibawah "FROM purchases" tambahkan code untuk mengambil maksimum 5 baris
dengan urutan terbesar dari kolom "price"
*/

SELECT *
FROM purchases
ORDER BY price DESC
LIMIT 5; 
```