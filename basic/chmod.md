# chmod權限(todo)


## 查看檔案權限

```
ll temp.txt
-rw-rw-r-- 1 samchentw samchentw 337  8月 29 21:35 temp.txt
```

## 更改檔案的擁有者
```
sudo chown sam temp.txt
```

# 更改檔案的擁有群組
```
sudo chown :groupname temp.txt
```

# 更改檔案的擁有者與群組
```
sudo chown sam:groupname temp.txt
```

# 遞迴更改整個目錄
```
sudo chown -R sam:groupname myfolder
```

# 說明
R:讀取權限
W:寫入權限
X:執行權權

owner：文件所有者
group：用户组
others：其它用户