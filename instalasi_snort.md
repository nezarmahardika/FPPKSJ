### Instalasi Snort di Ubuntu
--------------------

Instalasi Snort di ubuntu cukup sederhana tetapi membutuhkan langkah-langkah yang sedikit panjang. langkah-langkah tersebut akan dijabarkan dibawah ini :

- **Langkah 1**    : menginstall library yang dibutuhkan snort dengan mengetikkan command dibawah ini
    ```
    sudo apt install -y gcc libpcre3-dev zlib1g-dev libpcap-dev openssl libssl-dev libnghttp2-dev libdumbnet-dev bison flex libdnet
    ```

- **Langkah 2**    : membuat temporary folder di directory home untuk tempat mengunduh semua kebutuhan dalam mengisntall snort. lalu masuk ke folder tersebut
    ```
    mkdir ~/snort_src && cd ~/snort_src
    ```
- **Langkah 3**    : mengunduh Data Aquisition Library (DAQ) yang didalamnya ada library untuk meng-capture packet. setelah mendownloadnya, file tersebut di ekstrak, lalu masuk ke folder tersebut.
    ```
    wget https://www.snort.org/downloads/snort/daq-2.0.6.tar.gz
    ```
    ```
    tar -xvzf daq-2.0.6.tar.gz
    ```
    ```
    cd daq-2.0.6
    ```
    
- **Langkah 4**    : run skrip konfigurasi , lalu kompilasi program dengan 'make' dan install DAQ. lalu kembali ke temporary folder
    ```
    ./configure && make && sudo make install
    ```
    ```
    cd ~/snort_src
    ```
    
- **Langkah 5**    : mengunduh Snort (versi dari aplikasi bisa diubah jika memang ad ayang terbaru). setelah mendownloadnya, file tersebut di ekstrak, lalu masuk ke folder tersebut.
    ```
    wget https://www.snort.org/downloads/snort/snort-2.9.11.tar.gz
    ```
    ```
    tar -xvzf snort-2.9.11.tar.gz
    ```
    ```
    cd snort-2.9.11
    ```
    
- **Langkah 6**    : run skrip konfigurasi dengan 'sourcefire' , lalu kompilasi program dengan 'make' dan install
    ```
    ./configure --enable-sourcefire && make && sudo make install
    ```
    ```
    cd ~/snort_src
    ```
    
- **Langkah 7**    : selanjutnya kita butuh untuk menkonfigurasi Snort agar bisa terbaca oleh Ubuntu. dimulai dengam mengupdate library lalu membuat link untuk Snort
    ```
    sudo ldconfig
    ```
    ```
    sudo ln -s /usr/local/bin/snort /usr/sbin/snort
    ```
    
- **Langkah 8**    : untuk menjalankan snort tanpa harus masuk sebagai root, gunakan command sebagai berikut
    ```
    sudo groupadd snort
    ```
    ```
    sudo useradd snort -r -s /sbin/nologin -c SNORT_IDS -g snortt
    ```
    
- **Langkah 9**    : buat folder untuk menampung konfigurasi dari Snort dengan mengikuti command dibawah
    ```
    sudo mkdir -p /etc/snort/rules
    ```
    ```
    sudo mkdir /var/log/snort
    ```
    ```
    sudo mkdir /usr/local/lib/snort_dynamicrules
    ```

- **Langkah 10**    : ubah permission dari folder-folder tersebut
    ```
    sudo chmod -R 5775 /etc/snort
    ```
    ```
    sudo chmod -R 5775 /var/log/snort
    ```
    ```
    sudo chmod -R 5775 /usr/local/lib/snort_dynamicrules
    ```
    ```
    sudo chown -R snort:snort /etc/snort
    ```
    ```
    sudo chown -R snort:snort /var/log/snort
    ```
    ```
    sudo chown -R snort:snort /usr/local/lib/snort_dynamicrules
    ```
    
- **Langkah 11**    : buat file yang merupakan rules dari Snort
    ```
    sudo touch /etc/snort/rules/white_list.rules
    ```
    ```
    sudo touch /etc/snort/rules/black_list.rules
    ```
    ```
    sudo touch /etc/snort/rules/local.rules
    ```
    
- **Langkah 12**    : salin file konfigurasi dari temporary folder
    ```
    sudo cp ~/snort_src/snort-2.9.9.0/etc/*.conf* /etc/snort
    ```
    ```
    sudo cp ~/snort_src/snort-2.9.9.0/etc/*.map /etc/snort
    ```
    
- **Langkah 13**    : salin file konfigurasi dari temporary folder
    ```
    sudo cp ~/snort_src/snort-2.9.9.0/etc/*.conf* /etc/snort
    ```
    ```
    sudo cp ~/snort_src/snort-2.9.9.0/etc/*.map /etc/snort
    ```


### Instalasi Snort di Windows
--------------------
- **Langkah 1**    : masuk ke website dari Snort lalu pilih tab Windows
    ```
    https://www.snort.org/#get-started
    ```
     ![](/assets/Snort/instal.PNG)
- **Langkah 2**    : jalankan snort2.9.11.exe

- **Langkah 3**    : lakukan instalasi secara manual dan seperti biasa. setelah itu kita akan mendapatkan folder Snort seperti ini
     ![](/assets/Snort/windows.png)
