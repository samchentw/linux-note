# ufw(防火牆)
為ubuntu內建的防火牆

## 啟用 UFW，且開機自動載入和啟用：
```
sudo ufw enable
```

## 停用 UFW，且開機停用：
```
sudo ufw disable
```

## 顯示功能列表
```
sudo ufw app list
```

## 狀態
```
sudo ufw status
```

## 查看序號
```
sudo ufw status numbered
```

## 啟動/關閉某功能、刪除、重設
```
sudo ufw allow 'Apache'
sudo ufw deny 'Apache'
sudo ufw delete 1 # 指定刪除的項目
sudo ufw reset # 重設
```

## 針對連線 ip 設定
```
sudo ufw allow from 10.0.0.0/8
sudo ufw allow from 172.16.0.0/12
sudo ufw allow from 192.168.0.0/16
```

## 禁止某IP
```
sudo ufw deny from 192.168.1.123
sudo ufw deny from 192.168.1.1 port 22
```

## 日誌功能（日誌預設會存在 /var/log/ufw.log ）
```
sudo ufw logging on
sudo ufw logging off
```