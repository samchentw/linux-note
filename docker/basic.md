# docker基本指令

## 建立映像檔
在本地建Dockerfile 檔
 執行以下指令
```
docker build -t mytomcat . --no-cache
 ```

## 清build image catch
```
docker builder prune
```

##  執行映像檔

```
docker run mytomcat

//指定port
docker run -p 8080:8080 mytomcat
```

## 進入虛擬機

```
docker exec  -it {containerID} bash

 docker exec -it mypostgres bash
```

## 移除沒在用的volume
```
docker volume prune
```