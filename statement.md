# Statement
Apapun Perintah Yang Berdiri Sendiri Adalah Statement

Berikut Adalah Percakapan Gw Dengan AI

Question :

Jadi Apa itu statement?


**Statement (pernyataan) adalah satu instruksi lengkap dalam kode yang dijalankan oleh JavaScript.**

Anggap saja seperti satu kalimat dalam bahasa manusia. Satu kalimat menyampaikan satu maksud lengkap, begitu juga satu statement memberi satu perintah lengkap ke komputer.

```js
let nama = "Adi";       // statement: buat variabel
console.log(nama);      // statement: tampilkan ke layar
if (nama) { ... }       // statement: ambil keputusan
```

Poin pentingnya:

- **Satu statement = satu instruksi.** Kumpulan statement disebut program.
- **Dijalankan berurutan** dari atas ke bawah.
- **Jenisnya beragam**: bisa mendeklarasikan sesuatu (`let`), mengatur alur (`if`, `for`, `return`), atau menjalankan ekspresi (`console.log()`).
- **Biasanya diakhiri `;`**, seperti titik di akhir kalimat.

Singkatnya: **statement adalah satu langkah perintah yang dipahami dan dijalankan JavaScript.**



Question

Gw Masih Belum Ngerti



Oke, coba kita pakai analogi yang lebih konkret. Lupakan istilah teknis dulu.

**Bayangin resep masak.**

```
1. Panaskan minyak
2. Masukkan bawang
3. Aduk 2 menit
4. Matikan api
```

Tiap baris itu satu perintah. Nah, **statement itu sama kayak satu baris perintah di resep itu**, cuma ditulis buat komputer.

```js
let nama = "Adi";        // perintah 1: simpan kata "Adi" ke wadah bernama nama
console.log(nama);       // perintah 2: tampilkan isi wadah nama ke layar
```

Komputer baca dari atas ke bawah, jalanin perintah satu per satu. Satu perintah = **satu statement**.

**Intinya cuma ini:**

> Statement = satu perintah yang kamu tulis, dan komputer jalankan.

Gak lebih ribet dari itu. Jenis-jenisnya (`if`, `for`, `let`) cuma variasi perintahnya:

- `let x = 5;` → "simpan angka 5 dengan nama x"
- `console.log(x);` → "tampilkan x"
- `if (x > 3) {...}` → "kalau x lebih dari 3, lakukan ini"

Semuanya tetap sama: **satu perintah**.

> Question

```
function jumlahkan(data) {
    let total = 0;
    for (const nilai of data) {
        total += nilai;
    }
    return total;
}
```
Kalo INI 5?
Hampir, tapi hitungannya **4 statement** kalau dihitung semuanya, atau **5 kalau function-nya ikut dihitung**. Jadi tebakan kamu bisa benar, tergantung kamu menghitung `function` sebagai statement atau bukan.

Ini rinciannya:

```js
function jumlahkan(data) {      // 1: function declaration
    let total = 0;              // 2: deklarasi variabel
    for (const nilai of data) { // 3: for...of
        total += nilai;         // 4: expression statement
    }
    return total;               // 5: return
}
```

Ternyata hitungannya **5**, jadi tebakan kamu **benar**. Maaf, kalimat pembuka gw tadi bikin bingung. Hitungan yang tepat:

1. `function jumlahkan(data) { ... }` (deklarasi fungsi)
2. `let total = 0;`
3. `for (const nilai of data) { ... }`
4. `total += nilai;`
5. `return total;`

**Catatan soal hitungannya:**

- `const nilai` di dalam kurung `for...of` **bukan statement terpisah**, cuma bagian dari header `for`, sama kayak kasus `index` tadi.
- Kalau mengikuti spesifikasi resmi, `function` itu *declaration*, bukan statement. Tapi untuk belajar, wajar dihitung sebagai statement, jadi jawabannya 5.

Jadi: **5, benar.**


> question

jadi Apapun Perintah Yang Berdiri Sendiri Adalah statement?

Statement itu **satu perintah lengkap yang ditulis di baris kode, dan dijalankan komputer.**

Anggap kode itu resep masak, dan tiap langkah di resep adalah satu statement.

```js
let nama = "Adi";        // statement: simpan "Adi" ke wadah bernama nama
console.log(nama);       // statement: tampilkan isinya
if (nama) {              // statement: kalau nama ada isinya...
    console.log("ada");  // statement di dalam if
}
```

**Cara ngenalinnya:**

1. Dia satu perintah yang **lengkap** (bisa dijalankan komputer sebagai satu langkah).
2. Dia ditulis di posisi **baris kode**, bukan cuma potongan di dalam kurung statement lain.

**Yang bukan statement** adalah potongan yang jadi bagian dari statement lain:

```js
let hasil = 2 + 3;   // 1 statement. "2 + 3" cuma bagian di dalamnya (expression)
```

Jadi: **statement = satu langkah perintah. Kumpulan statement = program.**

Kalau masih terasa kabur, coba ini: gw kasih satu baris kode, terus kamu bilang itu statement atau bukan. Mau coba?
