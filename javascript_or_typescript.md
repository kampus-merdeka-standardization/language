# Introduction

**TypeScript** adalah superset dari JavaScript, yang berarti TypeScript mencakup semua aspek JavaScript dengan penambahan fitur-fitur khusus yang memungkinkan pengembangan aplikasi skala besar dengan lebih efisien.

Pada tahun 2012, TypeScript diperkenalkan ke publik dengan tujuan utama untuk mengatasi keterbatasan yang ada pada JavaScript. Microsoft, dalam mengembangkan TypeScript, ingin meningkatkan kemampuan dan fleksibilitas bahasa ini untuk pengembangan aplikasi yang lebih kompleks dan robust. Rilis pertama TypeScript (versi 0.8) diperkenalkan pada Oktober 2012.

# Comparation

## Pros & Cons Typescript

| Kelebihan                                              | Kekurangan                                                    |
|--------------------------------------------------------|---------------------------------------------------------------|
| Penyelesaian kode yang sangat baik | Keamanan tidak dijamin pada saat runtime |
| Dukungan untuk adopsi bertahap    | TypeScript menambah kompleksitas ekstra, bahkan untuk tugas-tugas sederhana|
| Integrasi library pihak ketiga yang lebih baik| Pesan kesalahan bisa sulit untuk diuraikan|
| Tipe yang disediakan oleh komunitas| Kinerja build dapat terpengaruh        |
| Keamanan tipe yang lebih baik: TypeScript menyediakan pengetikan statis, yang berarti Anda dapat menangkap kesalahan pada saat waktu kompilasi alih-alih waktu runtime|                                                               |

# Installation

## 1. Instalasi pada Ubuntu:

### Instalasi Node.js:

```bash
sudo apt update
sudo apt install nodejs npm
```

### Instalasi TypeScript:

```bash
sudo npm install -g typescript
```

## 2. Instalasi pada Windows:

### Instalasi Node.js Windows:

