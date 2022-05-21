# linux安裝php

## 安裝多版本php指令
```
sudo apt install software-properties-common
sudo add-apt-repository ppa:ondrej/php
```

## 安裝方式如下：
```
sudo apt install php[version]
```

範例：
```
sudo apt install php7.1 php7.1-common php7.1-opcache php7.1-mcrypt php7.1-cli php7.1-gd php7.1-curl php7.1-mysql
```

## 可以使用update-alternatives切換版本
```
sudo update-alternatives --config php
```

## 取得php.ini路徑
```
php -i | grep "Loaded Configuration File"

```