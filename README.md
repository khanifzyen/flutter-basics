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
