# Introduction
Java adalah bahasa pemrograman yang dapat dijalankan di berbagai komputer termasuk telepon genggam. Bahasa ini awalnya dibuat oleh James Gosling saat masih bergabung di Sun Microsystems, yang saat ini merupakan bagian dari Oracle dan dirilis tahun 1995. Java terlahir dari The Green Project, yang berjalan selama 18 bulan, dari awal tahun 1991 hingga musim panas 1992. Proyek ini dimotori oleh Patrick Naughton, Mike Sheridan, dan James Gosling, beserta sembilan pemrogram lainnya dari Sun Microsystems. Salah satu hasil proyek ini adalah maskot Duke yang dibuat oleh Joe Palrang. Awalnya, Proyek ini dikenal sebagai "Oak" dan ditujukan untuk perangkat elektronik konsumen, seperti mesin cuci, tetapi visinya berkembang menjadi lebih luas. Nama Oak, diambil dari pohon oak yang tumbuh di depan jendela ruangan kerja “bapak java”, James Gosling. Nama Oak ini tidak dipakai untuk versi release Java karena sebuah perangkat lunak sudah terdaftar dengan merek dagang tersebut, sehingga diambil nama penggantinya menjadi “Java”. Nama ini diambil dari kopi murni yang digiling langsung dari biji (kopi tubruk) kesukaan Gosling.

## JDK vs JRE
Sederhananya `JDK (Java Development Kit)` merupakan tools untuk `mengembangkan` program java, sedangkan `JRE (Java Runtime Environment)` merupakan tools untuk `menjalankan` program java. Ketika menginstall JDK didalamnya sudah terdapat JRE, sehingga kita tidak perlu lagi untuk menginstal JRE

# Comparation

## Pros & Cons

# Installation
Pada dokumentasi ini, kita akan mencoba meng-install menggunakan [OpenJDK](https://openjdk.java.net/) dikarenakan open source dan juga free.

Selain OpenJDK ada beberapa alternatif lain seperti:
- [OracleJDK](https://www.oracle.com/java/technologies/javase-downloads.html)
- [Amazon Corretto](https://aws.amazon.com/id/corretto/)
- [Zulu](https://www.azul.com/downloads/zulu-community/)


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