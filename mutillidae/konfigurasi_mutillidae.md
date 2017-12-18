Konfirgurasi Mutilidae
-----------------------
Mutilidae sudah terinstall pada virtual machine Metasploitable. Sebelum menggunakannya, ada beberapa langkah yang harus dilakukan terlebih dahulu untuk konfigurasi Mutilidae 
- **Step 1**    : Ganti nama database pada Mutilidae
    - Akses **config.inc**
        ```
        nano /var/www/multilidae/config.inc
        ```
    - Ganti isi pada __**config.inc**__ menjadi
        ```
        <?php
            /* NOTE: On Samurai, the $dbpass password is "samurai" rather than blank */
    
            $dbhost = '0.0.0.0';
            $dbuser = 'root';
            $dbpass = '';
            $dbname = 'owasp10';
        ?>
        ```

- **Step 2**    : Akses Mutilidae pada Metasploitable
    ```
    http://10.151.36.105/mutillidae/
    ```
- **Step 3**    : Reset DB untuk membuat struktur basis data dari Mutilidae ke MySQL pada Metasploitable

Muitilidae sudah siap digunakan
