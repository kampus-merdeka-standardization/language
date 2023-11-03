# Introduction
Java adalah bahasa pemrograman yang dapat dijalankan di berbagai komputer termasuk telepon genggam. Bahasa ini awalnya dibuat oleh James Gosling saat masih bergabung di Sun Microsystems, yang saat ini merupakan bagian dari Oracle dan dirilis tahun 1995. Java terlahir dari The Green Project, yang berjalan selama 18 bulan, dari awal tahun 1991 hingga musim panas 1992. Proyek ini dimotori oleh Patrick Naughton, Mike Sheridan, dan James Gosling, beserta sembilan pemrogram lainnya dari Sun Microsystems. Salah satu hasil proyek ini adalah maskot Duke yang dibuat oleh Joe Palrang. Awalnya, Proyek ini dikenal sebagai "Oak" dan ditujukan untuk perangkat elektronik konsumen, seperti mesin cuci, tetapi visinya berkembang menjadi lebih luas. Nama Oak, diambil dari pohon oak yang tumbuh di depan jendela ruangan kerja “bapak java”, James Gosling. Nama Oak ini tidak dipakai untuk versi release Java karena sebuah perangkat lunak sudah terdaftar dengan merek dagang tersebut, sehingga diambil nama penggantinya menjadi “Java”. Nama ini diambil dari kopi murni yang digiling langsung dari biji (kopi tubruk) kesukaan Gosling.

# Comparation

## Pros & Cons Java
| Pro | Kontra |
| :-- | :----- |
| Java adalah bahasa pemrograman yang sederhana, mudah dipelajari, dan dipahami. | Java membutuhkan lisensi komersial yang berbayar untuk penggunaan komersial. |
| Java adalah bahasa pemrograman berorientasi objek, yang membantu menyelesaikan masalah dunia nyata dengan lebih mudah dan aman. | Java memiliki kinerja yang lebih rendah dibandingkan bahasa pemrograman level rendah seperti C dan C++. |
| Java adalah bahasa pemrograman yang aman, karena tidak menggunakan pointer yang dapat menyebabkan akses memori yang tidak sah. | Java memiliki tampilan dan nuansa yang kurang menarik di desktop. |
| Java adalah bahasa pemrograman yang murah dan ekonomis untuk dikembangkan dan dipelihara, karena dapat berjalan di berbagai mesin tanpa memerlukan perangkat keras khusus. | Java memiliki tingkat kompleksitas kode yang tinggi, karena menggunakan banyak fitur dan konsep seperti abstraksi, enkapsulasi, pewarisan, polimorfisme, dll. |
| Java adalah bahasa pemrograman yang platform-independen, yang berarti kode yang ditulis di satu sistem dapat dijalankan di sistem lain yang memiliki Java di dalamnya. | Java membutuhkan ruang memori yang signifikan, karena menggunakan manajemen memori otomatis (garbage collection) yang dapat menyebabkan penundaan (latency) saat menjalankan aplikasi. |
| Java adalah bahasa pemrograman level tinggi, yang berarti kode ditulis dalam bahasa manusia yang mirip dengan bahasa Inggris. | Java memiliki dukungan terbatas untuk pemrograman level rendah, seperti manipulasi bit atau akses langsung ke perangkat keras. |
| Java mendukung fitur portabilitas, yang berarti Java dapat digunakan di berbagai platform dan perangkat. |  |
| Java memiliki komunitas dukungan yang besar dan aktif, yang dapat membantu programmer menyelesaikan masalah atau belajar hal-hal baru tentang Java. |  |
| Java mendukung multithreading, yang berarti Java dapat menjalankan beberapa proses secara bersamaan dan meningkatkan kinerja aplikasi. |  |
| Pada Java versi terbaru terdapat fitur-fitur yang menarik dan berguna seperti virtual threads, record patterns, pattern matching for switch, string templates, unnamed classes and instance main methods, dan lain-lain ||
| Java dapat digunakan untuk mengembangkan aplikasi web dan mobile yang berskala besar, efisien, dan responsif ||

