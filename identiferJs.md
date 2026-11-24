# Identifier
Identifier Adalah Sebuah Nama Yang Kita Berikan Pada Sebuah Variabel,Fungsi,class DLL

---
Ayo kita bahas! Identifier di JavaScript adalah **nama** yang kamu berikan ke variabel, fungsi, kelas, properti, dan sebagainya. Variabel itu sendiri adalah wadah bernama untuk menyimpan nilai.

---
## Aturan Penamaan Identifier

Sebuah identifier valid kalau:

- Diawali huruf (`a-z`, `A-Z`), underscore (`_`), atau tanda dolar (`$`)
- Karakter berikutnya boleh huruf, angka, `_`, atau `$`
- **Tidak** boleh memakai reserved word (`if`, `for`, `class`, `return`, dll.)
- Bersifat **case-sensitive**: `nama`, `Nama`, dan `NAMA` adalah tiga identifier berbeda

```javascript
let nama = "Adi";        // valid
let _private = 1;        // valid
let $el = null;          // valid
let user2 = "x";         // valid

let 2user = "x";         // ❌ tidak boleh diawali angka
let my-name = "x";       // ❌ tanda hubung tidak boleh
let class = "x";         // ❌ reserved word
```

## Cara Mendeklarasikan Variabel

Ada tiga kata kunci: `var`, `let`, dan `const`.

| | `var` | `let` | `const` |
|---|---|---|---|
| Scope | function | block | block |
| Bisa diubah nilainya | ya | ya | tidak |
| Bisa dideklarasi ulang | ya | tidak | tidak |
| Hoisting | ya (nilai `undefined`) | ya (tapi kena TDZ) | ya (tapi kena TDZ) |

```javascript
const PI = 3.14;     // nilai tetap
let umur = 20;       // bisa berubah
umur = 21;           // OK

var lama = "jangan dipakai lagi";
```

**Rekomendasi praktis:** pakai `const` sebagai default, pakai `let` kalau nilainya memang perlu berubah, dan hindari `var`.

## Scope Singkat

```javascript
if (true) {
  let a = 1;
  var b = 2;
}
console.log(b); // 2  (var bocor keluar blok)
console.log(a); // ❌ ReferenceError (let terkurung di blok)
```

## Hoisting dan TDZ

```javascript
console.log(x); // undefined (var di-hoist)
var x = 5;

console.log(y); // ❌ ReferenceError: Temporal Dead Zone
let y = 5;
```

## Konvensi Penamaan

- **camelCase** untuk variabel dan fungsi: `namaLengkap`, `hitungTotal()`
- **PascalCase** untuk class: `UserAccount`
- **UPPER_SNAKE_CASE** untuk konstanta: `MAX_RETRY`
- Beri nama yang bermakna: `totalHarga` lebih baik daripada `x`

## Catatan Penting: `const` dan Objek

`const` mencegah **penugasan ulang**, bukan perubahan isi.

```javascript
const user = { nama: "Adi" };
user.nama = "Budi";   // OK, isi objek boleh berubah
user = {};            // ❌ TypeError, tidak boleh diganti objek lain
```

---
