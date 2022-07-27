# 網路

## ip指令取代net-tools
```
ip a    # 等同ifconfig
ip addr # 等同ifconfig
ip address # 等同ifconfig
```

## ipv4、ipv6
```
ip -4 addr
ip -6 addr
ip addr show eth0 # 查詢個別網卡的資訊:
```
## 顯示 Routing Table
```
ip route # 或ip route list、ip r
```

## 安裝net-tools網路工具
```
apt install net-tools
```

## 列出開啟的網路服務
```
netstat -pnltu
```

## 檢視網路 Routing table:
```
netstat -nr
```

## 列出網卡使用統計資訊:
```
etstat -ai
```

## 檢查網路卡與IP
```
ifconfig
```

## 電腦名稱
```
hostname
```

## 路由表
```
route
route -n #用ip方式顯示
```

## arp 紀錄
```
arp 
```
