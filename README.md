# Flutter Basics

Materi Mata Kuliah Pemrograman Mobile | Teknik Informatika UNISNU Jepara | Akhmad Khanif Zyen

Di Modul ini, kita akan berkenalan dengan flutter basic, seperti bagaimana kita membuat project flutter, memahami struktur foldernya, struktur codenya dan juga akan membahas salah satu bagian dari flutter yaitu stateless widget dan stateful widget.

## Membuat Project Flutter

Dalam membuat project flutter ada 2 cara:

1. Menggunakan terminal/cmd,
2. Menggunakan IDE (VS Code,Android Studio)

### 1. Menggunakan Terminal

Pertama buka dulu terminalnya, lalu ketikan perintah:

```bash
flutter create project_flutter_pertama
```

![Gambar 1. create project flutter menggunakan terminal](img/01%20flutter%20create.png)

Gambar 1. create project flutter menggunakan terminal

Ingat aturan dalam membuat nama project adalah:

- Semua huruf kecil
- Bila terdapat lebih dari 1 kata, dihubungkan dengan karakter underscore

### 2. Menggunakan VS Code

Klik

- Windows : ctrl + shift + P
- Mac: command + shift + P

Lalu pilih, Flutter: New Project

Kemudian enter, pilih folder penyimpanan, lalu ketikan nama project flutter nya: project_flutter_pertama

![Gambar 2. Flutter New Project dari VS Code](img/02%20flutter%20new%20project.PNG)

Gambar 2. Flutter New Project dari VS Code

## Membuka Project Flutter

Untuk cara pertama, untuk membuka project ke visual studio code, maka pertama kita perlu masuk dulu ke folder projectnya dengan perintah:

```bash
cd project_flutter_pertama
```

Setelah itu ketik perintah:

```bash
code .
```

Lalu enter

Untuk cara kedua, otomatis folder project flutter akan terbentuk dan dibuka oleh vscode

![Gambar 3. Flutter terbuka di VS Code](img/03%20flutter%20open%20vs%20code.PNG)

Gambar 3. Flutter terbuka di VS Code

## Menjalankan Aplikasi Flutter

Untuk menjalankan aplikasi Flutter di sistem operasi android menggunakan emulator, kita perlu memastikan dulu apakah android sdk sudah terinstall di laptop kita. Cara cek nya adalah dengan mengetikan perintah berikut pada terminal:

```bash
flutter doctor -v
```

![Gambar 4. Android Toolchain error](img/04%20flutter%20doctor%20error.PNG)

Gambar 4. Android Toolchain error di dalam perintah flutter doctor

Bila android toolchain belum centang hijau, ada beberapa langkah yang perlu dilakukan. Langkahnya sebagai berikut:

### 1. Download Android Studio dan Install

Software android studio bisa anda download dari link dibawah. Setelah selesai download, lalu install. Android studio disini akan menjadi tools untuk me manage android emulator. https://developer.android.com/studio

![Gambar 5. Download Android Studio](img/05%20android%20studio%20download.PNG)

Gambar 5. Download Android Studio

### 2. Buka Android Studio

Setelah android studio dibuka, klik More Actions lalu klik virtual device manager.

![Gambar 6 Android Studio -  Virtual Device Manager](img/06%20android%20studio%20avd.png)

Gambar 6 Android Studio - Virtual Device Manager

### 3. Pilih Device

Selanjutnya kita diminta untuk memasukan tipe phone

![Gambar 7. Add Device - Select Hardware](img/07%20avd%20add%20device.PNG)

Gambar 7. Add Device - Select Hardware

### 4. Pilih System Image

Setelah itu pilih system image Android. Download bila belum pernah download. Pastikan internet lancar karena akan download file yang besar. Next sampai Virtual Device terbentuk.

![Gambar 8. Pilih System Image](img/08%20choose%20system%20image.PNG)

Gambar 8. Pilih System Image

