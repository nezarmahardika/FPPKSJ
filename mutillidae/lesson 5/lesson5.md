Lesson 5
--------
- **Step 1**    : Buka Login/Register
- **Step 2**    : Ketik `'` di kolom **Name**
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%205/1.JPG)
- **Step 3**    : Klik Login
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%205/2.JPG)
- **Step 4**    : Ketik `' or 1=1-- ` di kolom **Name** dan jangan lupa berikan spasi setelah `--`
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%205/3.JPG)
- Lalu akan muncul hasilnya seperti gambar di bawah
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%205/4.JPG)
- **Step 5**    : Ketik `samurai` di kolom **Name** dan ketik `'` di kolom **Password**
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%205/5.JPG)
- Lalu akan muncul error
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%205/6.JPG)
- **Step 6**    : Ketik `samurai` di kolom **Name** dan ketik `' or 1=1--` di kolom **Password** dan jangan lupa berikan spasi setelah `--`
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%205/7.JPG)
- Akan muncul hasil seperti berikut
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%205/8.JPG)
- **Step 7**    : Ketik `samurai` di kolom **Name** dan ketik `' or (1=1 and username='samurai')--` di kolom **Password** dan jangan lupa berikan spasi setelah `--`
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%205/9.JPG)
- Akan muncul hasil seperti berikut
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%205/10.JPG)
- **Step 8**    : Jalankan perintah pada metasploit sesuai dengan gambar di bawah ini dan akan muncul hasilnya juga sesuai pada gambar di bawah ini
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%205/11.JPG)
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%205/12.JPG)
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%205/13.JPG)
- **Step 9**    : Jalankan perintah pada metasploit `select * from accounts where username = 'samurai' and password = '' or 1=1; -- ';` dan perintah `select * from accounts where username = 'samurai' and password = '' or (1=1 and username = 'samurai'); -- ';` dan akan muncul hasilnya sesuai pada gambar di bawah ini
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%205/15.JPG)
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%205/16.JPG)
