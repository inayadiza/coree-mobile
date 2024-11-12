# Coree Elegante

<details>
<Summary><b>Tugas 7</b></Summary>

## 1. Apa itu Stateless Widget dan Stateful Widget? Jelaskan perbedaannya.

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

## 4. Apa Perbedaan antara `const` dan `final` ?

- **const**: Menandakan bahwa nilai dari variabel adalah konstan dan sudah diketahui saat compile time. Semua nilai yang diinisialisasi dengan `const` bersifat immutable dan tidak akan pernah berubah.
  
- **final**: Menandakan variabel yang nilainya hanya dapat diinisialisasi satu kali dan tidak dapat diubah setelahnya. Namun, nilai dari variabel `final` bisa didapatkan saat runtime, tidak harus saat compile time seperti `const`.

## 5. Bagaimana cara kamu mengimplementasikan checklist di atas?

1. Buat proyek Flutter baru dengan nama produk saya yaitu menggunakan perintah `flutter create coree_elegante`, lalu navigasikan ke direktori proyek tersebut dengan `cd coree_elegante`.
2. Jalankan aplikasi Flutter menggunakan `flutter run`, atau jika ingin membukanya di Google Chrome, gunakan perintah `flutter run -d chrome`.
3. Atur skema warna di `main.dart` dengan menggunakan `ColorScheme.fromSwatch`
4. Pindahkan widget `MyHomePage` dari `main.dart` ke file baru bernama `menu.dart` di dalam folder `lib`, lalu tambahkan `import 'package:coree_elegante/menu.dart';` di `main.dart`.
5. Deklarasikan variabel `npm`, `name`, dan `className` dalam `MyHomePage` di `menu.dart` untuk menampilkan informasi berupa NPM, nama, dan kelas.
6. Buat widget `InfoCard` di `menu.dart` untuk menampilkan informasi di atas dalam bentuk kartu sederhana.
7. Tambahkan daftar `ItemHomepage` di `menu.dart`, berisi tiga tombol: "Lihat Daftar Produk", "Tambah Produk", dan "Logout".
8. Implementasikan widget `ItemCard` di `menu.dart` untuk menampilkan tombol-tombol tersebut dan buat `SnackBar` yang muncul saat tombol ditekan, menampilkan pesan sesuai tombol yang dipilih.
9. Gunakan `GridView` dan `Row` di `MyHomePage` untuk menampilkan `InfoCard` dan `ItemCard`, mengatur tata letak informasi dan tombol secara rapi.
</details>

<details>
<Summary><b>Tugas 8</b></Summary>

## 1. Apa kegunaan const di Flutter? Jelaskan apa keuntungan ketika menggunakan const pada kode Flutter. Kapan sebaiknya kita menggunakan const, dan kapan sebaiknya tidak digunakan?

**Keuntungan Menggunakan `const`:**
- Efisiensi memori: Objek konstan disimpan hanya sekali di memori
- Performa rendering yang lebih baik: Widget `const` dapat di-cache dan tidak perlu di-rebuild

**Kapan Menggunakan `const`?**
- Literal widget (Text, Icon, Container)
- Objek immutable (warna, ukuran, style)
- Variabel konstan (URL API, konfigurasi)

**Kapan Tidak Menggunakan `const`?**
- Objek mutable (nilai berubah-ubah)
- Komputasi kompleks
- Konteks yang berbeda (objek hanya berguna dalam konteks tertentu)
 
## 2. Jelaskan dan bandingkan penggunaan Column dan Row pada Flutter. Berikan contoh implementasi dari masing-masing layout widget ini!

**`Column`**
- Menyusun anak-anak widget secara vertikal, dari atas ke bawah
- Berguna untuk menyusun elemen bertumpuk (judul, deskripsi, tombol)

Contoh implementasi `Column`:

```dart
Column(
  children: [
    Text('Ini Judul'),
    SizedBox(height: 16.0),
    Text('Ini Deskripsi'),
    SizedBox(height: 16.0),
    ElevatedButton(
      onPressed: () { /* aksi */ },
      child: Text('Klik Saya'),
    ),
  ],
)
```

**`Row`**
- Menyusun anak-anak widget secara horizontal, dari kiri ke kanan 
- Berguna untuk menyusun elemen berdampingan (ikon, teks)

Contoh implementasi `Row`:

```dart
Row(
  children: [
    Icon(Icons.arrow_back),
    SizedBox(width: 8.0),
    Text('Kembali'),
  ],
)
```

**Perbedaan**
- `Column` untuk layout vertikal, `Row` untuk layout horizontal
- `Column` untuk elemen bertumpuk, `Row` untuk elemen berdampingan
- Dapat digabungkan untuk membuat layout kompleks (grid, kartu)

## 3. Jelaskan dan bandingkan penggunaan Column dan Row pada Flutter. Berikan contoh implementasi dari masing-masing layout widget ini!

1. **TextField**
   - Digunakan untuk menerima input teks dari pengguna.
   - Memiliki banyak opsi kustomisasi seperti hint text, input formatters, dan validasi.

2. **NumberField**
   - Digunakan untuk menerima input angka dari pengguna.
   - Merupakan turunan khusus dari TextField dengan format input angka.

Selain elemen-elemen di atas, Flutter juga menyediakan elemen input lain yang mungkin tidak saya gunakan pada tugas kali ini, seperti:
- **Dropdown** : Bisa digunakan untuk memilih satu opsi dari daftar.
- **Checkbox/Switch** : Digunakan untuk menerima input boolean (ya/tidak) dari pengguna.
- **RadioButton**: Digunakan untuk memilih satu opsi dari beberapa pilihan.
- **Slider**: Digunakan untuk memilih nilai dalam rentang tertentu.
- **RangeSlider**: Digunakan untuk memilih rentang nilai.
- **FileInput**: Digunakan untuk memilih file dari penyimpanan perangkat.

## 4. Bagaimana cara kamu mengatur tema (theme) dalam aplikasi Flutter agar aplikasi yang dibuat konsisten? Apakah kamu mengimplementasikan tema pada aplikasi yang kamu buat?
1. Mendefinisikan tema global pada `main.dart` menggunakan `ThemeData`
   - Mengatur warna, tipografi, dan gaya visual yang konsisten

2. Menggunakan komponen dari `Theme.of(context)` saat membangun widget
   - Memastikan konsistensi tema pada seluruh aplikasi

3. Menerapkan tema khusus pada widget tertentu jika diperlukan
   - Membungkus widget dalam `Theme` widget

Dengan implementasi tema yang konsisten, aplikasi Flutter saya memiliki tampilan dan gaya visual yang selaras di seluruh aplikasi.

## 5. Bagaimana cara kamu menangani navigasi dalam aplikasi dengan banyak halaman pada Flutter?
1. Menggunakan `Navigator` sebagai stack untuk mengelola perpindahan antar halaman
2. Mendefinisikan rute-rute halaman pada `main.dart`
3. Menggunakan `Navigator.pushNamed(context, routeName)` untuk berpindah ke halaman baru
4. Menggunakan `Navigator.pop(context)` untuk kembali ke halaman sebelumnya
5. Menambahkan Drawer untuk navigasi cepat antar halaman
</details>



