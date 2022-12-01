# snapcraft(Snappy套件管理器)
可在多種linux中安裝，可以用來安裝軟體及發佈軟體部署。

## 安裝
```
apt-get update
apt-get install snapd
```

## 版本確認
```
snap --version
```

## 移除
```
apt-get remove snapd
```

## snap安裝軟體
```
sudo snap install slack
```

## snap移除已安裝軟體
```
sudo snap remove slack
```

## snap查詢已安裝軟體
```
sudo snap list
```

## snap搜尋可安裝軟體
find後面加入要搜尋的關鍵字
```
sudo snap find slack
```