# Assignment Operator

Assignment operator adalah operator yang dipakai untuk **memberi (menyimpan) nilai ke sebuah variabel**. Tanda dasarnya `=`, tapi bukan "sama dengan" seperti di matematika. Artinya: *hitung sisi kanan, lalu simpan hasilnya ke sisi kiri*.

```js
let x = 10;   // x sekarang berisi 10
x = x + 5;    // hitung x + 5 (= 15), simpan lagi ke x
```

## Compound Assignment (Operator Gabungan)

Gabungan operasi aritmatika/bitwise dengan assignment, supaya penulisan lebih singkat.

| Operator | Contoh | Sama dengan |
|---|---|---|
| `=` | `x = 5` | simpan 5 ke x |
| `+=` | `x += 3` | `x = x + 3` |
| `-=` | `x -= 3` | `x = x - 3` |
| `*=` | `x *= 3` | `x = x * 3` |
| `/=` | `x /= 3` | `x = x / 3` |
| `%=` | `x %= 3` | `x = x % 3` (sisa bagi) |
| `**=` | `x **= 2` | `x = x ** 2` (pangkat) |

## Contoh Praktis

```js
let skor = 100;
skor += 20;   // 120
skor -= 10;   // 110
skor *= 2;    // 220
skor /= 4;    // 55
skor %= 10;   // 5
```

String juga bisa:

```js
let teks = "Halo";
teks += " Dunia";  // "Halo Dunia"
```

## Assignment Operator Lanjutan (JavaScript)

Selain di atas, ada operator logika yang berguna untuk otomasi/scripting:

```js
let a = null;
a ??= "default";  // isi hanya jika a null/undefined -> "default"

let b = 0;
b ||= 10;         // isi jika b falsy (0, "", false, null) -> 10

let c = 5;
c &&= 99;         // isi hanya jika c truthy -> 99
```

## Hal yang Sering Bikin Bingung

**1. `=` vs `==` vs `===`**

```js
x = 5;     // assignment (memberi nilai)
x == 5;    // perbandingan (longgar)
x === 5;   // perbandingan (ketat, cek tipe juga)
```

**2. Assign berantai**

```js
let a, b, c;
a = b = c = 7;  // ketiganya jadi 7 (dievaluasi dari kanan ke kiri)
```

**3. Destructuring assignment**

```js
const [p, q] = [1, 2];          // p = 1, q = 2
const { nama, umur } = { nama: "Adi", umur: 20 };
[p, q] = [q, p];                // tukar nilai tanpa variabel bantu
```

**4. Objek/array itu referensi**

```js
const arr1 = [1, 2];
const arr2 = arr1;   // bukan salinan, tapi menunjuk ke array yang sama
arr2.push(3);
console.log(arr1);   // [1, 2, 3]
```

## Catatan Antar Bahasa

- **Python**: sama (`+=`, `-=`, dst), plus walrus operator `:=` (assign di dalam ekspresi).
- **C/Java**: sama, plus `<<=`, `>>=`, `&=`, `|=`, `^=`.
- Python tidak punya `++`/`--`, jadi pakai `x += 1`.

Mau lanjut ke bahasa tertentu (JS, Python, C++), atau mau saya buatkan latihan soal untuk menguji pemahamannya?
