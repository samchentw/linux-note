# vim

## 安裝

指令安裝
```
sudo apt update
sudo apt install vim
```

## 基本

建立
```
vim note.txt
```

編輯
```
vim note.txt
```

vim的設定檔案是vimrc，通過如下命令進入vimrc配置檔案
```
sudo vim /etc/vim/vimrc
```
執行完上述命令之後，輸入i，進入編輯模式，可將以下貼上去。
```
 set nu           "在左側行號                                                
 set tabstop      "tab 長度設定為 4
 set nobackup     "覆蓋檔案時不備份
 set cursorline   "突出顯示當前行
 set ruler        "在右下角顯示游標位置的狀態行
 set autoindent   "自動縮排
```