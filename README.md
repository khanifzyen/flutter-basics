# Flutter Basics

Materi Mata Kuliah Pemrograman Mobile | Teknik Informatika UNISNU Jepara | Akhmad Khanif Zyen

Di Modul ini, kita akan berkenalan dengan flutter basic, seperti bagaimana kita membuat project flutter, memahami struktur foldernya, struktur codenya dan juga akan membahas salah satu bagian dari flutter yaitu stateless widget dan stateful widget.

## Membuat Project Flutter

Dalam membuat project flutter ada 2 cara:

1. Menggunakan terminal/cmd,
2. Menggunakan IDE (VS Code,Android Studio

### 1. Menggunakan Terimal

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
