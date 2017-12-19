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