### 5. Masuk Android Studio, Klik More Actions, Pilih SDK Manager

![Gambar 9. SDK Manager](img/09%20sdk%20manager.png)

Gambar 9. SDK Manager

### 6. Pilih Tab SDK Tools, centang Android SDK Command-line

Kemudian setelah berhasil download, kembali ke terminal kembali untuk check apakah android sdk nya siap untuk di konsumsi.

![Gambar 10. Android Command-line tools](img/10%20command-line%20tools.png)

### 7. Menerima Lisensi Android

Jalankan perintah

```bash
flutter doctor --android-licenses
```

Selanjutnya ketik y enter sampai selesai

![Gambar 11. Android Licenses Accepted](img/11%20accept%20android%20licenses.PNG)

Gambar 11. Android Licenses Accepted

### 8. Buka Project yang Sudah Dibuat dengan VS Code

Disini kita akan melihat struktur folder dan pilihan device yang akan kita gunakan.

1. Buka lib/main.dart terlebih dahulu

2. kemudian pilih Device di toolbar (default Windows), nanti akan muncul daftar emulator.

3. Pilih salah satu emulator.

![Gambar 12. Pilih Emulator](img/12%20choose%20avd.png)

Gambar 12. Pilih Emulator

### 9. Pilih Device dan Run aplikasi

Setelah memilih device, kita dapat lanjut dengan cara klik menu Run dilanjut button run without debugging

![Gambar 13. Run Without Debuggnig](img/13%20run%20without%20debugging.png)

Gambar 13. Run Without Debugging

### 10. Aplikasi berhasil dijalankan

Selanjutnya bila tidak ada problem, maka aplikasi akan tampil di emulator yang sebelumnya sudah kita pilih.

![Gambar 14. Aplikasi Berjalan](img/14%20aplikasi%20berjalan.png)

Gambar 14. Aplikasi Berjalan

## Penjelasan File dan Folder Bawaan Flutter

Setelah project terbentuk, kita akan melihat banyak folder dan file yang sudah dibuatkan oleh flutter. Yuk kita bahas file dan folder folder yang sudah di generate tersebut.

![Gambar 15. Struktur Folder Project Flutter](img/15%20struktur%20folder.PNG)

Gambar 15. Struktur Folder Project Flutter

Folder, android, ios, linux, macos, web, dan windows adalah folder yang sudah disiapkan khusus oleh flutter supaya aplikasi yang kita buat bisa di jalankan di platform tersebut.

Disini nanti folder platform yang paling penting adalah folder android karena dalam case program flutter engineering kali ini kita hanya akan fokus pada
development aplikasi android.

Folder android sendiri adalah folder yang penting karena didalamnya berisi project android lengkap dimana kita dapat membuatnya tanpa flutter, namun disini nanti flutter sdk akan menggabungkan kode flutter kita ke project android, jadi ketika kode flutter kita dikompilasi ke kode asli, pada dasarnya kode asli itu nanti akan disuntikkan ke dalam folder android untuk menjadi aplikasi asli android.

Dan untuk itu kita tidak begitu perlu merubah apapun di folder ini, dan sangat jarang sekali kita merubah kecuali ada beberapa penyesuaian konfigurasi yang berkaitan dengan update version dan sebagainya. Ini akan dibahas di materi selanjutnya.

![Gambar 16. Struktur folder .dart_tools dan .idea](img/15%20struktur%20folder%20dart_tool%20dan%20idea.PNG)

Gambar 16. Struktur folder .dart_tools dan .idea

Folder .idea ini menyimpan beberapa konfigurasi untuk android studio. Karena kita nantinya tidak menggunakan android studio untuk editornya, maka kita tidak butuh untuk mengubah apapun di dalam
folder ini.

Folder .dart_tool sendiri berisi konfigurasi dart package yang di generate oleh flutter. Folder ini pun tidak perlu kita ubah-ubah. Dapat kita abaikan terlebih dahulu.

