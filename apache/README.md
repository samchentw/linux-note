# Apache
伺服器，大部份ubuntu內建就有安裝apache2


## 使用

狀態
```
 sudo systemctl status apache2
```

啟用
```
 sudo systemctl start apache2
```

重啟
```
sudo systemctl restart apache2
```

停止
```
sudo systemctl stop apache2
```


## 加入新port號

```
cd /etc/apache2
vim ports.conf
```

可在以下Listen 80再加入Listen 81，修改後存檔，如下：
```
   # If you just change the port or add more ports here, you will likely also
   # have to change the VirtualHost statement in
   # /etc/apache2/sites-enabled/000-default.conf
   
   Listen 80
   Listen 81
   <IfModule ssl_module>
           Listen 443
   </IfModule>
   
   <IfModule mod_gnutls.c>
           Listen 443
   </IfModule>
   
   # vim: syntax=apache ts=4 sw=4 sts=4 sr noet
```
在到sites-enabled資料夾下建立site.conf檔
```
<VirtualHost *:81>

        ServerAdmin samchentw@localhost
        DocumentRoot /var/www/html

        ErrorLog ${APACHE_LOG_DIR}/error.log
        CustomLog ${APACHE_LOG_DIR}/access.log combined

</VirtualHost>
```
建立完後重新啟動apache2
```
sudo systemctl restart apache2
```