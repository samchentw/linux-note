# Caddy
以golang寫的server，支援自動從 Let’s Encrypt 取得與更新 TLS 1.3 加密憑證

## 安裝
```
sudo apt install -y debian-keyring debian-archive-keyring apt-transport-https
curl -1sLf 'https://dl.cloudsmith.io/public/caddy/stable/gpg.key' | sudo tee /etc/apt/trusted.gpg.d/caddy-stable.asc
curl -1sLf 'https://dl.cloudsmith.io/public/caddy/stable/debian.deb.txt' | sudo tee /etc/apt/sources.list.d/caddy-stable.list
sudo apt update
sudo apt install caddy
```

## Caddyfile
首先先建立Caddyfile檔
```
localhost {
	respond "Hello, world!"
}

localhost:2016 {
	respond "Goodbye, world!"
}
```
並在終端機執行
```
caddy start
```
在瀏覽器執行
https:localhost  
https:localhost:2016  

## 使用
在終端機執行caddy
```
caddy run
```

在背景執行的caddy
```
caddy start
```

關閉在背景執行的caddy
```
caddy stop
```


## 反向代理
首先先建立Caddyfile檔
```
:2016
reverse_proxy 127.0.0.1:8000
```

並執行
```
caddy run
```

## https
首先先建立Caddyfile檔
```
example.com {
    reverse_proxy 127.0.0.1
}
```

並執行
```
caddy run
```

注意dns要先設定好，要先指向本機IP

## file server
首先先建立Caddyfile檔
```
:2022 {
    file_server
}
```
並執行
```
caddy run
```