![Gambar 17. Struktur folder build](img/16%20struktur%20folder%20buiild.PNG)

Gambar 17. Struktur folder build

Folder build ini akan penting karena folder ini nantinya
akan menampung output dari aplikasi flutter kita.
Contoh file .apk, .abb, .ipa, .exe hasil build ke tiap
platform nanti akan berada di folder ini.

![Gambar 18. Struktur folder lib](img/18%20struktur%20folder%20lib.PNG)

Gambar 18. Struktur folder lib

Folder lib ini sangat penting bagi kita karena 99% pekerjaan kita nantinya akan dilakukan di folder ini.

Lib sendiri adalah singkatan dari library dan itu artinya kode dart dan flutter yang kita tulis di dalam lib akan diartikan sebagai library yang akan disuntikan ke dalam kode asli tiap tiap platform.

Jadi folder ini adalah tempat kita menambah semua file dart dan tempat kita menulis kode.

![Gambar 19. Struktur folder test](img/19%20struktur%20folder%20test.PNG)

Gambar 19. Struktur folder test

Folder test untuk saat ini belum terlalu penting, didalam folder ini kita dapat menuliskan test untuk kode kita, yang nantinya dapat dijalankan secara otomatis. Salah satu fungsinya adalah ketika kita ada perubahan yang berkaitan kode yang pernah kita tulis test nya, dan ada impact, maka unit test ini akan memastikan apakah impact itu bermasalah apa tidak.

Ini tentu penting ketika kita mengembangkan aplikasi yang sudah terlalu kompleks.

![Gambar 20. Struktur file project flutter](img/20%20struktur%20file.PNG)

Gambar 20. Struktur file project flutter

.gitignore berisi list folder atau file yang tidak akan ikut masuk kedalam git repository ketika kita push ke repository tersebut.

.metadata file ini untuk melacak properties di dalam project flutter, ini berfungsi sebagai alat flutter dalam menilai kemampuan dan peningkatan dan sebagainya, file ini tidak perlu diapa-apakan.

.analysis_options.yaml berisi konfigurasi untuk melihat statistik analisis kode dart untuk mengecek error, warning, dan linter. Tidak perlu kita apa-apa kan.

Config.json berisi konfigurasi tambahan ketika kita ingin run aplikasi untuk pertama kalinya di dalam proses development.

Project_flutter_pertama.iml file yang dikelola oleh flutter sdk dalam mengelola dipedensi internal dan beberapa pengaturan project. Ini file yang tidak perlu kita ubah.

![Gambar 21. Struktur file pubspec.yaml](img/21%20struktur%20file%20pubspec%20yaml.PNG)

Gambar 21. Struktur file pubspec.yaml

Pubspec.yml merupakan file yang akan sering kita gunakan. File ini yang memungkinan kita untuk mengelola sebagian besar dependensi project kita.

Apa artinya ini?

Artinya anda dapat mengkonfigurasi package pihak ketiga kedalam project kita dan dan semua fiturnya dapat langsung kita pakai.

Kita juga dapat mengkonfigurasi beberapa hal lain disini, seperti misalnya font yang ingin kita pakai, atau gambar yang ingin kita import dari asset. Jadi file ini adalah file yang akan sering kita ubah untuk urusan konfigurasi project.

![Gambar 22. Struktur file pubspec.lock dan README.md](img/22%20struktur%20file%20pubspec%20lock%20dan%20readme%20md.PNG)

Gambar 22. Struktur file pubspec.lock dan README.md

Pubspec.lock adalah file yang dihasilkan secara otomatis berdasarkan file .yaml, dan ini hanya menyimpan lebih banyak detail tentang semua dependensi yang kita miliki di project flutter kita. Namun ini file yang bukan kita kerjakan.

README.md ini bisa kita abaikan, bisa juga kita isi sebagai informasi tentang project yang sedang kita bangun. Jadi file ini dapat kita ubah sebagai informasi yang dapat berguna baik developer lain yang berhubungan dengan project flutter ini.

