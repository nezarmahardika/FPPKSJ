Lesson 8
--------
- **Step 1**    : Setting networks pada mozilla yang ada di Kali Linux dengan mengisi manual proxy dan diisi HHTP Proxy `127.0.0.1` dan port `8080`
- **Step 2**    : Buka aplikasi burpsuite yang sudah ada di Kali, lalu setting `intercept is off` pada tab proxy lalu tab intercept
- **Step 3**    : Lalu klik OWASP Top 10 --> A1 - SQL Injection --> SQLi - Extract Data --> User Info pada mutillidae, lalu ubah size pada kolom **Name** dari **20** menjadi **100** lalu ketik `' union select null -- ` dan jangan lupa tambahkan spasi setelah `--` dan view account details
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%208/1.JPG)
- Lalu akan menghasilkan error
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%208/2.JPG)
- **Step 4**    : Lalu ubah lagi size pada kolom **Name** menjadi **100** lagi, dan ketik `' union select null,null,null,null,null --`
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%208/3.JPG)
- Lalu akan muncul
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%208/4.JPG)
- **Step 5**    : Lalu ubah lagi size pada kolom **Name** menjadi **100** lagi, dan ketik `' union select 1,2,3,4,5 --`
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%208/5.JPG)
- Lalu akan muncul
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%208/6.JPG)
- **Step 6**    : Lalu ubah lagi size pada kolom **Name** menjadi **100** lagi, dan ketik `' union select ccid,ccnumber,ccv,expiration,null from credit_cards -- `
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%208/7.JPG)
- Lalu akan muncul
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%208/8.JPG)
- **Step 7**    : Lalu buka aplikasi burpsuite, pada tab proxy, lalu HTTP history, buka pada host yang terdapat method get yang baru kita lakukan pada mutillidae
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%208/9.JPG)
