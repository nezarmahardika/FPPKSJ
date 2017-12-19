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
