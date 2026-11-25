
# Declaration
# Apa Itu Deklarasi?

**Deklarasi** adalah langkah **membuat variabel dan memberinya nama**, supaya JavaScript tahu bahwa variabel itu ada. Analoginya seperti menyiapkan kotak dan menempelkan label di atasnya, sebelum kamu mengisinya.

```javascript
let umur;
```

Baris ini hanya mendeklarasikan. Kotak bernama `umur` sudah ada, tapi belum ada isinya (nilainya `undefined`).

## Tiga Istilah yang Sering Tertukar

| Istilah | Artinya | Contoh |
|---|---|---|
| **Deklarasi** | Membuat variabel | `let umur;` |
| **Inisialisasi** | Memberi nilai pertama kali | `umur = 20;` |
| **Assignment** | Memberi/mengganti nilai | `umur = 21;` |

Biasanya deklarasi dan inisialisasi digabung dalam satu baris:

```javascript
let umur = 20;
//  ↑ deklarasi   ↑ inisialisasi
```

## Kenapa Harus Dideklarasikan?

Kalau kamu memakai variabel yang belum dideklarasikan, JavaScript tidak tahu itu apa:

```javascript
console.log(nama); // ❌ ReferenceError: nama is not defined
```

Setelah dideklarasikan, barulah bisa dipakai:

```javascript
let nama = "Adi";
console.log(nama); // ✅ "Adi"
```

## Kata Kunci Deklarasi

Deklarasi dilakukan dengan tiga kata kunci yang tadi kita bahas: `var`, `let`, dan `const`.

```javascript
let skor = 0;       // bisa diubah
const PI = 3.14;    // tetap
var lama = "hindari"; // cara lama
```

## Satu Catatan Tambahan

Konsep deklarasi juga berlaku untuk **fungsi**:

```javascript
function sapa() {   // ← function declaration
  console.log("Halo!");
}
```

Tapi untuk sekarang, fokus saja ke deklarasi variabel dulu.

---

# Declaring Variables di JavaScript

Variabel adalah "wadah" untuk menyimpan data. Di JavaScript modern ada tiga cara mendeklarasikannya: `var`, `let`, dan `const`.

## 1. `let`: nilai bisa diubah

```javascript
let umur = 20;
umur = 21; // boleh diubah
console.log(umur); // 21
```

Cocok untuk nilai yang memang akan berubah, seperti counter, skor, atau status.

## 2. `const`: nilai tidak bisa di-assign ulang

```javascript
const nama = "Adi";
nama = "Budi"; // ❌ TypeError: Assignment to constant variable
```

Catatan penting: `const` melarang **re-assignment**, bukan perubahan isi objek/array.

```javascript
const user = { nama: "Adi" };
user.nama = "Budi"; // ✅ boleh, isi objek berubah
user = {};          // ❌ tidak boleh, assign ulang

const list = [1, 2];
list.push(3);       // ✅ boleh
```

## 3. `var`: cara lama (hindari)

```javascript
var kota = "Ambon";
var kota = "Jakarta"; // boleh deklarasi ulang, rawan bug
```

Masalah `var`:
- **Function-scoped**, bukan block-scoped, jadi bocor keluar `if`/`for`
- Bisa dideklarasikan ulang tanpa error
- Perilaku hoisting yang membingungkan

```javascript
if (true) {
  var a = 1;
  let b = 2;
}
console.log(a); // 1 (bocor keluar block)
console.log(b); // ❌ ReferenceError
```

## Perbandingan Singkat

| | `var` | `let` | `const` |
|---|---|---|---|
| Scope | Function | Block | Block |
| Re-assign | ✅ | ✅ | ❌ |
| Re-declare | ✅ | ❌ | ❌ |
| Hoisting | Ya (nilai `undefined`) | Ya (tapi TDZ) | Ya (tapi TDZ) |

**TDZ (Temporal Dead Zone):** `let` dan `const` tidak bisa diakses sebelum baris deklarasinya.

```javascript
console.log(x); // ❌ ReferenceError
let x = 5;
```

## Aturan Penamaan

```javascript
let namaUser = "Adi";     // ✅ camelCase (konvensi umum)
let _private = 1;         // ✅ boleh diawali _ atau $
let $element = 2;         // ✅
let 2nama = "x";          // ❌ tidak boleh diawali angka
let my-var = 1;           // ❌ tidak boleh pakai tanda hubung
let class = 1;            // ❌ kata kunci reserved
```

JavaScript itu **case-sensitive**: `nama` dan `Nama` adalah dua variabel berbeda.

## Deklarasi Tanpa Nilai & Multiple Declaration

```javascript
let hasil;              // undefined
hasil = 100;

let a = 1, b = 2, c = 3; // beberapa sekaligus
```

`const` wajib langsung diberi nilai: `const x;` akan error.

## Best Practice

1. **Default pakai `const`**
2. Pakai `let` hanya kalau nilainya memang perlu berubah
3. **Jangan pakai `var`** di kode baru
4. Beri nama yang deskriptif (`totalHarga`, bukan `th`)

---

Mau lanjut ke topik berikutnya, misalnya **tipe data** (string, number, boolean, null, undefined, dst.) atau **scope & hoisting** lebih dalam? Atau kalau mau, kita bisa latihan soal dulu supaya konsepnya nempel.
