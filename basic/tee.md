# tee

## 將結果輸入至檔案
```
ls > temp.txt
echo "run" > temp.txt
```


## 將結果輸入至檔案與螢幕(使用管線)
```
ls | tee temp.txt
echo "run" | tee temp.txt
```

## 同時存到檔案和顯示在螢幕上 (附加在 result.txt 原內容後面)
```
ls | tee -a temp.txt
```
## 後面可以把螢幕顯示的結果繼續再用管線做繼續其他處理：
```
ls | tee -a temp.txt | grep aws
```
