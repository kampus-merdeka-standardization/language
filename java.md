# Introduction

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