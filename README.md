# Synchronous-vs-Asynchronous

Penjelasan Synchronous
Synchronous adalah situasi ketika dua atau lebih aktivitas atau proses berlangsung secara bersamaan dalam waktu nyata (real-time).

Penjelasan Asynchronous
Asynchronous merupakan bentuk komunikasi yang berlangsung secara tertunda atau tidak langsung melalui media digital, seperti email, forum diskusi, dan dokumen daring. Proses ini tidak terikat oleh rentang waktu yang kaku serta memiliki kecepatan transmisi data yang bervariasi.

Perbedaan Synchronous dan Asynchronous
Pendekatan sinkron dan asinkron memiliki perbedaan mendasar pada pola penyampaian materi, interaksi pengajar dan peserta, serta tingkat fleksibilitas waktu.

Waktu Interaksi
Synchronous: Mengandalkan komunikasi langsung secara serempak di waktu yang sama, misalnya melalui perkuliahan tatap muka, diskusi video langsung, atau kelas virtual.
Asynchronous: Memberikan kebebasan kepada peserta untuk mempelajari materi, mengerjakan tugas, dan berdiskusi kapan saja sesuai ketersediaan waktu masing-masing.

Waktu dan Tempat
Synchronous: Terikat pada waktu dan tempat yang telah dijadwalkan. Peserta wajib hadir tepat waktu serta memerlukan koneksi internet yang stabil.
Asynchronous: Menawarkan fleksibilitas lokasi dan jadwal. Peserta dapat mengakses materi dan berpartisipasi dalam diskusi dari mana saja selama terhubung ke platform pembelajaran.

Interaksi dan Respon
Synchronous: Pertukaran informasi terjadi secara langsung sehingga tanggapan dan tanggapan balik dapat diperoleh secara real-time.
Asynchronous: Peserta memiliki kesempatan untuk memahami materi terlebih dahulu sebelum merespons. Meskipun jawaban tidak didapatkan seketika, peserta dapat menyusun tanggapan secara lebih matang.

Tingkat Keterlibatan
Synchronous: Mendorong keterlibatan aktif karena adanya interaksi langsung dan diskusi yang dinamis di waktu nyata.
Asynchronous: Membutuhkan inisiatif dan kemandirian peserta yang lebih tinggi, namun fleksibilitas waktu membantu peserta mengatur ritme belajar secara mandiri.

Contoh Penerapan

Synchronous (Waktu Nyata)
Interaksi berlangsung secara serempak meskipun para peserta berada di tempat berbeda.

Contoh: Rapat daring via Zoom/Google Meet, panggilan telepon, percakapan pesan instan (live chat), dan kelas fisik tatap muka.

Kelebihan: Umpan balik didapatkan secara instan dan diskusi terasa lebih dinamis.

Kekurangan: Terikat jadwal yang ketat dan membutuhkan koneksi internet yang stabil.

Asynchronous (Tidak Serempak)
Interaksi dilakukan secara bertahap atau tertunda tanpa mengharuskan semua pihak aktif di saat bersamaan.

Contoh: Pengiriman email, mengakses modul/video di LMS, berdiskusi di forum daring, dan pembaruan tugas di aplikasi manajemen proyek (seperti Trello atau Notion).

Kelebihan: Waktu sangat fleksibel serta mendukung pembelajaran mandiri.

Kekurangan: Respons jawaban bisa tertunda dan membutuhkan kedisiplinan tinggi.

Tiga Cara Menulis Kode Asynchronous di JavaScript

JavaScript menyediakan tiga pendekatan utama untuk mengelola proses asinkron:

Callback
Callback adalah fungsi yang dikirimkan sebagai argumen ke fungsi lain dan akan dipanggil kembali setelah proses utama selesai dijalankan.

Contoh penulisan:

function ambilData(callback) {
setTimeout(() => {
callback("Data berhasil diambil");
}, 2000);
}

ambilData(function(data) {
console.log(data);
});

Promise
Promise merupakan fitur yang diperkenalkan pada ES6 untuk mengelola proses asinkron secara lebih terstruktur dibandingkan callback.

Contoh penulisan:

const data = new Promise((resolve, reject) => {
setTimeout(() => {
resolve("Data berhasil diambil");
}, 2000);
});

data
.then((hasil) => {
console.log(hasil);
})
.catch((error) => {
console.log(error);
});

Async/Await
Fitur dari ES8 ini menyederhanakan penulisan Promise agar terlihat menyerupai kode sinkron. Fungsi berlabel async secara otomatis mengembalikan Promise.

Contoh penulisan:

function ambilData() {
return new Promise((resolve) => {
setTimeout(() => {
resolve("Data berhasil diambil");
}, 2000);
});
}

async function tampilkanData() {
const hasil = await ambilData();
console.log(hasil);
}

tampilkanData();
