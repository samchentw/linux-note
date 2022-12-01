# nginx

## 安裝
```
sudo apt update
sudo apt install nginx
```

## 防火牆開通
```
sudo ufw allow 'Nginx HTTP'
sudo ufw status
```

## 狀態查詢
```
systemctl status nginx
```

## 關閉啟用
```
sudo systemctl stop nginx
sudo systemctl start nginx
```
