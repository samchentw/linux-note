# tar指令


ubuntu tar打包

tar指令只是打包資料，不包含解壓縮，

簡單來說，就是把很多檔案把它們打包起來，

結合成一個檔案。

指令：tar [-參數] [目標位置] [檔案位置]

參數

-c ：建立打包

-t ：開啟預覽

-x ：解開打包

-v：顯示過程

-f：指定打包的名字

## 範例一（打包檔案）把myfolder資料夾打包
```
tar -cvf myfolder.tar myfolder
```

## 範例二（解開打包檔案）
```
tar -xvf new.tar
```


## tar.gz 格式
```
tar -zcvf myfolder.tar myfolder
tar -zxvf myfolder.tar
```

