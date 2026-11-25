
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

Sudah kebayang bedanya deklarasi dan inisialisasi? Kalau mau, saya kasih beberapa soal latihan kecil untuk mengetesnya.
