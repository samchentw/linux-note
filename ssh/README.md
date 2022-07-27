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
ssh -i "xxx.pem" ubuntu@exxxxxxxxx.compute.amazonaws.com  #aws為例
```


