# 遠端

## 複製遠端數據庫
```
git clone <url>
```

## 顯示遠端數據庫
```
git remote
git remote -v # 取得遠端網址
```

## 取得遠端某分支
```
git checkout <branch>
```


## 取得遠端某分支
```
git checkout <branch>
```

## 查看遠端數據庫分支的修改內容
```
git fetch <branch>
```

## 加入遠端數據庫
```
git branch -M master  # 建立主分支
git remote add origin https://github.com/samchentw/xxx.git  # 加入遠端資料庫
git push -u origin master # 第一次推送
```

## 拉取遠端最新資料
```
git pull
git pull --tag # 所有的標籤也一起下載
```

## 推送到遠端
```
git push
git push --tag # 所有的標籤也一起推送
```