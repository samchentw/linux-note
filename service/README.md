# 系統與服務管理器的狀態
service為較高階的指令，用於不同unix 和 linux 中啟動和停止服務。  
systemctl為較低階指令，可控制的項目比service多。

## service指令
```
service nginx start
service nginx stop
service nginx reload
service nginx restart
service nginx status
```

## systemctl指令
```
systemctl start nginx
systemctl start nginx.service
systemctl stop nginx
systemctl reload nginx
systemctl restart nginx
systemctl status nginx
```

## 啟動/禁用系統自啟動服務
```
systemctl enable nginx.service (.service可省略如下)
systemctl enable nginx

systemctl disable nginx.service
systemctl disable nginx
```

## 使用is-enabled來檢查服務是否已經啟動了自啟動
```
systemctl is-enabled apache2
# enabled/disabled
```


## is-active檢查一個服務是否啟動：
```
systemctl is-active apache2
# active/inactive
```