## Flutter Basic Widget

![Gambar 23. Contoh Flutter App](img/23%20contoh%20flutter%20app.PNG)

Gambar 23. Contoh Flutter App

Sebelum mulai membuat layout tampilan aplikasi, sebaiknya kita pahami dulu bagaimana flutter bekerja mengelola berbagai widget menjadi tampilan aplikasi yang tersusun rapi.

![Gambar 24. function main](img/24%20function%20main.PNG)

Gambar 24. function main

Dalam project flutter, kita mempunya main function seperti halnya dart. function ini tidak memiliki kembalian dan tidak memerlukan argument.

Seperti yang pernah kita pelajari, main adalah function yang secara otomatis dijalankan ketika aplikasi mulai dijalankan oleh flutter dan dart. Karena ada di file main.dart, kita tidak boleh mengganti namanya.

![Gambar 25. Struktur Widget](img/25%20struktur%20widget.PNG)

Gambar 25. Struktur Widget

Untuk merubah kode menjadi tampilan dilayar, pertama kita perlu memahami, pada dasarnya tampilan dilayar itu adalah sekumpulan widget.

Flutter adalah tentang widget, dan setiap aplikasi yang kita buat hanya sekumpulan widget dan widget adalah blok penyusun UI yang dapat kita lihat di layar. Lihat yang saya kotakin merah, itu semua adalah widget. Jika disatukan di dalam satu widget, akan menjadi tampilan yang sesuai dengan kebutuhan UI.

Widget juga sering berisi widget lain, seperti list daftar yang berisi daftar item. Seperti yang kita lihat di samping, dimana list navigation bar berisi widget item navigation bar.

Jadi sesungguhnya kita membuat aplikasi flutter kita ini menjadi widget tree, yang memiliki root widget dimana ini merupakan keseluruhan aplikasi kita.

Sehingga apa yang kita lihat di layar adalah widget yang menampung widget lain.

![Gambar 26. Class Widget](img/25%20class%20widget.PNG)

Gambar 26. Widget MyApp

Karena semua yang ada di flutter adalah widget, yuk sekarang waktunya kita membuat widget kita sendiri.

Untuk membuat widget kita perlu membuat class widget adalah object, dan kita memerlukan class untuk membuat object.

Jadi mari lihat class MyApp baris 7 diatas. Ini adalah contoh class yang nantinya akan menjadi object widget.

![Gambar 27. Class StatelessWidget](img/27%20extends%20statelesswidget.PNG)

Gambar 27. Class StatelessWidget

Sekarang yang kita lihat adalah MyApp hanya menjadi sebuah class. Sedangkan widget yang benar-benar dapat kita lihat di layar bukanlah hal sepele untuk dibuat, karena pada akhirnya setiap pixel pada layar perlu kita kontrol.

Disinilah tugas flutter. Flutter sudah memiliki fungsi-fungsi tersebut dibalik layar, jadi kita tidak perlu menulisnya sendiri. Kita hanya perlu menggunakan fitur yang disebut pewarisan (inheritance).

Ini artinya kita akan membangun di atas class dasar, mendapatkan semua fitur dari class dasar tersebut dan hanya akan menambahkan fitur baru didalamnya.

Cara pewarisan class yang sudah dibuat oleh flutter adalah dengan menambahkan kata kunci extends setelah nama class dan sebelum kurung kurawal dan memberitahu dart bahwa class ini akan mewarisi class lain dan kita hanya dapat memperluas atau mewarisi satu class dalam satu waktu.

![Gambar 28. Pubspec.yaml](img/28%20pubspec%20yaml.PNG)

Gambar 28. pubspec.yaml

Terus bagaimana bisa kita menggunakan class dan library yang telah disediakan oleh flutter, jawabannya ada di pubspec.yaml.

