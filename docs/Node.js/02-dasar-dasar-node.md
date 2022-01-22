---
title: Dasar-Dasar Node
---

## Dasar-dasar _Module_

Kali ini kita akan membahas bagaimana cara untuk menggunakan _module_, yang mana memanfaatkan _function_ yang ada di Node yaitu `require()`.
Terlebih dahulu buat folder untuk tempat menyimpan projek, sebagai contoh kita namakan `catatan-node` dan buat file `app.js`

```bash title="terminal"
mkdir catatan-node
cd catatan node
```

### Penggunaan `require()` untuk menggunakan _built-in module_

Kita dapat daftar komplit mengenai _built-in module_ di Node.js API.  
Untuk contoh kali ini kita akan menggunakan **File System** _module_ untuk membuat file baru dan **OS** _module_ yang memungkinkan kita mengambil hal-hal seperti nama pengguna.

Kita mulai dengan membuat file dan juga menambahkan teks didalamnya, kita akan menggunakan [fs.appendFileSync](https://nodejs.org/dist/latest-v16.x/docs/api/fs.html#fsappendfilesyncpath-data-options).
Pertama-tama untuk dapat menggunakan `fs.appendFileSync` kita perlu menuliskan

```js title="catatan-node/app.js"
const fs = require("fs");
```

Setelah menuliskan kode tersebut kita dapat mengakses seluruh _function_ yang tersedia pada _fs module_.  
Selanjutnya kita akan membuat file `sambutan.txt` dan menambahkan teks `hello world!` pada file tersebut, dengan menuliskan kode berikut:

```js title="app.js" {3}
const fs = require("fs");

fs.appendFileSync("sambutan.txt", "hello world!");
```

Untuk lebih memahami _function_ `require()`, kita akan mencoba _built-in module_ yang kedua yaitu **OS** _module_. Kita akan menggunakan [`os.userInfo([options])`](https://nodejs.org/dist/latest-v16.x/docs/api/os.html#osuserinfooptions) sebagai contoh.

```js title="app.js" {2,4-5}
const fs = require("fs");
const os = require("os");

let user = os.userInfo();
console.log(user);

fs.appendFileSync("sambutan.txt", "hello world!");
```

Dengan menulis `const os = require("os")` kita dapat memanggil _methods_ yang tersedia pada OS _module_.  
Kita membuat variabel baru `let user = os.userInfo()` yang mana kita dapat memanggil _userInfo_.  
Untuk dapat melihat isi dari variabel user di _console_ dengan cara menuliskan `console.log(user)`.

Kita dapat menuliskan operator `+` untuk menambahkan _string_ lain.

```js title="app.js" {6}
const fs = require("fs");
const os = require("os");

let user = os.userInfo();

fs.appendFileSync("sambutan.txt", "hello " + user.username + "!");
```

Pertama-tama kita hapus terlebih dahulu kata `world` lalu ganti dan hubungkan dengan `user.username`.  
Sekarang kita jalankan kode tersebut di terminal, kemudian buka file sambutan.txt maka akan terlihat seperti ini

```txt title="sambutan.txt"
Hello world! Hello world! Hello adiprass!
```

Cara kedua untuk menukar kata `world` dengan `user.username` adalah dengan menggunakan fitur ES6 yang diketahui sebagai _template string_. _Template string_ diawali dan diakhiri dengan operator \` (tick)
Untuk meletakkan variabel Javascript kedalam _template string_ kita perlu menggunakan `$` (dollar) yang diikuti dengan dengan buka dan tutup kurung kurawa ({}).

```js title="app.js" {6}
const fs = require("fs");
const os = require("os");

let user = os.userInfo();

fs.appendFileSync("sambutan.txt", `Hello ${user.username}`);
```

Jika kamu menjalankan kode tersebut, pada `sambutan.txt` akan menambahkan kalimat

```txt title="sambutan.txt"
Hello world! Hello world! Hello adiprass!
Hello adiprass!
```
