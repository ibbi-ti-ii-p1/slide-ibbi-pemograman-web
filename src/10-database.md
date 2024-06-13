---
marp: true
theme: gaia
paginate: true
footer: https://github.com/ibbi-ti-ii-p1/slide-ibbi-pemograman-web
style: |
  section::after {
    content: 'Page ' attr(data-marpit-pagination) ' / ' attr(data-marpit-pagination-total);
  }
---

# Database

<!--
_class: lead
_paginate: skip
-->

---

## Apa itu Database ?

Database, atau basis data, adalah kumpulan data yang terorganisir dengan baik.  Data ini disimpan secara elektronik pada sistem komputer sehingga mudah untuk dicari, dikelola, dan diupdate.

---

## Apa itu Database Relasional

Database relasional adalah jenis database yang mengatur data dalam bentuk tabel-tabel yang saling berhubungan.  Tiap tabel ini terdiri dari baris (record) dan kolom (atribut).

---

## Apa itu MySQL

MySQL adalah salah satu sistem manajemen database relasional (RDBMS) yang paling populer.  RDBMS seperti MySQL mengatur data dalam bentuk tabel-tabel yang saling berhubungan. RDBMS seperti MySQL mengatur data dalam bentuk tabel-tabel yang saling berhubungan.

---

## Karakteristik MySQL

- Open Source
- Mudah digunakan
- Gratis
- Fleksibel
- Andal

---

## Apa itu SQLite

SQLite adalah mesin database relasional yang tertanam (embedded), artinya SQLite  berupa library yang bisa diintegrasikan ke dalam program lain.  Berbeda dengan MySQL yang merupakan  sistem manajemen database (DBMS) yang berdiri sendiri, SQLite tidak memerlukan server terpisah dan  biasanya berukuran lebih kecil.

---

## Karakteristik SQLite

1. Ringan dan Cepat
2. Tanpa Server
3. Mudah digunakan
4. Fleksibel
5. Andal

---

## Apa itu SQL

SQL, atau Structured Query Language, adalah bahasa khusus (domain-specific language) yang dirancang untuk mengelola data dalam  sistem manajemen database relasional (RDBMS).

---

## Contoh SQL 

```sql
-- Menampilkan semua data dari tabel "customers"
SELECT * FROM customers;

-- Mencari pelanggan dengan nama "John Doe"
SELECT * FROM customers WHERE name = 'John Doe';

-- Menambahkan data pelanggan baru
INSERT INTO customers (name, email) VALUES ('Jane Doe', 'jane.doe@example.com');

-- Mengupdate email pelanggan dengan ID 1
UPDATE customers SET email = 'new.email@example.com' WHERE id = 1;

-- Menghapus pelanggan dengan ID 1
DELETE FROM customers WHERE id = 1;
```

--- 

## Install SQLite di NodeJS

Untuk menggunakan SQLite dengan Node.js, Anda memerlukan library `sqlite3`.  Anda dapat menginstalnya menggunakan `npm`:

```js
npm install sqlite3
```

---

## Membuat tabel baru

```js
db.run(`CREATE TABLE users (
  id INTEGER PRIMARY KEY AUTOINCREMENT, 
  username TEXT UNIQUE, 
  password TEXT)`);
```

---

## Menambahkan data baru ke tabel

```js
db.run(`INSERT INTO users 
  (username, password) 
  VALUES (?, ?)`, 
  ['johndoe', 'password123']);
```

---

## Membaca data dari tabel

```js
db.all('SELECT * FROM users', (err, rows) => {
  if (err) {
    console.error(err);
    return;
  }

  console.log(rows);
});
```

---

## Memperbarui data di tabel

```js
db.run('UPDATE users SET password = ? WHERE id = ?', ['newPassword', 1]);
```

---

## Menghapus data dari tabel

```js
db.run('DELETE FROM users WHERE id = ?', [1]);
```

---

## Menutup koneksi ke database

```js
db.close();
```