Di file ini, kita dapat melihat bahwa dependencies pertama yang secara default dibuat ketika membuat project flutter adalah dependencies ke sdk flutter. Dimana sdk ini letak nya ada di folder lain di luar project
ini

![Gambar 29. Menambahkan dependency](img/29%20menambahkan%20dependency.PNG)

Gambar 29. Menambahkan dependency

Dengan adanya dependencies sdk flutter, kita dapat menggunakan semua class class nya kedalam project kita untuk kita perluas lagi dengan cara meng extends class class tersebut.

Di file ini pulalah nantinya kita dapat mendaftarkan package-package lain yang sudah disediakan oleh flutter ataupun yang dibuat oleh dev lain sudah di publish sebagai library yang dapat kita lihat di pub.dev

Dalam penulisan package, perhatikan spasi, harus sejajar dengan packages flutter line 33.

![Gambar 30. Method build](img/30%20method%20build.PNG)

Gambar 30. Method build

Setelah kita membuat class widget yang meng extends class stateless widget. Ada method yang wajib kita implement yaitu `build(BuildContex context)`

Method ini wajib mengembalikan widget karena disini kita bekerja dengan widget flutter, seluruh aplikasi kita adalah widget.

`BuildContext` sendiri adalah object khusus yang sudah disediakan oleh flutter lewat material.dart, dimana dia akan selalu membawa informasi meta tentang widget tersebut yang akan diteruskan ke build widget selanjutnya, dan informasi tersebut dapat digunakan oleh widget tree selanjutnya.

Dalam contoh diatas widget build mengembalikan widget `MaterialApp()`

![Gambar 31. Property home pada widget MaterialApp](img/31%20property%20home.PNG)

Gambar 31. Property home pada widget MaterialApp

Class widget kita yang kita beri nama MyApp membutuhkan kembalian berupa widget juga. Dan disini saya akan menggunakan widget MaterialApp untuk kembaliannya. MaterialApp ini adalah widget yang sudah disediakan oleh flutter melalui class
material.dart.

MaterialApp ini memiliki beberapa argumen yang dapat kita gunakan, janis argumennya adalah named argument. Seperti contoh disamping, saya menggunakan argument home untuk memasukan widget text yang bertuliskan Coding Flutter ke dalam widget MaterialApp yang nantinya akan diteruskan ke widget tree MyApp lalu di eksekusi dengan runApp dan akhirnya bisa tampil dilayar.

![Gambar 31. Function RunApp](img/31%20runApp.png)

Gambar 31. Function RunApp

Untuk menyambungkan widget yang kita buat sampai dengan tampil dilayar, kita akan butuh function yang sudah disediakan oleh flutter melalui material.dart nya yaitu runApp().

runApp sendiri function yang disediakan oleh flutter untuk menjalankan aplikasi flutter setelah aplikasi android atau ios di-boot. Alurnya dia akan mencoba mengambil widget tree yang kita buat, dan menggambarnya ke layar yang didasarkan pada widget tree tersebut. Jadi disini dia akan menggambar text Coding Flutter ke layar.

MyApp didalam runApp harus berupa function dengan cara memberinya kurung buka kurung tutup, karena tanpa itu, MyApp akan hanya menjadi tipe data.

![Gambar  32. Running App](img/32%20coding%20flutter.png)

Gambar 32. Running App

Ketika di running aplikasi flutter kita, tampilannya akan
seperti ini.

Dalam tahap ini kita baru memperlihatkan bagaimana text Coding Flutter yang sebelumnya berupa string, sekarang bisa tampil dilayar. Belum memperdulikan tampilan layar yang indah karena belum menambahkan widget lain selain widget Text().

Dari hasil yang kita lihat, ini membuktikan bahwa fungsi dasar berjalan baik. Dengan alur widget MyApp yang kita buat dengan tambahan fitur yang disediakan oleh widget stateless berupa method build() diterima oleh fungsi utama untuk menjalankan aplikasi dengan bantuan runApp.

