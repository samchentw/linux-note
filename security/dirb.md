# dirb
可以用來做目錄掃描，dirb掃路徑的方法是用暴力掃描


## 安裝
```
sudo apt update
sudo apt install dirb
```

## 基本使用
```
dirb http://192.168.2.3   //掃描目標為ip時
dirb http://example.com.tw   //掃描目標為網址時
```

## 將輸出結果轉成檔案
```
dirb http://192.168.2.3 -o result.txt
```