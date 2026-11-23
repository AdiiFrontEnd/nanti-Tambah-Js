# Coment
Komentar adalah teks yang diabaikan oleh engine JS, dipakai untuk menjelaskan kode, menandai TODO, atau menonaktifkan kode sementara.
## 1. Komentar satu baris `//`
```js
// Ini komentar satu baris
let umur = 20; // Bisa juga di akhir baris kode
```

## 2. Komentar multi-baris `/* ... */`

```js
/*
  Ini komentar
  yang panjang
  beberapa baris
*/
function hitung(a, b) {
  return a + b;
}
```

Catatan: komentar `/* */` **tidak bisa di-nesting** (bersarang):

```js
/* luar /* dalam */ ini sudah keluar dari komentar */  // ❌ error
```

## 3. Komentar dokumentasi (JSDoc)

Ditulis dengan `/** ... */`. Editor seperti VS Code memakainya untuk autocomplete dan tooltip.

```js
/**
 * Menjumlahkan dua angka.
 * @param {number} a - Angka pertama
 * @param {number} b - Angka kedua
 * @returns {number} Hasil penjumlahan
 */
function tambah(a, b) {
  return a + b;
}
```

## 4. Menonaktifkan kode sementara

```js
// console.log("debug");
console.log("aktif");
```

Shortcut di VS Code: `Ctrl + /` (satu baris) atau `Shift + Alt + A` (blok).

## 5. Tag komentar yang umum dipakai

```js
// TODO: tambahkan validasi input
// FIXME: bug saat array kosong
// NOTE: fungsi ini dipanggil dari modul auth
```

## 6. Hashbang (kasus khusus)

Di file Node.js yang dieksekusi langsung, baris pertama boleh berupa:

```js
#!/usr/bin/env node
```

## Tips komentar yang baik

- Jelaskan **kenapa**, bukan **apa**. Kode sudah menunjukkan apa yang terjadi.
  ```js
  // ❌ Buruk: menambah 1 ke i
  i++;

  // ✅ Bagus: lewati header baris pertama CSV
  i++;
  ```
- Jangan biarkan komentar usang. Komentar yang salah lebih berbahaya daripada tidak ada komentar.
- Jangan menumpuk kode lama yang di-comment; Git sudah menyimpan riwayatnya.
- Beri nama variabel dan fungsi yang jelas supaya komentar tidak perlu terlalu banyak.

Mau lanjut ke bagian mana? Misalnya JSDoc lebih dalam, kebiasaan komentar di proyek nyata, atau topik JS lainnya.
