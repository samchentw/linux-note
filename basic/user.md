# 使用者

## 查看所有帳號
```
cat /etc/passwd
```

## getent 指令
```
getent passwd
```


## 檢查指定的使用者帳號資訊
```
getent passwd root
```

## 建立使用者與設定密碼
```
sudo useradd ian
sudo passwd ian
sudo mkdir /home/ian -p
chown ian:ian /home/ian
```