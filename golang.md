# Introduction

Dokumentasi ini dibuat untuk menghadirkan pedoman dan panduan standar dalam mengembangkan proyek dalam bahasa Go di perusahaan. Tujuan utamanya adalah meningkatkan konsistensi, kualitas, dan efisiensi pengembangan perangkat lunak.

Golang (atau biasa disebut dengan Go) adalah bahasa pemrograman yang dikembangkan di Google oleh Robert Griesemer, Rob Pike, dan Ken Thompson pada tahun 2007 dan mulai diperkenalkan ke publik tahun 2009. Penciptaan bahasa Go didasari bahasa C dan C++, oleh karena itu gaya sintaksnya mirip.

# Comparation

## Pros & Cons Golang

| pros | cons |
| :-- | :-- |
| Mendukung konkurensi di level bahasa dengan pengaplikasian cukup mudah | Golang relatif muda dalam hal umur bahasa pemrograman. Hal ini berarti lebih sedikit library yang ada, terutama ketika berinteraksi dengan platform lain |
| Mendukung pemrosesan data dengan banyak prosesor dalam waktu yang bersamaan (pararel processing) | Karena usia bahasa pemrograman yang bisa dibilang muda, Komunitas bahasa pemrograman ini mungkin tidak sebesar bahasa-bahasa pemrograman lain di luar sana |
| Memiliki garbage collector dan kompilasi yang sangat cepat | |
| Bukan bahasa pemrograman yang hirarkial dan bukan strict OOP, memberikan kebebasan ke developer perihal bagaimana cara penulisan kode | |

# Installation

## Windows

