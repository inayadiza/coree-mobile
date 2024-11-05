# Coree Elegante

## Tugas 7
## PApa itu Stateless Widget dan Stateful Widget? Jelaskan perbedaannya.

- **Stateless Widget** : Stateless Widget adalah jenis widget yang tidak memiliki state yang dapat berubah saat aplikasi berjalan. Widget ini statis dan hanya menampilkan data yang sudah ada tanpa perubahan selama runtime. Contoh dari stateless widget adalah `Text` atau `Icon`. Stateless widget cocok untuk elemen-elemen UI yang tidak memerlukan pembaruan.

- **Stateful Widget**: Stateful Widget adalah jenis widget yang memiliki state yang dapat berubah selama aplikasi berjalan. Widget ini lebih dinamis karena mampu menyimpan data dan memperbaruinya berdasarkan interaksi pengguna. Contoh dari stateful widget adalah `Checkbox` atau `TextField`, di mana perubahan dalam interaksi pengguna dapat mempengaruhi tampilan atau data yang ditampilkan.

## 2. Sebutkan widget yang kamu gunakan dalam proyek ini dan fungsinya.

- **MaterialApp**: Menjadi titik masuk aplikasi dan menyediakan tema global untuk aplikasi.
- **ThemeData**: Mengatur tema untuk aplikasi, seperti warna primary dan secondary, serta berbagai properti tema lainnya.
- **Scaffold**: Memberikan struktur dasar aplikasi, termasuk AppBar, Body, dan FloatingActionButton.
- **AppBar**: Menampilkan toolbar di bagian atas aplikasi dengan judul atau ikon.
- **Center**: Mengatur posisi widget di tengah layar.
- **Text**: Menampilkan teks di layar, digunakan untuk memberikan label, judul, atau informasi.
- **Icon**: Menampilkan ikon yang digunakan untuk mempercantik tampilan atau memberikan informasi visual.
- **FloatingActionButton**: Menambahkan tombol aksi floating yang biasanya digunakan untuk melakukan aksi penting dalam aplikasi.

## 3. Apa fungsi dari `setState()`? Sebutkan variabel apa saja yang bisa terpengaruh oleh fungsi tersebut

`setState()` adalah fungsi yang digunakan dalam stateful widget untuk memberi tahu Flutter bahwa ada perubahan pada state yang memerlukan pembaruan tampilan UI. Dengan memanggil `setState()`, Flutter akan merender ulang bagian-bagian yang terpengaruh oleh perubahan tersebut.

Variabel yang terdampak oleh `setState()` adalah variabel yang disimpan dalam kelas stateful widget dan harus diperbarui ketika UI membutuhkan pembaruan. Contoh variabel yang sering terdampak adalah variabel yang menyimpan nilai input pengguna, status tombol, atau data yang diambil dari API.

## Apa Perbedaan antara `const` dan `final` ?

- **const**: Menandakan bahwa nilai dari variabel adalah konstan dan sudah diketahui saat compile time. Semua nilai yang diinisialisasi dengan `const` bersifat immutable dan tidak akan pernah berubah.
  
- **final**: Menandakan variabel yang nilainya hanya dapat diinisialisasi satu kali dan tidak dapat diubah setelahnya. Namun, nilai dari variabel `final` bisa didapatkan saat runtime, tidak harus saat compile time seperti `const`.

## 5. Bagaimana cara kamu mengimplementasikan checklist di atas?

1. Buat proyek Flutter baru dengan nama produk saya yaitu menggunakan perintah `flutter create coree_elegante`, lalu navigasikan ke direktori proyek tersebut dengan `cd coree_elegante`.
2. Jalankan aplikasi Flutter menggunakan `flutter run`, atau jika ingin membukanya di Google Chrome, gunakan perintah `flutter run -d chrome`.
3. Atur skema warna di `main.dart` dengan menggunakan `ColorScheme.fromSwatch`, lalu pilih kombinasi warna biru-hijau, misalnya `Colors.teal` sebagai warna utama dan `Colors.tealAccent` sebagai warna sekunder.
4. Pindahkan widget `MyHomePage` dari `main.dart` ke file baru bernama `menu.dart` di dalam folder `lib`, lalu tambahkan `import 'package:delicate/menu.dart';` di `main.dart`.
5. Deklarasikan variabel `npm`, `name`, dan `className` dalam `MyHomePage` di `menu.dart` untuk menampilkan informasi berupa NPM, nama, dan kelas.
6. Buat widget `InfoCard` di `menu.dart` untuk menampilkan informasi di atas dalam bentuk kartu sederhana.
7. Tambahkan daftar `ItemHomepage` di `menu.dart`, berisi tiga tombol: "Lihat Daftar Produk", "Tambah Produk", dan "Logout".
8. Implementasikan widget `ItemCard` di `menu.dart` untuk menampilkan tombol-tombol tersebut dan buat `SnackBar` yang muncul saat tombol ditekan, menampilkan pesan sesuai tombol yang dipilih.
9. Gunakan `GridView` dan `Row` di `MyHomePage` untuk menampilkan `InfoCard` dan `ItemCard`, mengatur tata letak informasi dan tombol secara rapi.
