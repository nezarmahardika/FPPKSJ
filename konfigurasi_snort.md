### Konfigurasi Snort
--------------------

Konfigurasi Snort di Ubuntu maupun windows pada dasarnya sama saja, hanya letak file konfigurasinya saja yang berbeda. Berikut adalah langkah-langkah melakukan konfigurai pada Snort :
       
- **Langkah 1**    : membuka file snort.conf
    - Dengan Cara   :
        - Ubuntu        : untuk membuka file konfigurasi bisa dilakukan dengan mengetikkan command dibawah ini, jika mengikuti langkah-langkah instalasi yang telah dijelaskan sebelumnya
         ```
        sudo gedit /etc/snort/snort.conf
         ```
        - Windows       : Terletak di dalam folder 'etc' di dalam folder instalasi Snort
        ![](/assets/Snort/snortwindows.PNG)


- **Langkah 2**    : konfigurasi di snort yang utama adalah menentukan letak dari rules Snort di snort.conf. setelah membuka snort.conf, cari dan edit hal-hal dibawah
    - Dengan Cara   :
        - Ubuntu        
         ```
        var RULE_PATH /etc/snort/rules
        var SO_RULE_PATH /etc/snort/so_rules
        var PREPROC_RULE_PATH /etc/snort/preproc_rules
        var WHITE_LIST_PATH /etc/snort/rules
        var BLACK_LIST_PATH /etc/snort/rules
         ```
        - Windows (Jika folder instalasi Snort ada di C:\Snort)  
         ```
        var RULE_PATH C:\Snort\rules
        var SO_RULE_PATH C:\Snort\rules
        var PREPROC_RULE_PATH C:\Snort\rules
        var WHITE_LIST_PATH C:\Snort\rules
        var BLACK_LIST_PATH C:\Snort\rules
         ```
- **Langkah 3**    : menambahkan rules yang akan dipakai dalam pengujian dengan cara mengedit snort.conf dang menambahkan
    ```
    include $RULE_PATH/<nama_file_rules>.rules
    ```

- **Langkah 4**    : setelah melakukan konfigurasi diatas kita perlu mengecek apakah konfigurasi yang kita lakukan tadi benar. dengan cara membuka terminal atu command prompt lalu mengetikkan
    ```
    sudo snort -T -c /etc/snort/snort.conf
    ```
    Jika konfigurasi berhasil akan muncul pesan sebagai berikut
     ```
    Snort successfully validated the configuration!
    Snort exiting
    ```
    ![](/assets/Snort/sukses.png)
