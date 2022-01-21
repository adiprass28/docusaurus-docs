---
title: Perkenalan Node.js
---

# Node.js

## Perkenalan Node.js

Sebelum kita memualai membahas tentang Node, ada baiknya kita sudah menginstal Node itu sendiri di dalam komputer kita. Jika belum menginstal bisa mengunjungi situs [Node.js](https://nodejs.org/en/download/).
Sangat disarankan untuk menggunakan versi LTS yang paling terbaru, karna versi tersebut didukung oleh developer Node dalam jangka panjang. Jika menggunakan sistem operasi Ubuntu, maka dapat mengikuti panduan berikut ini pada terminal:
:::info
Saat artikel ini dibuat versi Node LTS yang paling terbaru adalah versi 16.x
:::

```bash
curl -fsSL https://deb.nodesource.com/setup_16.x | sudo -E bash -
sudo apt-get install -y nodejs
```

### Apa itu Node?

Sebelum kehadiran Node, JavaScript hanya memiliki fitur yang terbatas.
Kini Node hadir dengan fitur yang hampir sama dengan bahasa pemograman lain, seperti Python, Java, atu PHP yang dapat _menghandle server-side_. Beberapa fiturnya yaitu:

- Dapat membuat aplikasi Node dengan menggunakan sintaks JavaScript.
- Dapat memanipulasi filesystem, seperti membuat dan menghapus folder.
- Membuat _query databases_ secara langsung.
- Membuat web server menggunakan Node.  
  Javascript dan Node keduanya dapat dieksekusi di dalam web browser, dimana dijalankan di engine yang sama yang disebut _V8 Javascript runtime engine_. Berkat _V8 Engine_ yang ditulis dengan bahasa C++, Javascript dapat _dicompile_ ke _machine code_ dengan cepat, dan mengksekusinya.
  Untuk menggunakan javascript di terminal, ketikkan pada terminal.

```bash
node
```

Setelah itu ketikkan sesuatu yang kita ingin eksekusi dengan menggunakan bahasa javascript, contohnya:

```js title="di terminal"
console.log("Hello World");
```

_Command_ diatas dieksekusi oleh _V8 Engine_ yang bekerja dibalik layar.
Hal yang sama juga dapat kita lakukan didalam web browser kita. Tahapannya yaitu pertama buka Chrome, kemudian buka _control chrome tool_ (titik tiga di pojok kanan atas), kemudian pilih _more tools_, kemudain _developer tools_. Pilih bagian _Console_, kemudian ketikkan kode javascript diatas, lalu jalankan di _console_ tersebut. Disini kita dapat melihat, kode javascript tersebut dapat dijalankan melalui teminal maupun _console_ pada web browser.

### Mengapa menggunakan Node?

Beberapa alasan untuk menggunakan adalah:

- Dengan mempalajari satu bahasa yaitu Javascript, kita dapat menggunakannya dari sisi _frontend_ maupun _backend_.
- Menggunakan teknologi _event-driven_ dan _non-blocking I/O_ yang membuatnya ringan serta efisien.
- Dukungan ekosistem dari Node Package Manager (npm) yang luas serta komunitasnya besar.
