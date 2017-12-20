### Uji Coba Membaca Pcap di Snort
--------------------

Ada 2 cara membaca file pcap dengan snort

- **Cara 1**
  cara pertama adalah dengan merujuk ke snort.conf untuk menggunakan satu atau lebih rules
    ```
    Snort -r <lokasi_file_pcap>/<nama_file>.pcap -T -c <lokasi_konfigurasi_snort>/snort.conf
    ```
    contoh di Ubuntu :
    ```
    Snort -r /Downloads/log.pcap -T -c /etc/snort/snort.conf
    ```
    contoh di Windows :
    ```
    Snort -r C:\Downloads\log.pcap -T -c C:\Snort\etc\snort.conf
    ```

- **Cara 2**
  cara pertama adalah dengan langsung menggunakan rules tanpa merujuk ke snort.conf
    ```
    Snort -r <lokasi_file_pcap>/<nama_file>.pcap -c <nama_rules>.rules
    ```
    Contoh :
     ```
    Snort -r log.pcap -c rules.rules
    ```
    
    - **Hasil** 
    ini adalah hasil dari pembacaan FTP crack/bad login oleh snort yang dimasukkan kedalam suatu log file.
    
    ![](/assets/Snort/hasil1.PNG)
    ![](/assets/Snort/hasil2.PNG)
