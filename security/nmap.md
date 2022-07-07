# nmap 
可以掃描port號、收集目標資訊、服務版本號、作業系統版本、IP偽裝等等

## 安裝
```
sudo apt-get install nmap
```

## 基本主機掃描
```
nmap www.example.net
```

## 掃ip
```
nmap 202.39.253.11
nmap 192.168.0.*
nmap 192.168.0.0/24
nmap 192.168.0.123-140
```

## 詳細資訊(如：SSH 伺服器版本、Apache 伺服器版本、作業系統類型等等)
```
nmap -A www.example.net
```

## 加快掃描的速度
```
nmap -F www.example.net
```

