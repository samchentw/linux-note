# apt常用指令


```
# 更新軟體的最新資訊及列表
sudo apt update

# 升級apt
sudo apt upgrade

# 安裝某插件(以vs code為例)
sudo apt install code

# 然後執行，觀看有哪些套件需要更新
apt list --upgradable

# 移除某插件(以vs code為例)
sudo apt remove code

# 移除依賴(刪東西比較乾淨)
sudo apt autoremove

# 清除之前下載的安裝檔 (*.deb)
sudo apt clean

# 同 sudo apt clean，但不刪除仍安裝在電腦中軟體的安裝檔
sudo apt autoclean

# 顯示插件說明
sudo apt show code 

# 檢查是否有損壞的依賴
sudo apt-get check 

# 搜尋插件
apt search gitkraken

# 安裝.deb檔
sudo dpkg -i package_file.deb

# 顯示已安裝項目
apt list --installed

# 顯示可更新套件
apt list --upgradeable
```
