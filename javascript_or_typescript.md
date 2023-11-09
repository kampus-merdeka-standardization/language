# Introduction
**TypeScript** adalah superset dari JavaScript, yang berarti TypeScript mencakup semua aspek JavaScript dengan penambahan fitur-fitur khusus yang memungkinkan pengembangan aplikasi skala besar dengan lebih efisien.

Pada tahun 2012, TypeScript diperkenalkan ke publik dengan tujuan utama untuk mengatasi keterbatasan yang ada pada JavaScript. Microsoft, dalam mengembangkan TypeScript, ingin meningkatkan kemampuan dan fleksibilitas bahasa ini untuk pengembangan aplikasi yang lebih kompleks dan robust. Rilis pertama TypeScript (versi 0.8) diperkenalkan pada Oktober 2012.

**Referensi**:

- [Apa Itu TypeScript? Kelebihan TypeScript, dan Perbedaannya - Caraguna](https://caraguna.com/apa-itu-typescript/)
- [Sejarah Lengkap JavaScript, TypeScript, dan Node.js - ICHI.PRO](https://ichi.pro/id/sejarah-lengkap-javascript-typescript-dan-node-js-38930825526926)


# Comparation

## Pros & Cons Typescript
| Kelebihan                                              | Kekurangan                                                    |
|--------------------------------------------------------|---------------------------------------------------------------|
| Penyelesaian kode yang sangat baik | Keamanan tidak dijamin pada saat runtime |
| Dukungan untuk adopsi bertahap    | TypeScript menambah kompleksitas ekstra, bahkan untuk tugas-tugas sederhana|
| Integrasi library pihak ketiga yang lebih baik| Pesan kesalahan bisa sulit untuk diuraikan|
| Tipe yang disediakan oleh komunitas| Kinerja build dapat terpengaruh        |
| Keamanan tipe yang lebih baik: TypeScript menyediakan pengetikan statis, yang berarti Anda dapat menangkap kesalahan pada saat waktu kompilasi alih-alih waktu runtime|                                                               |

Referensi:
- [LogRocket Blog: Understanding TypeScript’s benefits and pitfalls](https://blog.logrocket.com/understanding-typescripts-benefits-and-pitfalls-24c1e02b3e9c/)
- [Ablison: Pros And Cons Of Typescript 2023](https://www.ablison.com/pros-and-cons-of-typescript-2023/)


## Pros & Cons Php

Berikut adalah tabel yang diperbarui untuk kelebihan dan kekurangan PHP dengan referensi di akhir:

| Kelebihan                                       | Kekurangan                   |
|-------------------------------------------------|------------------------------|
| Gratis dan open-source      | Dapat menurun popularitasnya|
| Dapat diunduh dan digunakan di mana saja untuk acara atau aplikasi web| Sintaks yang tidak konsisten|
| Platform-independent: aplikasi PHP dapat berjalan di berbagai OS seperti UNIX, Linux, Windows, dll.| Alat debugging yang buruk|
| library yang luas              | Masalah keamanan seperti XSS, SQL Injection, dan Session hacking|
| Dapat disesuaikan dengan berbagai platform dan teknologi| Masalah dan bug tidak dapat diatasi dengan cepat|
| Dukungan komunitas yang kuat   | Harus menulis banyak kode untuk membangun aplikasi|
| Pemeliharaan yang lebih mudah   |                              |
| Pilihan spesialis yang tersedia dalam jumlah besar|       |
| Kecepatan pemuatan yang meningkat|                            |
| Seleksi database yang luas      |                              |
| Fleksibilitas yang baik         |                              |
| Kompatibilitas dengan layanan cloud|                          |
| Dapat diskalakan                |                              |

Referensi:
- [GeeksforGeeks: Advantages and Disadvantages of PHP](https://www.geeksforgeeks.org/advantages-and-disadvantages-of-php/)
- [Softjourn: Why Use PHP in 2023? Advantages and Disadvantages](https://softjourn.com/en/blog/why-use-php-2023-advantages-and-disadvantages)
- [EPAM: Advantages and Disadvantages of PHP Programming Language](https://anywhere.epam.com/business/pros-and-cons-of-php)
- [Unstop: Advantages And Disadvantages Of PHP: Why Should You Use PHP?](https://unstop.com/php-pros-cons/)
- [CHTips: Advantages and Disadvantages of PHP | Pros and Cons of PHP](https://www.chtips.com/php/advantages-and-disadvantages-of-php)

## Pros & Cons Python
| Kelebihan                                      | Kekurangan                                                     |
|------------------------------------------------|----------------------------------------------------------------|
| Mudah dipelajari dan digunakan| Masalah kecepatan dan performa                 |
| library yang luas        | Kurang mendukung komputasi mobile             |
| Versatil (berbagai kegunaan)  | Akses database yang kurang dikembangkan      |
| Produktivitas yang meningkat  | Kesalahan runtime karena tipe data dinamis    |
| Portabilitas (dapat berjalan di berbagai platform)|                                                                |
| Bahasa yang diinterpretasikan (memudahkan debugging)|                                                               |
| Cocok untuk pemula         |                                                                |
| Sintaks yang mudah dibaca  |                                                                |

Referensi:
- [ScanSkill: Python Programming Language: Pros & Cons](https://scanskill.com/backend/python/python-what-are-the-benefits-and-downsides-of-the-programming-language/)
- [PixelCrayons: Pros and Cons of Python Programming Language](https://www.pixelcrayons.com/blog/web/pros-and-cons-of-python-programming-language/)
- [Python Geeks: Advantages of Python | Disadvantages of Python](https://pythongeeks.org/advantages-disadvantages-python/)

# Installation
Tentu! Berikut adalah beberapa contoh tambahan yang mencakup langkah-langkah instalasi TypeScript dan Node.js pada sistem operasi yang berbeda, serta cara membuat dan menjalankan program TypeScript sederhana.

### 1. Instalasi pada Ubuntu:

#### Instalasi Node.js:
```bash
sudo apt update
sudo apt install nodejs npm
```

#### Instalasi TypeScript:
```bash
sudo npm install -g typescript
```

### 2. Instalasi pada Windows:

#### Instalasi Node.js:
- Unduh installer Node.js dari [situs web resmi](https://nodejs.org/).
- Jalankan installer dan ikuti petunjuk di layar.

#### Instalasi TypeScript:
Buka Command Prompt atau PowerShell, lalu jalankan:
```bash
npm install -g typescript
```

### 3. Membuat Program TypeScript Sederhana:

3.1. Buat file dengan ekstensi `.ts`, misalnya `hello.ts`, dan buka dengan editor teks pilihan Anda.
3.2. Tulis kode berikut di dalam file `hello.ts`:
```typescript
function sayHello(name: string) {
    console.log("Hello, " + name + "!");
}

sayHello("World");
```
3.3. Simpan file, lalu buka terminal atau command prompt dan navigasikan ke direktori tempat file `hello.ts` disimpan.
3.4. Kompilasi file TypeScript ke JavaScript dengan menjalankan perintah berikut:
```bash
tsc hello.ts
```
Ini akan menghasilkan file `hello.js`.

3.5. Sekarang, jalankan file JavaScript yang dikompilasi dengan Node.js:
```bash
node hello.js
```
Anda seharusnya akan melihat output: `Hello, World!`

### 4. Instalasi pada macOS:

#### Instalasi Node.js:
- Anda bisa menggunakan Homebrew untuk menginstal Node.js dengan perintah:
```bash
brew install node
```

#### Instalasi TypeScript:
```bash
npm install -g typescript
```

Dengan langkah-langkah ini, Anda seharusnya bisa menginstal Node.js dan TypeScript di sistem operasi yang berbeda dan juga membuat dan menjalankan program TypeScript sederhana.

# Convention Code

## File

### Benar:
- Nama file harus menggunakan kebab-case dan memiliki ekstensi `.ts`, seperti `hello-world.ts`.
- Setiap file harus memiliki satu tujuan atau tanggung jawab.

### Salah:
- Menggunakan nama file dengan spasi atau karakter khusus lainnya seperti `Hello World.ts`.

## Variable

### Benar:
- Gunakan camelCase untuk nama variabel:
```typescript
let myVariableName: string;
```

### Salah:
- Menggunakan nama variabel dengan huruf besar atau underscore:
```typescript
let MyVariableName: string;
let my_variable_name: string;
```

## Fungsi

### Benar:
- Gunakan camelCase untuk nama fungsi dan berikan tipe kembali yang jelas:
```typescript
function addNumbers(a: number, b: number): number {
    return a + b;
}
```

### Salah:
- Menggunakan nama fungsi dengan huruf besar atau tidak memiliki tipe kembali:
```typescript
function AddNumbers(a, b) {
    return a + b;
}
```

## Const

### Benar:
- Gunakan UPPERCASE untuk konstanta dan pisahkan kata dengan underscore:
```typescript
const MAX_LIMIT: number = 100;
```

### Salah:
- Menggunakan camelCase atau kebab-case untuk konstanta:
```typescript
const maxLimit: number = 100;
const max-limit: number = 100;
```

## Object

### Benar:
- Gunakan camelCase untuk objek:
```typescript
let person = {
    firstName: "John",
    lastName: "Doe"
};
```

### Salah:
- Menggunakan huruf besar atau underscore untuk kunci objek:
```typescript
let person = {
    First_Name: "John",
    Last_Name: "Doe"
};
```

Tentu, berikut adalah perincian yang disederhanakan untuk penamaan kelas, interface, dan tipe:

## Class, Interface, dan Type (Tipe)

### Benar:
- Gunakan PascalCase (huruf kapital di awal setiap kata) untuk penamaan kelas, interface, dan tipe:
```typescript
class UserAccount {
    // ...
}

interface IUserProfile {
    // ...
}

type UserCredentials = {
    // ...
};
```

### Salah:
- Menggunakan camelCase (huruf kecil di awal kata pertama dan huruf kapital di awal kata berikutnya) atau huruf kecil untuk penamaan kelas, interface, dan tipe:
```typescript
class userAccount {
    // ...
}

interface iUserProfile {
    // ...
}

type userCredentials = {
    // ...
};
```


## Comment

### Benar:
- Gunakan komentar untuk menjelaskan kode yang kompleks atau tidak jelas:
```typescript
// Ini adalah fungsi untuk menambahkan dua angka
function add(a: number, b: number): number {
    return a + b;
}
```

### Salah:
- Menulis komentar yang tidak berguna atau jelas:
```typescript
// Menambahkan a dan b
function add(a: number, b: number): number {
    return a + b;
}
```

## Error Handling

### Benar:
- Gunakan blok `try-catch` untuk menangani kesalahan:
```typescript
try {
    let result = riskyFunction();
} catch (error) {
    console.error(error);
}
``` 

### Salah:
- Mengabaikan kesalahan atau tidak menanganinya:
```typescript
let result = riskyFunction();  // jika terjadi kesalahan, tidak ada penanganannya
```