- Unduh installer Node.js dari [situs web resmi](https://nodejs.org/).
- Jalankan installer dan ikuti petunjuk di layar.

### Instalasi TypeScript Windows:

Buka Command Prompt atau PowerShell, lalu jalankan:

```bash
npm install -g typescript
```

## 3. Instalasi pada macOS:

### Instalasi Node.js macOS:

- Anda bisa menggunakan Homebrew untuk menginstal Node.js dengan perintah:

```bash
brew install node
```

### Instalasi TypeScript macOS:

```bash
npm install -g typescript
```

Dengan langkah-langkah ini, Anda seharusnya bisa menginstal Node.js dan TypeScript di sistem operasi yang berbeda dan juga membuat dan menjalankan program TypeScript sederhana.

# Convention Code

## Table Comparison

## Conclusion

| Kategori | Penulisan | Pemilihan Kata |
| --- | --- | --- |
| File name | kebab-case | kata benda |
| Variable name | camelCase | kata benda |
| Function name | camelCase | kata kerja |
| Constant name | UPPERCASE | kata benda |
| Object key | camelCase | kata benda |
| Class | PascalCase | kata benda |
| Interface | PascalCase | kata benda |
| Type name | PascalCase | kata benda |

## File

### Benar:

- Nama file harus menggunakan kebab-case dan memiliki ekstensi `.ts`, seperti `hello-world.ts`.
- Setiap file harus memiliki satu tujuan atau tanggung jawab, biasanya mengikuti kata benda, misalnya `user-service.ts`.

### Salah:

- Menggunakan nama file dengan spasi atau karakter khusus lainnya seperti `Hello World.ts`.

## Variable

### Benar:

- Gunakan camelCase untuk nama variabel, biasanya kata benda atau frasa kata benda:

```typescript
let userName: string;
```

### Salah:

- Menggunakan nama variabel dengan huruf besar atau underscore:

```typescript
let UserName: string;
let user_name: string;
```

## Fungsi

### Benar:

- Gunakan camelCase untuk nama fungsi. Fungsi biasanya mengikuti kata kerja atau frasa kata kerja dan berikan tipe kembali yang jelas:

```typescript
function calculateArea(width: number, height: number): number {
    return width * height;
}
```

### Salah:

- Menggunakan nama fungsi dengan huruf besar atau tidak memiliki tipe kembali:

```typescript
function CalculateArea(width, height) {
    return width * height;
}
```

## Const

### Benar:

- Gunakan UPPERCASE untuk konstanta dan pisahkan kata dengan underscore. Konstanta sering kali adalah kata benda:

```typescript
const DEFAULT_COLOR: string = "blue";
```

### Salah:

- Menggunakan camelCase atau kebab-case untuk konstanta:

```typescript
const defaultColor: string = "blue";
const default-color: string = "blue";
```

## Object

### Benar:

- Gunakan camelCase untuk objek dan propertinya, biasanya kata benda atau frasa kata benda:

```typescript
let orderDetails = {
    itemId: "B123",
    quantity: 2,
    pricePerUnit: 39.95
};
```

### Salah:

- Menggunakan huruf besar atau underscore untuk kunci objek:

```typescript
let Order_Details = {
    Item_ID: "B123",
    Quantity: 2,
    Price_Per_Unit: 39.95
};
```

## Class, Interface, dan Type (Tipe)

### Benar:

- Gunakan PascalCase untuk penamaan kelas, interface, dan tipe, biasanya menggunakan kata benda atau frasa kata benda yang menjelaskan entitas atau konsep:

```typescript
class UserAccount {
    // ...
}

interface UserProfile {
    // ...
}

type UserCredentials = {
    // ...
};
```

### Salah:

- Menggunakan camelCase atau huruf kecil untuk penamaan kelas, interface, dan tipe:

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

- Gunakan komentar untuk menjelaskan kode yang kompleks atau tidak jelas. Komentar biasanya merupakan frasa atau kalimat yang menjelaskan logika atau fungsi kode:

```typescript
// Menghitung dan mengembalikan area dari sebuah persegi panjang
function calculateRectangleArea(width: number, height: number): number {
    return width * height;
}
```

### Salah:

- Menulis komentar yang tidak berguna atau jelas, atau yang hanya mengulangi apa yang sudah jelas dari kode:

```typescript
// Menambahkan width dan height
function calculateRectangleArea(width: number, height: number): number {
    return width * height;
}
```

## Error Handling

### Benar:

- Gunakan blok `try-catch` untuk menangani kesalahan dan memberikan komentar yang menjelaskan penanganan jika perlu:

```typescript
try {
    // Mencoba menjalankan fungsi yang berisiko
    let result = riskyFunction();
} catch (error) {
    // Menangkap dan mencatat kesalahan
    console.error(error);
}
```

### Salah:

- Mengabaikan kesalahan atau tidak menanganinya dengan benar, atau tidak memberikan komentar yang cukup jika penanganan kompleks:

```typescript
let result = riskyFunction();  // Kesalahan tidak ditangani
```

## API Documentation

### Swagger

Untuk pengembangan backend node.js wajib membuat dan mencantumkan swagger agar para pengembang dan reviewer dapat melihat dokumentasi API yang dituju.

Berikut adalah contoh menggunakan Swagger untuk framework NestJS:

1. **Instalasi Paket Swagger**: Pertama, Anda perlu menginstal paket `@nestjs/swagger`.

    ```bash
    npm install --save @nestjs/swagger
    ```

2. **Impor Modul Swagger**: Setelah paket terinstal, impor `SwaggerModule` dan `DocumentBuilder` ke dalam aplikasi NestJS Anda.

    ```javascript
    import { SwaggerModule, DocumentBuilder } from '@nestjs/swagger';
    ```

3. **Konfigurasi Dokumentasi**: Buat instance baru dari kelas `DocumentBuilder` untuk mengonfigurasi properti dasar dokumentasi Swagger Anda, seperti judul, deskripsi, dan versi.

    ```javascript
    const config = new DocumentBuilder()
      .setTitle('My NestJS API')
      .setDescription('The API description')
      .setVersion('1.0')
      .addTag('my-api')
      .build();
    ```

4. **Menghasilkan Dokumen Swagger**: Gunakan instance `DocumentBuilder` untuk menghasilkan dokumen Swagger untuk aplikasi NestJS Anda.

    ```javascript
    const document = SwaggerModule.createDocument(app, config);
    ```

5. **Mounting Swagger UI**: Terakhir, mount Swagger UI ke aplikasi NestJS Anda.

    ```javascript
    SwaggerModule.setup('api', app, document);
    ```

Setelah menyelesaikan langkah-langkah ini, Anda dapat melihat dokumentasi Swagger Anda di `http://localhost:<PORT>/api`. 

ini hanyalah contoh untuk framework NestJS, untuk penggunaan di framework lainnya diharapkan cek dokumentasi resmi.

## Referensi

- [Apa Itu TypeScript? Kelebihan TypeScript, dan Perbedaannya - Caraguna](https://caraguna.com/apa-itu-typescript/)
- [Sejarah Lengkap JavaScript, TypeScript, dan Node.js - ICHI.PRO](https://ichi.pro/id/sejarah-lengkap-javascript-typescript-dan-node-js-38930825526926)
- [LogRocket Blog: Understanding TypeScript’s benefits and pitfalls](https://blog.logrocket.com/understanding-typescripts-benefits-and-pitfalls-24c1e02b3e9c/)
- [Ablison: Pros And Cons Of Typescript 2023](https://www.ablison.com/pros-and-cons-of-typescript-2023/)