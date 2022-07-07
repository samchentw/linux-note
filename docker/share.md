# 檔案共享


## 實體機複製到docker container
```
docker cp /path/file1 DOCKER_ID:/path/file2
```

## 複製資料夾
```
docker cp /path/folder DOCKER_ID:/another/path/
```

## docker container複製到實體機
```
docker cp DOCKER_ID:/path/file1 /path/file2
```
## 複製資料夾
```
docker cp DOCKER_ID:/path/folder /path/to/
```