1. Download terlebih dahulu installer-nya di https://golang.org/dl/. Pilih installer untuk sistem operasi Windows sesuai jenis bit yang digunakan.
2. Setelah ter-download, jalankan installer, klik next hingga proses instalasi selesai. By default jika anda tidak merubah path pada saat instalasi, Go akan ter-install di C:\go. Path tersebut secara otomatis akan didaftarkan dalam PATH environment variable.
3. Buka Command Prompt / CMD, eksekusi perintah berikut untuk mengecek versi Go.
    ```shell 
    go version
    ````
4. Jika output adalah sama dengan versi Go yang ter-install, menandakan proses instalasi berhasil.

## MacOS

Cara termudah instalasi Go di MacOS adalah menggunakan [Homebrew](https://brew.sh).

1. Install terlebih dahulu Homebrew (jika belum ada), caranya jalankan perintah berikut di terminal.
    ```shell
    $ ruby -e "$(curl -fsSL http://git.io/pVOl)"
    ```
2. Install Go menggunakan command brew.
    ```shell
    $ brew install go
    ```
3. Tambahkan path binary Go ke PATH environment variable.
    ```shell
    $ echo "export PATH=$PATH:/usr/local/go/bin" >> ~/.bash_profile
    $ source ~/.bash_profile
    ```
4. Jalankan perintah berikut mengecek versi Go.
    ```shell
    go version
    ```
5. Jika output adalah sama dengan versi Go yang ter-install, menandakan proses instalasi berhasil.

## Linux

1. Unduh arsip installer dari https://golang.org/dl/, pilih installer untuk Linux yang sesuai dengan jenis bit komputer anda. 
Proses download bisa dilakukan lewat CLI, menggunakan `wget` atau `curl`.
    ```shell
    $ wget https://storage.googleapis.com/golang/go1...
    ```
2. Buka terminal, extract arsip tersebut ke /usr/local.
    ```shell
    $ tar -C /usr/local -xzf go1...
    ```
3. Tambahkan path binary Go ke PATH environment variable.
    ```shell
    $ echo "export PATH=$PATH:/usr/local/go/bin" >> ~/.bashrc
    $ source ~/.bashrc
    ```
4. Selanjutnya, eksekusi perintah berikut untuk mengetes apakah Go sudah terinstal dengan benar.
    ```shell
    go version
    ```
5. Jika output adalah sama dengan versi Go yang ter-install, menandakan proses instalasi berhasil.

## Variabel `GOROOT`

By default, setelah proses instalasi Go selesai, secara otomatis akan muncul environment variable GOROOT. Isi dari 
variabel ini adalah lokasi di mana Go ter-install. Sebagai contoh di Windows, ketika Go di-install di C:\go, maka path 
tersebut akan menjadi isi dari GOROOT. Silakan gunakan command go env untuk melihat informasi konfigurasi environment yang ada.

# Convention

## Table Comparison

| Kategori | Penulisan | Pemilihan Kata |
| -------- | --------- | -------------- |
| File name | snake_case| kata benda     |
| Variable name| private: camelCase <br> public: PascalCase | kata benda |
| Constanta name | UPPER_SNAKE_CASE | kata benda |
| Struct name | private: camelCase <br> public: PascalCase | kata benda |
| Function name | private: camelCase <br> public: PascalCase | kata kerja |
| Interface name | private: camelCase <br> public: PascalCase | kata benda dengan akhiran "Interface" |

## File

- Go mengikuti konvensi di mana semua file sumber menggunakan huruf kecil dengan garis bawah yang memisahkan beberapa kata
- Nama file gabungan dipisahkan dengan _
- Nama file yang dimulai dengan “.” atau “_” diabaikan oleh Go
- File dengan akhiran _test.go hanya dikompilasi dan dijalankan oleh alat go test
- Penamaan nama file menggunakan *snake_case* dan kata benda

### Example

- Benar
  ```sh
  user_repository.go
  user_repository_test.go
  ```
- Salah
  ```sh
  userRepository.go
  user-reposirory.go
  userRepositoryTest.go
  ```

## Variable

- Nama variabel harus deskriptif dan singkat, dan harus menggambarkan nilai yang disimpan dalam variabel
- Nama awal variabel harus ditulis dalam huruf kecil, kecuali jika variabel bersifat *public*
- Penulisan nama variabel menggunakan *camelCase* untuk *private* dan *PascalCase* untuk *public*
- Gunakan kata benda
- Hindari penggunaan nama variabel yang sama dengan tipe data bawaan Go, seperti `string` atau `int`

### Example

- Benar
  ```go
  var age int
  var firstName string
  var LastName string //variabel public
  ```
- Salah
  ```go
  var myString string
  var customer_name string
  var TOTAL int
  ```

## Function

- Nama fungsi harus deskriptif dan singkat, dan harus menggambarkan nilai yang disimpan dalam fungsi
- Nama awal fungsi harus ditulis dalam huruf kecil, kecuali jika fungsi bersifat *public*
- Gunakan *camelCase* untuk *private* dan *PascalCase* untuk *public*
- Gunakan kata kerja dalam penamaan fungsi

### Example

- Benar
  ```go
  func countArea(side float64) float64 {
    return side * side
  }
  ```

  ```go
  func CountArea(side float64) float64 { //public
    return side * side
  }
  ```
- Salah
  ```go
  func counttotal(amount int, price float64) float64 {
    return amount * price
  }
  ```

  ```go
  func COUNTTOTAL(amount int, price float64) float64 {
    return amount * price
  }
  ```

## Const

- Nama constant harus ditulis dalam huruf besar
- Jika nama constant terdiri dari dua atau lebih kata, gunakan underscore (_) sebagai pemisah antara kata-kata tersebut
- Penulisan constant menggunakan *UPPER_SNAKE_CASE*
- Gunakan kata benda

### Example

- Benar
  ```go
  const PI_VALUE float64 = 3.14159265358979323846
  ```
- Salah
  ```go
  const DATABASENAME string = "my_database"
  const max_connections int = 100
  ```

## Struct

- Penulisan nama struct sama dengan nama variabel
- Nama struct harus deskriptif dan singkat, dan harus menggambarkan nilai yang disimpan dalam struct
- Nama awal struct harus ditulis dalam huruf kecil, kecuali jika struct bersifat *public*
- Gunakan *camelCase* untuk *private* dan *PascalCase* untuk *public*
- Gunakan kata benda untuk nama struct

### Example

- Benar
  ```go
  var personData = struct {
    name string
    age int
  }
  ```

  ```go
  var PersonData = struct { //public
    Name string
    Age int
  }
  ```

- Salah
  ```go
  var customerdata = struct {
    name string
    email string
  }
  ```

  ```go
  var CUSTOMERDATA = struct {
    NAME string
    EMAIL string
  }
  ```

## Interface 

- Nama interface harus deskriptif dan mencerminkan fungsinya
- Nama awal interface harus ditulis dalam huruf kecil, kecuali jika interface bersifat *public*
- Gunakan *camelCase* untuk *private* dan *PascalCase* untuk *public*
- Gunakan kata benda untuk nama interface
- Tambahkan suffix atau akhiran "Interface"

### Example

- Benar
  ```go
  type shapeInterface interface {
    countArea() float64
  }

  type ShapeInterface interface {
    countArea() float64
  }
  ```

- Salah
  ```go
  type shape interface {
    countArea() float64
  }
  ```

## Comment

- Komentar harus deskriptif dan singkat, dan harus menggambarkan tugas yang dilakukan oleh kode
- Komentar harus dihindari jika kode itu sendiri sudah cukup deskriptif

### Example

```go
// countArea menghitung luas persegi dengan sisi yang diberikan
func countArea(side float64) float64 {
    return side * side
}
```

## Error Handling

- Multiple return values
  ```go
  func example() (string, error) {
    if err != nil {
        return "", err
    }

    return "Hello, world!", nil
    }
  ```
- Blank identifier
  ```go
  _, err := example()
  if err != nil {
    // Handle the error.
  }
  ```

## API Documentation

diarahkan pake swagger & cara makenya

## Reference

- [Dokumentasi Resmi Go](https://go.dev/doc/)
- [Effectice Go](https://go.dev/doc/effective_go)
- [Dasar Pemrograman Golang](https://dasarpemrogramangolang.novalagung.com/)
- [Interface Naming](https://medium.com/@dotronglong/interface-naming-convention-in-golang-f53d9f471593)