### Reference :
- [Pros and Cons of Java | Advantages and Disadvantages of Java - DataFlair](https://data-flair.training/blogs/pros-and-cons-of-java/)
- [20 Important Pros and Cons of Java 2023 | Ablison](https://www.ablison.com/important-pros-and-cons-of-java/#google_vignette)
- [Pros and Cons of Choosing Java Development For Your Project](https://star-knowledge.com/blog/pros-and-cons-of-choosing-java-development-for-your-project/)
- [Advantages and disadvantages of Java - Javatpoint](https://www.javatpoint.com/advantages-and-disadvantages-of-java)
- [The Pros and Cons of Java Development | Blog - BairesDev](https://www.bairesdev.com/blog/pros-cons-java-development/)
- [Pros and Cons of Java: Key Advantages and Disadvantages - Softjourn](https://softjourn.com/insights/pros-and-cons-of-java-development)

# Installation
Pada dokumentasi ini, kita akan mencoba meng-install menggunakan [OpenJDK](https://openjdk.java.net/) dikarenakan open source dan juga free.

Selain OpenJDK ada beberapa alternatif lain seperti:
- [OracleJDK](https://www.oracle.com/java/technologies/javase-downloads.html)
- [Amazon Corretto](https://aws.amazon.com/id/corretto/)
- [Zulu](https://www.azul.com/downloads/zulu-community/)

## JDK vs JRE
Sederhananya `JDK (Java Development Kit)` merupakan tools untuk `mengembangkan` program java, sedangkan `JRE (Java Runtime Environment)` merupakan tools untuk `menjalankan` program java. Ketika menginstall JDK didalamnya sudah terdapat JRE, sehingga kita tidak perlu lagi untuk menginstal JRE


## Windows
1. Install dan pilih versi java yang diinginkan pada laman https://jdk.java.net/archive/

2. Lalu ekstrak file pada lokasi yang kita inginkan

3. Atur environment variable
    - tekan tombol windows
    - cari 'env' maka nanti akan muncul seperti ini<br/>
    ![Searching Environtment Image](/img/java/installation/windows/environment-search.jpg)
    - Klik Environment Variables<br/>
    ![Environtment Variables Image](/img/java/installation/windows/environment-variables.jpg)
    - Tambahkan environment variable baru dengan nama variable `JAVA_HOME`, dan nilai variable berupa lokasi direktori yang mengarah pada jdk yang kita install sebelumnya. Lokasi direktori adalah lokasi **sebelum `bin`** folder<br/>
    ![Menambahkan environment JAVA_HOME](/img/java/installation/windows/JAVA_HOME.jpg)
    - Tambahkan lokasi folder jdk bin pada `Path` di system variable<br/>
    ![Edit Path di system variable](/img/java/installation/windows/edit-path.jpg)
    ![tambahkan '%JAVA_HOME%/bin'](/img/java/installation/windows/jdk-bin-on-path.jpg)
4. Kemudian simpan dan pastikan berhasil dengan mencoba perintah 
    - `$ java --version`
    - kalau berhasil akan muncul detail versi java seperti 
        ```
        openjdk 17.0.2 2022-01-18
        OpenJDK Runtime Environment (build 17.0.2+8-86)
        OpenJDK 64-Bit Server VM (build 17.0.2+8-86, mixed mode, sharing)
        ```
        versi mungkin berbeda sesuai yang kita install sebelumnya
    - `$ javac --version`
    - kalau berhasil akan muncul detail versi java compiler seperti 
        ```
        javac 17.0.2
        ```

## Linux atau MacOs
1. Install dan pilih versi java yang diinginkan pada laman https://jdk.java.net/archive/

2. Atur environment variable 
    - Tambahkan lokasi jdk **(sebelum direktori `bin`)** yang kita install kedalam environment dengan nama `JAVA_HOME`
    - Tambahkan lokasi jdk bin pada environment `PATH` 
    - Dua tahapan diatas bisa dilakukan dengan menambahkan baris berikut pada `.bashrc` atau `.profile` atau `.zshrc`
        ```sh
        export JAVA_HOME="/lokasi/ke/jdk/yang/kita/simpan"
        export PATH="$JAVA_HOME/bin:$PATH"
        ```

3. Pastikan dengan mencoba perintah 
    - `$ java --version`
    - kalau berhasil akan muncul detail versi java seperti 
        ```
        openjdk 17.0.2 2022-01-18
        OpenJDK Runtime Environment (build 17.0.2+8-86)
        OpenJDK 64-Bit Server VM (build 17.0.2+8-86, mixed mode, sharing)
        ```
        versi mungkin berbeda sesuai yang kita install sebelumnya
    - `$ javac --version`
    - kalau berhasil akan muncul detail versi java compiler seperti 
        ```
        javac 17.0.2
        ```

# Convention

## _File_
- _File_ Java harus diberi nama dengan huruf kapital pertama (PascalCase) yang mencerminkan nama kelas di dalamnya. Contoh: `MyClass.java`.

## Variabel
- Nama variabel harus dimulai dengan huruf kecil (camelCase) dan harus menjelaskan tujuan variabel tersebut. Contoh: `namaDepan`, `jumlahMahasiswa`.

### Contoh yang benar
```java
int studentAge;
String carModel;
double bankBalance;
```

### Contoh yang salah
```java
int StudentAge; // menggunakan PascalCase
String car_model; // menggunakan snake_case
double bank_balance; // menggunakan snake_case
int 123Var; // diawali dengan angka
```

## Fungsi (Metode)
- Nama metode harus dimulai dengan huruf kecil (camelCase) dan harus menjelaskan tujuan metode tersebut. Contoh: `hitungTotal()`, `ambilData()`.
- Nama metode yang bertindak sebagai perintah harus menggunakan kata kerja yang jelas untuk menjelaskan tindakan yang dilakukan. Contoh: `jalankanProses()`, `simpanData()`.
- Metode yang mengembalikan nilai boolean seringkali diawali dengan kata kerja yang bersifat mengecek (misalnya, `is`, `has`, `can`, `should`). Contoh: `isValid()`, `hasPermission()`.

### Contoh yang benar
```java
public class Example {
    public void printMessage(String message) {
        System.out.println(message);
    }

    public int calculateSum(int a, int b) {
        return a + b;
    }
}
```

### Contoh yang salah
```java
public class Example {
    // Fungsi dengan nama PascalCase
    public void PrintMessage(String message) {
        System.out.println(message);
    }

    // Fungsi dengan snake_case
    public int calculate_sum(int a, int b) {
        return a + b;
    }

    // Fungsi dengan nama yang tidak deskriptif
    public void func1(int x, int y) {
        // ...
    }
}
```

## Konstanta
- Nama konstanta harus ditulis dengan huruf besar dan menggunakan garis bawah sebagai pemisah (`SNAKE_CASE`). Contoh: `PI`, `MAX_VALUE`.
- Konstanta umumnya diletakkan pada bagian awal kelas

### Contoh yang benar
```java
public class MyClass {
    public static final int MAX_VALUE = 100;
    public static final String API_KEY = "myApiKey";
    public static final double PI = 3.14159265359;
    // ...
}
```

### Contoh yang salah 
```java
public class ConstantsExample {

    // ...    => seharusnya field konstan berada pada awal kelas

    public static final int maxvalue = 100; // Penamaan dengan huruf kecil
    public static final String apikey = "myApiKey"; // Penamaan dengan huruf kecil
    public static final double PiValue = 3.14159265359; // Penamaan tidak konsisten
}
```

## Class, interface, Enum, Dan lain lain
- Ditulis dengan format `PascalCase` seperti `Person`, `Animal`, `User`

### Contoh yang benar
```java
public class Student {
    // ...
}

public class CarModel {
    // ...
}

public class BankAccount {
    // ...
}
```

### Contoh yang salah
```java
public class student {
    // Nama class dengan huruf kecil
    // ...
}

public class car_model {
    // Nama class dengan garis bawah
    // ...
}

public class Bank_Account {
    // ...
}

public class 123Class {
    // Nama class dengan angka di depan
    // ...
}
```

## Comment
- Selalu sertakan komentar untuk menjelaskan kode yang kompleks, tujuan, atau pemahaman tambahan tentang cara kode bekerja.
- Komentar harus informatif dan relevan, membantu pembaca memahami mengapa kode tertentu ditulis atau cara kerjanya.
- Hindari komentar yang hanya memberikan informasi yang jelas dari kode itu sendiri (misalnya, "Ini adalah penjumlahan dua angka").

### Single-Line Comment
Komentar single-line digunakan untuk memberikan penjelasan singkat pada baris kode tertentu. Caranya adalah dengan menambahkan komentar single-line dengan menggunakan dua garis miring `//`.

```java
int umur = 30; // Variabel untuk menyimpan umur
```

### Multi-line Comment
Komentar multi-line digunakan untuk memberikan penjelasan lebih panjang atau untuk menutupi beberapa baris kode. Caranya adalah dengan menambahkan komentar multi-line dengan menggunakan `/*` untuk awalan komentar dan `*/` untuk mengakhiri komentar.

```java
/**
 * Ini adalah komentar multi-line.
 * Ini dapat menutupi beberapa baris kode sekaligus.
 * Berguna untuk penjelasan yang lebih rinci.
 */
int jumlahMahasiswa = 50;
```

## Penanganan Kesalahan (Error Handling)
- Ketika menangani kesalahan, gunakan struktur pengecualian (_exception_) yang sesuai, dan berikan pesan kesalahan yang informatif.
- Selalu tangani kesalahan dengan cara yang sesuai dengan konteks, seperti menggunakan blok `try-catch` untuk menangani pengecualian.

## Try-with-resource
- Saat menggunakan sumber daya seperti berkas, soket, atau objek yang memerlukan penutupan eksplisit, selalu gunakan blok try-with-resources untuk mengelola sumber daya tersebut.
- Blok try-with-resources memastikan bahwa sumber daya akan ditutup secara otomatis setelah selesai digunakan, yang menghindari kebocoran sumber daya (resource leaks).
- Blok try-with-resources hanya dapat digunakan pada Object yang mengimplementasikan interface `Closeable`
- Contoh penggunaan blok try-with-resources untuk menangani sumber daya:
```java
try (FileInputStream input = new FileInputStream("file.txt");
     FileOutputStream output = new FileOutputStream("output.txt")) {
    // Lakukan operasi pada file
} catch (IOException e) {
    // Tangani kesalahan jika terjadi
}
```
Penggunaan try-with-resources adalah praktik yang sangat disarankan dalam Java untuk memastikan bahwa sumber daya eksternal dielola dengan benar dan ditutup setelah selesai digunakan. Hal ini membantu mencegah kebocoran sumber daya dan membuat kode lebih aman dan efisien.

Berikut contoh yang tidak direkomendasikan, yaitu tanpa try-with-resource 

```java
FileInputStream input = null;
FileOutputStream output = null;

try {
    input = new FileInputStream("file.txt");
    output = new FileOutputStream("output.txt");

    // Lakukan operasi pada file
} catch (IOException e) {
    // Tangani kesalahan jika terjadi
} finally {
    try {
        if (input != null) {
            input.close();
        }
    } catch (IOException e) {
        // Tangani kesalahan saat menutup input stream
    }

    try {
        if (output != null) {
            output.close();
        }
    } catch (IOException e) {
        // Tangani kesalahan saat menutup output stream
    }
}
```