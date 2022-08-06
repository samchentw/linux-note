# Supervisor套件
Supervisor 是 Linux 環境中常用的進程監視器，我們將在以下文檔中討論如何配置它。


## 安裝
```
sudo apt-get install supervisor
```


## laravel 文件範例：
Supervisor 配置文件通常存儲在該/etc/supervisor/conf.d目錄中。在此目錄中，您可以創建任意數量的配置文件，以指示主管如何監控您的進程。例如，讓我們創建一個laravel-worker.conf啟動和監控queue:work進程的文件：

/etc/supervisor/laravel-worker.conf
```
[program:laravel-worker]
process_name=%(program_name)s_%(process_num)02d
command=php /home/jhong/桌面/hr-system-app/artisan queue:work  --max-time=3600
autostart=true
autorestart=true
stopasgroup=true
killasgroup=true
user=jhong
numprocs=8
redirect_stderr=true
stdout_logfile=/home/jhong/桌面/hr-system-app/worker.log
stopwaitsecs=3600

```


## 保存文件，到supervisord.conf 檔後後在最後一行改為以下，如下所示。
```
[include]
files = /etc/supervisor/laravel-worker.conf
```




## supervisor指令
創建配置文件後，您可以更新 Supervisor 配置並使用以下命令啟動進程：
```
sudo supervisorctl reread

sudo supervisorctl update

sudo supervisorctl start laravel-worker:*

sudo supervisorctl stop laravel-worker:*

sudo supervisorctl status

```


## 啟動服務
```
service supervisor start
```

## 關閉服務
```
service supervisor stop
```

## 重啟服務
```
service supervisor restart
```