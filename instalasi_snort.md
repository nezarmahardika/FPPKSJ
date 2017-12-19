Instalasi Snort di Ubuntu
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
    sudo useradd snort -r -s /sbin/nologin -c SNORT_IDS -g snort
    ```
    ```
    sudo ln -s /usr/local/bin/snort /usr/sbin/snort
    ```