![Gambar  33. Widget Scaffold](img/33%20scaffold.PNG)

Gambar 33. Widget Scaffold

Untuk mendapatkan tampilan yang lebih indah, kita dapat menggunakan widget lain yang sudah disediakan oleh flutter yaitu widget scaffold. Widget ini mempunyai beberapa argument, yang sering digunakan adalah argument appBar dan body.

Disamping saya contohkan untuk menambahkan widget scaffold yang saya masukan kedalam argument home yang ada di MaterialApp, lalu di dalam scaffold terdapat appBar. Ini yang nantinya akan menjadi tampilan di bagian anah layar. Lalu terdapat juga body, ini nanti berisi content yang ingin kita kelola.

![Gambar 34. Aplikasi berjalan](img/34%20aplikasi%20berjalan.png)

Gambar 34. Aplikasi berjalan

Hasil ketika kita jalankan akan seperti yang ada di atas ini.

Terdapat appbar dengan title Coding Flutter, lalu untuk body nya sendiri masih berupa text dengan Text
Coding Flutter bersama Teknik Informatika.

Setelah ini kita akan belajar mengenal widget, ada widget yang visible dan invisible. Maksudnya bagaimana yuk lanjut ke bab selanjutnya.

![Gambar 35. Visible dan invisible widget](img/35%20visible%20dan%20invisible%20widget.PNG)

Gambar 35. Visible dan invisible widget

Di bab sebelumnya sudah mengenal widget text, dimana hasilnya itu dapat dilihat dalam berupa text di layar.
Diatas saya beri ilustrasi bahwa widget itu ada yang terlihat dan ada juga yang tidak terlihat. Baik yang terlihat maupun yang tidak terlihat kedua nya sama-sama penting.

Widget yang terlihat akan memberikan UI dan UX yang baik bagi user. User dapat berinteraksi dengan aplikasi. Untuk widget yang tidak nampak seperti listview, column, row, ini adalah widget-widget penting yang fungsinya untuk mengatur widget tree supaya widget yang nampak dapat disusun dengan rapi.

## Stateless Widget

![Gambar 36. Diagram stateless widget](img/36%20diagram%20statelesswidget.PNG)

Gambar 36. Diagram stateless widget

Sebelum kita masuk ke stateless stateful pertama perlu tahu apa itu state ?

State adalah data atau informasi yang digunakan aplikasi atau widget dalam aplikasi kita.

State sendiri terbagi menjadi 2, yaitu app state dan local state. Stateless dan stateful ini masuk ke dalam local state.

Stateless sendiri widget yang tidak memiliki state, sehingga perubahan dan hasil render UI nya itu ditentukan oleh inputan yang masuk kedalam stateless widget tersebut.

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
        title: 'Flutter Demo',
        theme: ThemeData(
          primarySwatch: Colors.blue,
        ),
        home: Scaffold(
          appBar: AppBar(
            title: const Text('Coding Flutter'),
          ),
          body: const ShowTextWidget(
              text: 'Belajar Coding Flutter bersama Teknik Informatika UNISNU'),
        ));
  }
}

class ShowTextWidget extends StatelessWidget {
  final String text;
  const ShowTextWidget({super.key, required this.text});

