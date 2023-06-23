# SSH

## linux安裝ssh server
```
sudo apt-get install openssh-server
```

## 確認 SSH 服務
```
sudo service ssh status
```

## 開啟與關閉服務
```
sudo service ssh stop
sudo service ssh startss
```


## 連線到其他ssh服務(client端)
```
ssh username@192.168.1.2 
ssh -i "xxx.pem" ubuntu@exxxxxxxxx.compute.amazonaws.com 
```


## 將遠端的 /var/www/html/ 目錄備份至本地端的 /home/sam/download/backup.tar.gz
ssh sam@192.168.1.2 tar zcf - /var/www/html/ > /home/sam/download/backup.tar.gz

## 將本地端的 /my/path/ 目錄備份至遠端的 /your/file.tar.gz
tar zcf - /home/sam/myproject/ | ssh sam@192.168.1.2 "cat > /var/www/html/myproject.tar.gz"

