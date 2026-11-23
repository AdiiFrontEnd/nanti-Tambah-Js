# Variabel
Variabel Adalah Sebuah Data Yang Disimpan Pada Sebuah Nama Untuk Di Pakai Berulang Ulang

> AI
> **Variabel adalah nama yang merujuk ke sebuah data (nilai) yang disimpan di memori, supaya bisa dipakai dan diubah berulang kali.**

Intinya ada 3 hal:
1. **Nama**: identitas variabel (misalnya `umur`)
2. **Nilai**: data yang disimpan (misalnya `20`)
3. **Memori**: tempat data itu tersimpan, yang diakses lewat nama tadi

```javascript
let umur = 20;      // nama: umur, nilai: 20
console.log(umur);  // dipakai: 20
console.log(umur + 1); // dipakai lagi: 21
```

Satu tambahan kecil: variabel `let` bisa diubah nilainya, sedangkan `const` nilainya tetap. Jadi "dipakai berulang-ulang" itu benar, tapi "diubah-ubah" hanya berlaku untuk `let` (dan `var`).

# Variabel di JavaScript

Variabel adalah "wadah" untuk menyimpan data. Ada 3 cara membuatnya:

## 1. `let` (nilai bisa diubah)
```javascript
let umur = 20;
umur = 21; // boleh diubah
console.log(umur); // 21
```

## 2. `const` (nilai tetap, tidak bisa diubah)
```javascript
const nama = "Adi";
// nama = "Budi"; // ERROR! const tidak bisa diubah
console.log(nama); // Adi
```

## 3. `var` (cara lama, hindari)
```javascript
var kota = "Ambon";
```
`var` punya perilaku scope yang membingungkan, jadi sekarang jarang dipakai.

## Aturan Penamaan
- Boleh diawali huruf, `_`, atau `$`
- Tidak boleh diawali angka (`1nama` ❌)
- Tidak boleh pakai spasi (`nama saya` ❌)
- Case-sensitive: `nama` dan `Nama` berbeda
- Konvensi umum: **camelCase**, contoh `namaLengkap`

## Tipe Data yang Bisa Disimpan
```javascript
const teks = "Halo";        // string
const angka = 42;           // number
const benar = true;         // boolean
const kosong = null;        // null
const belumAda = undefined; // undefined
const daftar = [1, 2, 3];   // array
const orang = { nama: "Adi", umur: 20 }; // object
```

## Contoh Pemakaian
```javascript
const harga = 15000;
const jumlah = 3;
const total = harga * jumlah;

console.log("Total: Rp" + total);
// atau pakai template literal:
console.log(`Total: Rp${total}`);
```

## Tips Praktis
- **Default-nya pakai `const`**, ganti ke `let` hanya kalau nilainya memang perlu berubah.
- Hindari `var`.
- Beri nama yang jelas: `hargaBarang` lebih baik daripada `x`.

Mau saya jelaskan lanjutan seperti scope (`let` vs `const` di dalam blok/fungsi), atau cara pakai variabel di fungsi dan loop?