  @override
  Widget build(BuildContext context) {
    return Text(text);
  }
}
```

Seperti kode yang kita lihat di atas ini. Class ShowTextWidget ini extends ke StatelessWidget yang artinya UI akan dirender ketika class ini dipanggil oleh widget lain dengan inputan berupa string text. Jadi dia tidak memiliki state sendiri di dalam dirinya.

## Stateful Widget

![Gambar 37. Diagram Stateful Widget](img/37%20diagram%20statefullwidget.PNG)

Gambar 37. Diagram Stateful Widget

Untuk stateful dia adalah widget yang memiliki state didalamnya. Sehingga class yang meng extends class statefulwidget, akan dapat memiliki internal state nya sendiri, hal ini dapat menguntungkan karena render UI nya tidak hanya bergantung dari inputan dari widget lain, namun dengan memanggil setState maka widget build akan re-run ulang dengan state yang baru tanpa harus menunggu perubahan di widget tree atas nya.

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
        title: 'Flutter Demo',
        theme: ThemeData(
          primarySwatch: Colors.blue,
        ),
        home: Scaffold(
          appBar: AppBar(
            title: const Text('Coding Flutter'),
          ),
          body: const ChangeTimeWidget(),
        ));
  }
}

class ChangeTimeWidget extends StatefulWidget {
  const ChangeTimeWidget({super.key});

  @override
  State<ChangeTimeWidget> createState() => _ChangeTimeWidgetState();
}

class _ChangeTimeWidgetState extends State<ChangeTimeWidget> {
  DateTime time = DateTime.now();

  @override
  Widget build(BuildContext context) {
    return Column(
      children: [
        Text('Jam Sekarang: $time'),
        ElevatedButton(
          onPressed: () {
            setState(() {
              time = DateTime.now();
            });
          },
          child: const Text('Perbarui Waktu'),
        ),
      ],
    );
  }
}
```

Seperti class ChangeTextWidget di atas ini, dimana dia meng extends class StatefulWidget. Untuk susunan class nya seperti diatas. Class ini memiliki variable time dan valuenya dapat diganti ketika klik button, setelah itu text akan di set ulang menggunakan DateTime.now(), karena terdapat setState di situ, maka widget build akan di run ulang yang akhirnya menciptakan tampilan baru dengan data yang baru. Berikut hasilnya bila kita running dan klik button Perbarui Waktu.

![Gambar 38. Contoh StatefulWidget](img/38%20example%20statefulwidget.png)

Gambar 38. Contoh Tampilan Aplikasi Menggunakan StatefulWidget

> **Tugas Latihan 1**
>
> 1. Bagaimana cara membuat project Flutter menggunakan terminal/cmd?
> 2. Apa aturan dalam memberikan nama project pada Flutter?
> 3. Apa saja folder yang secara khusus disiapkan oleh Flutter untuk menjalankan aplikasi pada platform tertentu?
> 4. Apa fungsi dari folder .dart_tools dan .idea?
> 5. Bagaimana cara membuka project Flutter menggunakan Visual Studio Code?
> 6. Mengapa kita perlu memastikan Android SDK terinstall untuk menjalankan aplikasi Flutter di sistem operasi Android?
> 7. Apa langkah-langkah untuk mengatasi masalah "Android Toolchain error" pada perintah flutter doctor?
> 8. Bagaimana cara menambahkan Android SDK Command-line tools melalui Android Studio?
> 9. Apa fungsi dari file .gitignore dalam struktur folder Flutter?
> 10. Mengapa file pubspec.yaml sangat penting dalam pengembangan aplikasi Flutter?
> 11. Apa yang dimaksud dengan widget dalam konteks Flutter?
> 12. Bagaimana pewarisan (inheritance) digunakan dalam pembuatan widget Flutter?
> 13. Apa peran widget MaterialApp dalam pembuatan aplikasi Flutter?
> 14. Mengapa kita membutuhkan fungsi runApp untuk menjalankan aplikasi Flutter?
> 15. Apa kegunaan widget Scaffold dalam struktur aplikasi Flutter?
> 16. Bagaimana cara menambahkan app bar dan body pada widget Scaffold?
> 17. Apa perbedaan antara Stateless Widget dan Stateful Widget?
> 18. Mengapa Stateful Widget disebut memiliki state internal?
> 19. Berikan contoh penggunaan Stateless Widget dalam pembuatan aplikasi Flutter.
> 20. Berikan contoh penggunaan Stateful Widget dalam pembuatan aplikasi Flutter beserta alasan penggunaannya.
